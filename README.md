# css-search-v2

[DEMO](##)
> **Provide a live demo of your plugin**
For a better user engagement create a simple live demo by using services like [JSFiddle](https://jsfiddle.net) [CodeSandbox](https://codesandbox.io) [CodePen](https://codepen.io) and link it here in your README (attaching a screenshot/gif will also be a plus).
To help you in this process here below you will find the necessary HTML/CSS/JS, so it just a matter of copy-pasting on some of those services. After that delete this part and update the link above

# IMPORTANT
This grapesjs extension is the copy of the [grapesjs-ui-suggest-classes](https://github.com/silexlabs/grapesjs-ui-suggest-classes) extension, what this extension enables is to read the styles that you yourself added in the localstorage of your project (check the code to see how it works) it is intended for large projects with large amount of styles as it is optimized for large amount of CSS parameters and created for elements that are added from outside the project, if you want to see how it really works, you can try adding large styling components and you will see that it can read them at high speed and include tags (#id) that you have in your localstorage. (It works with all the pages in case you have several in the same project). And the characteristics of my predecessor are preserved.

#### Intended for large amounts of CSS code or for large projects.

### HTML
```html
<link href="https://unpkg.com/grapesjs/dist/css/grapes.min.css" rel="stylesheet">
<script src="https://unpkg.com/grapesjs"></script>
<script src="https://unpkg.com/css-search-v2"></script>

<div id="gjs"></div>
```

### JS
```js
const editor = grapesjs.init({
	container: '#gjs',
  height: '100%',
  fromElement: true,
  storageManager: false,
  plugins: ['css-search-v2'],
});
```

### CSS
```css
body, html {
  margin: 0;
  height: 100%;
}
```

## Options

| Option | Description | Default |
|-|-|-|
| `containerStyle` | The css style of the tags container | check the source code |
| `tagStyle` | The css style of the tags | check the source code |
| `enablePerformance` | Display execution times | false |
| `enableCount` | Compute and display the number of components using each CSS class, and order classes accordingly. The algorithm for this is not very efficient yet and impacts preformances | true |

## Download

* CDN
  * `https://unpkg.com/css-search-v2`
* NPM
  * `npm i css-search-v2`
* GIT
  * `git clone https://github.com/VMASPAD/css-search-v2.git`



## Usage

Directly in the browser
```html
<link href="https://unpkg.com/grapesjs/dist/css/grapes.min.css" rel="stylesheet"/>
<script src="https://unpkg.com/grapesjs"></script>
<script src="path/to/css-search-v2.min.js"></script>

<div id="gjs"></div>

<script type="text/javascript">
  var editor = grapesjs.init({
      container: '#gjs',
      // ...
      plugins: ['css-search-v2'],
      pluginsOpts: {
        'css-search-v2': { /* options */ }
      }
  });
</script>
```

Modern javascript
```js
import grapesjs from 'grapesjs';
import plugin from 'css-search-v2';
import 'grapesjs/dist/css/grapes.min.css';

const editor = grapesjs.init({
  container : '#gjs',
  // ...
  plugins: [plugin],
  pluginsOpts: {
    [plugin]: { /* options */ }
  }
  // or
  plugins: [
    editor => plugin(editor, { /* options */ }),
  ],
});
```



## Development

Clone the repository

```sh
$ git clone https://github.com/VMASPAD/css-search-v2.git
$ cd css-search-v2
```

Install dependencies

```sh
$ npm i
```

Start the dev server

```sh
$ npm start
```

Build the source

```sh
$ npm run build
```



## License

MIT
