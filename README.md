# Slackula
Slack Dark Mode

## Installation

Append the following to `/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js`


```
/**
 * Add Darkmode
 */
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/Cam/Slackula/master/slackula.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
To inspect Slack app to create/update styles, in terminal launchctl setenv SLACK_DEVELOPER_MENU true, then restart Slack app.
```
