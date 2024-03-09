# Source Code Editor

Source Code Editor plugin for [Tinymce WYSIWYG Editor](https://www.tiny.cloud/) built alongside [ACE](https://ace.c9.io/#nav=about&api=editor)

![preview](/preview.png)

To use this plugin copy the folder "codeeditor" and paste it into tinymce "plugins" folder in its source directory.
Here's the path for tinymce_6.8.3 self-hosted production release -> tinymce_6.8.3/tinymce/js/tinymce/plugins

Download any of tinymce self-hosted releases [here](https://download.tiny.cloud/tinymce/community/tinymce_6.8.3.zip) or
[dev](https://download.tiny.cloud/tinymce/community/tinymce_6.8.3_dev.zip)

## Tutorial
### Initializing
In order to have it in your editor, after including _codeeditor_ folder in your tinymce plugins directory, you must tell tinymce to inlcude the plugin as well as its toolbar button as demonstrated bellow...
```javascript
tinymce.init({
    selector: "#target-element", // change this value according to your HTML target element selector
    toolbar: ["codeeditor"],
    plugins: ["codeeditor"],
});
```
### Plugin configuration
The following configuration options are provided:
  1. __codeeditor_themes_pack__ -> EITHER a __string__ with a set of words matching _ACE_ theme names with a space inbetween them OR an __array__ of strings, each matching any _ACE_ theme name. Default is _"chrome dreamweaver eclipse github github_dark xcode twilight"_.

Check out _ACE_ available themes [here](https://github.com/ajaxorg/ace/tree/master/src/theme). Preview [here](https://ace.c9.io/build/kitchen-sink.html).

  2. __codeeditor_wrap_mode__ -> Boolean. Default is __true__. If set to __false__, long lines won't be wrapped automatically to fit modal view size and therefore horizontal scrolling will be available.

  3. __codeeditor_font_size__ -> Number representing height in pixels. Default is __16__.
    
```javascript
      tinymce.init({
          selector: "#target-element", // change this value according to your HTML target element selector
          toolbar: ["codeeditor"],
          plugins: ["codeeditor"],
          codeeditor_themes_pack: "chrome dreamweaver eclipse github github_dark xcode twilight", // or ['chrome', 'dreamweaver', 'eclipse', 'github', 'github_dark', 'xcode', 'twilight']
          codeeditor_wrap_mode: true,
          codeeditor_font_size: 16
      });
```


