cat <<EOL > README.md
# Angular Jitsi Meet Integration

This project provides Angular wrappers for select Jitsi Meet modules, such as \`xmpp\` and \`RTC\`. These wrappers are CommonJS modules that integrate Jitsi Meet functionalities into Angular applications using browserify.

Upon requiring \`angular-jitsi-meet\`, a global \`APP\` object is created and attached to the \`window\`, with each Jitsi Meet module wrapped in Angular and its events wired to the Angular event bus. The Angular service names correspond to the module names on the \`APP\` object.

## Setup Instructions

### 1. Prerequisites
Ensure you have the following installed on your machine:
- [Node.js](https://nodejs.org/) (LTS version recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Angular CLI](https://angular.io/cli)

If Angular CLI is not installed, run:
```bash
npm install -g @angular/cli
```

### 2. Clone the Repository
Clone this project from GitHub:
```bash
git clone https://github.com/pstros/angular-jitsi-meet.git
cd angular-jitsi-meet
```

### 3. Install Dependencies
Run the following command to install all necessary dependencies:
```bash
npm install
```

### 4. Include the Module in Your Application
In your Angular application's main module file, require \`angular-jitsi-meet\` and add it as a dependency:
```javascript
angular.module('app', [require('angular-jitsi-meet')])
  .run(function(xmpp, RTC) {
    // Utilize the xmpp and RTC modules here
  });
```

### 5. Start the Application
Run the following command to serve the application locally:
```bash
ng serve
```
The application should now be running at [http://localhost:4200](http://localhost:4200).

### 6. Build for Production
To create a production build of the application, run:
```bash
ng build --prod
```

### 7. Utilize Jitsi Modules
Inject the desired Jitsi modules (e.g., \`xmpp\`, \`RTC\`, \`settings\`, \`statistics\`, \`connectionquality\`, \`desktopsharing\`, or \`jitsiApp\`) into your Angular components as needed.

For more details and updates, visit the project's [GitHub repository](https://github.com/pstros/angular-jitsi-meet).
