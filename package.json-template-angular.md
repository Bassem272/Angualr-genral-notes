```json
{
  "name": "art-gallery",
  "version": "0.0.0",
  "scripts": {
    "ng": "ng",
    "start": "ng serve",
    "build": "ng build",
    "watch": "ng build --watch --configuration development",
    "test": "ng test"
  },
  "private": true,
  "dependencies": {
    "@angular/animations": "^16.2.0",
    "@angular/cdk": "^16.2.4",
    "@angular/common": "^16.2.0",
    "@angular/compiler": "^16.2.0",
    "@angular/core": "^16.2.0",
    "@angular/forms": "^16.2.0",
    "@angular/material": "^16.2.4",
    "@angular/platform-browser": "^16.2.0",
    "@angular/platform-browser-dynamic": "^16.2.0",
    "@angular/router": "^16.2.0",
    "@fortawesome/angular-fontawesome": "^0.13.0",
    "@fortawesome/fontawesome-free": "^6.4.2",
    "@fortawesome/fontawesome-svg-core": "^6.4.2",
    "@fortawesome/free-brands-svg-icons": "^6.4.2",
    "@fortawesome/free-regular-svg-icons": "^6.4.2",
    "@fortawesome/free-solid-svg-icons": "^6.4.2",
    "bootstrap": "^5.3.1",
    "rxjs": "~7.8.0",
    "tslib": "^2.3.0",
    "zone.js": "~0.13.0"
  },
  "devDependencies": {
    "@angular-devkit/build-angular": "^16.2.1",
    "@angular/cli": "~16.2.1",
    "@angular/compiler-cli": "^16.2.0",
    "@types/jasmine": "~4.3.0",
    "jasmine-core": "~4.6.0",
    "karma": "~6.4.0",
    "karma-chrome-launcher": "~3.2.0",
    "karma-coverage": "~2.2.0",
    "karma-jasmine": "~5.1.0",
    "karma-jasmine-html-reporter": "~2.1.0",
    "typescript": "~5.1.3"
  }
}
```
UPDATE src/app/admin/admin.module.ts (638 bytes)
PS F:\ArtGallery> npm install bootstrap


115 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS F:\ArtGallery> ng add @angular/material
ℹ Using package manager: npm
✔ Found compatible package version: @angular/material@16.2.4.
✔ Package information loaded.

The package @angular/material@16.2.4 will be installed and executed.
Would you like to proceed? Yes
✔ Packages successfully installed.
? Choose a prebuilt theme name, or "custom" for a custom theme: Indigo/Pink        [ Preview: 
https://material.angular.io?theme=indigo-pink ]
? Set up global Angular Material typography styles? Yes  
? Include the Angular animations module? Include and enable animations
✔ Packages installed successfully.
UPDATE src/app/app.module.ts (423 bytes)
UPDATE angular.json (2855 bytes)
UPDATE src/index.html (578 bytes)
UPDATE src/styles.css (181 bytes)
PS F:\ArtGallery> npm install @fortawesome/fontawesome-free

added 1 package, and audited 1016 packages in 19s
115 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS F:\ArtGallery> npm i --save @fortawesome/fontawesome-svg-core @fortawesome/free-brands-svg-icons @fortawesome/free-regular-svg-icons 
@fortawesome/free-solid-svg-icons


115 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS F:\ArtGallery> npm i --save @fortawesome/angular-fontawesome

added 1 package, and audited 1022 packages in 10s

115 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS F:\ArtGallery> 
