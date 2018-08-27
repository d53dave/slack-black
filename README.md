# slack-black

Copied this code from [laCour/slack-night-mode](https://github.com/laCour/slack-night-mode) to fix an annoying issue with low contrast text in menus.

## Usage

Append the following snippet to any file that Slack will interpret inside it's WebApp, for example `/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js`.

```
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
    url: 'https://raw.githubusercontent.com/d53dave/slack-black/master/black.css',
    success: function(css) {
      $("<style></style>").appendTo('head').html(css);
    }
  });
});
```

