## aframe-select-bar-component

This component creates a menu that can be defined using html option elements and attached to a VR controller.

Work in progress, use at your own risk.

[![Video](https://img.youtube.com/vi/JlfMPgNpm3o/0.jpg)](https://www.youtube.com/watch?v=JlfMPgNpm3o)

For [A-Frame](https://aframe.io).

To Do items:
* remove use of "data" for dynamic properties not specified in DOM. revise functions in city builder that make use of the .data prefix

### API

| Property | Description | Default Value |
| -------- | ----------- | ------------- |
|          |             |               |

### Installation

#### Browser

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.4.0/aframe.min.js"></script>
  <script src="https://unpkg.com/aframe-select-bar-component/dist/aframe-select-bar-component.min.js"></script>
</head>

<body>
  <a-scene>
    <a-entity select-bar="foo: bar"></a-entity>
  </a-scene>
</body>
```

<!-- If component is accepted to the Registry, uncomment this. -->
<!--
Or with [angle](https://npmjs.com/package/angle/), you can install the proper
version of the component straight into your HTML file, respective to your
version of A-Frame:

```sh
angle install aframe-select-bar-component
```
-->

#### npm

Install via npm:

```bash
npm install aframe-select-bar-component
```

Then require and use.

```js
require('aframe');
require('aframe-select-bar-component');
```
