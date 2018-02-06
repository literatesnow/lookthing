# LookThing

LookThing is a very lightweight lightbox written in pure JavaScript.

## Features

* Display image title, description, licence and date
* Next/previous/close buttons
* Keyboard shortcuts that no one knows about
* Very customisable by editing the source code

### Keyboard Shortcuts

* ``Escape``: Close the lightbox
* ``Space/Right Arrow``: Next image
* ``Backspace/Left Arrow``: Previous image

## Usage

All elements with the ``data-lookthing`` attribute will display a lightbox with the corresponding image when clicked.

The ``data-lookthing`` attribute value can either be the name of another attribute of the image to display or the image itself.

```html
  <!-- Image is in the href attribute -->
  <a href="example1.jpg"
     data-lookthing="href"
     data-lookthing-title="First Example"
     data-lookthing-desc="This is the first example."
     data-lookthing-date="2018-02-06 15:04"
     data-lookthing-attribution-name="Me"
     data-lookthing-attribution-uri="http://example.com/images/one/">
    <img src="example1.jpg" alt="Example 1">
  </a>

  <!-- ...or the image is specified directly -->
  <div data-lookthing="example1.jpg"></div>
```

```javascript
  new LookThing({
    imageLicense: {
      name: 'CC BY-SA 4.0',
      uri: 'https://creativecommons.org/licenses/by/4.0/'
    },
    baseDir: './' //[Optional] Assets directory (the loading image)
  });
```

## Examples

See the example [page](example/example.html) or view in [action](https://www.nisda.net/photos.html).

## Browser Support

Uses CSS3 [background-size](https://caniuse.com/#search=background-size) and [flexbox](https://caniuse.com/#search=flexbox). Tested with recent versions of Chrome and Firefox.
