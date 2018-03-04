# Slackula
Dark Mode for Slack on MacOS

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
```

## Creating new themes

To inspect Slack app to create/update styles, in terminal launchctl setenv SLACK_DEVELOPER_MENU true, then restart Slack app.

## Credits

* [Theming Slack for OSx by @DrewML](https://gist.github.com/DrewML/0acd2e389492e7d9d6be63386d75dd99)
* [SBlack by @frankdilo](https://github.com/frankdilo/sblack)
