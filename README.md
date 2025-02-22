cat <<EOL > README.md
# Angular Jitsi Meet Integration

This project provides Angular wrappers for select Jitsi Meet modules, such as \`xmpp\` and \`RTC\`. These wrappers are CommonJS modules that integrate Jitsi Meet functionalities into Angular applications using browserify.

Upon requiring \`angular-jitsi-meet\`, a global \`APP\` object is created and attached to the \`window\`, with each Jitsi Meet module wrapped in Angular and its events wired to the Angular event bus. The Angular service names correspond to the module names on the \`APP\` object.

## Setup Instructions

### 1. Install the Package
Add \`angular-jitsi-meet\` to your project's dependencies:
\`\`\`bash
npm install angular-jitsi-meet --save
\`\`\`

### 2. Include the Module in Your Application
In your Angular application's main module file, require \`angular-jitsi-meet\` and add it as a dependency:
\`\`\`javascript
angular.module('app', [require('angular-jitsi-meet')])
  .run(function(xmpp, RTC) {
    // Utilize the xmpp and RTC modules here
  });
\`\`\`

### 3. Utilize Jitsi Modules
Inject the desired Jitsi modules (e.g., \`xmpp\`, \`RTC\`, \`settings\`, \`statistics\`, \`connectionquality\`, \`desktopsharing\`, or \`jitsiApp\`) into your Angular components as needed.

For more details and updates, visit the project's [GitHub repository](https://github.com/pstros/angular-jitsi-meet).
EOL


