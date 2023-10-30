```
6Le5xuEoAAAAAH1IZ8Xe0YRm_eo5zTukw2KQqQeM
```
website key
```
6Le5xuEoAAAAAJ8M8y44oKM7Uj-J5PqR_FJ34vEx
```
secret key


Adding a CAPTCHA to a registration form is a good way to protect your website from automated bot submissions. Google's reCAPTCHA is a popular and user-friendly CAPTCHA service that you can integrate into your registration form. Here are the steps to add reCAPTCHA to your Angular registration form:

1. **Sign Up for reCAPTCHA:**

   Go to the [reCAPTCHA website](https://www.google.com/recaptcha) and sign in with your Google account. Click on "Admin Console" to create a new site.

2. **Register Your Site:**

   In the reCAPTCHA admin console, click on the "+" button to register a new site. Choose the reCAPTCHA type you want (reCAPTCHA v2 "I'm not a robot" Checkbox or reCAPTCHA v3) and enter your domain details.

3. **Get Your Site Key and Secret Key:**

   After registering your site, you'll be provided with a site key and a secret key. You will use these keys to integrate reCAPTCHA into your Angular application.

4. **Integrate reCAPTCHA into Your Angular Application:**

   In your Angular project, you can use the `ngx-captcha` library to integrate reCAPTCHA. Here's how to do it:

   First, install the library using npm:

   ```bash
   npm install ngx-captcha
   ```

   Next, integrate reCAPTCHA into your registration form component:

   ```typescript
   import { Component } from '@angular/core';
   import { FormBuilder, FormGroup, Validators } from '@angular/forms';
   import { RecaptchaValidatorService } from 'ngx-captcha';

   @Component({
     selector: 'app-registration',
     templateUrl: './registration.component.html',
     styleUrls: ['./registration.component.css']
   })
   export class RegistrationComponent {
     registrationForm: FormGroup;

     constructor(private formBuilder: FormBuilder, private recaptchaValidatorService: RecaptchaValidatorService) {
       this.registrationForm = this.formBuilder.group({
         // Your other form fields here
         // ...
         recaptcha: ['', [Validators.required], [this.recaptchaValidatorService.validate()]]
       });
     }

     onSubmit() {
       if (this.registrationForm.valid) {
         // Handle form submission, e.g., make an API request
       }
     }
   }
   ```

   In this code, we import the `RecaptchaValidatorService` from `ngx-captcha` and add a `recaptcha` form field to your form. The `RecaptchaValidatorService` is used to validate the reCAPTCHA response.

   In your HTML template, add the reCAPTCHA widget:

   ```html
   <form [formGroup]="registrationForm" (ngSubmit)="onSubmit()">
     <!-- Your other form fields here -->

     <recaptcha-container [siteKey]="yourSiteKey"></recaptcha-container>

     <button type="submit" [disabled]="registrationForm.invalid">Register</button>
   </form>
   ```

   Replace `yourSiteKey` with your actual reCAPTCHA site key.

5. **Configure reCAPTCHA in Your App:**

   In your Angular app module, provide your reCAPTCHA site key and secret key in the `RECAPTCHA_SETTINGS` provider:

   ```typescript
   import { NgModule } from '@angular/core';
   import { RecaptchaFormsModule, RECAPTCHA_SETTINGS, RecaptchaSettings } from 'ngx-captcha';

   const recaptchaSettings: RecaptchaSettings = { siteKey: 'yourSiteKey', secretKey: 'yourSecretKey' };

   @NgModule({
     imports: [RecaptchaFormsModule],
     providers: [
       { provide: RECAPTCHA_SETTINGS, useValue: recaptchaSettings }
     ]
   })
   export class YourAppModule { }
   ```

   Replace `yourSiteKey` and `yourSecretKey` with your actual reCAPTCHA site key and secret key.

6. **Test and Deploy:**

   Make sure to test your registration form with reCAPTCHA locally to ensure it's working as expected. Once you're satisfied, deploy your Angular application to your server.

Now, your registration form should include reCAPTCHA, which will help protect your site from automated bot submissions. Users will be required to complete the reCAPTCHA challenge to submit the registration form.
