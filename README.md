## aframe-select-bar-component

This [A-Frame](https://aframe.io) component creates a menu that can be defined using html option elements and attached to a VR controller.

This component is inspired by the HTML5 standard [`select`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) element including [`optgroup`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup) element for grouping options together. The idea was to create a VR UI component which mimicked an existing traditional HTML standard.

I made this component out of necessity. When creating a [WebVR app](https://github.com/kfarr/aframe-city-builder) using A-Frame, I wanted a simple way to allow a user to select from a large number of objects organized in multiple categories.

I wrote up a description coming up with the component design here: https://medium.com/@kfarr/building-a-vr-user-interface-for-a-frame-city-builder-38b0c86ed7b7

[![Video](https://img.youtube.com/vi/JlfMPgNpm3o/0.jpg)](https://www.youtube.com/watch?v=JlfMPgNpm3o)

### Requirements and Limitations
* WebVR, HTC Vive and/or Oculus Rift
* (!) This component only supports at least 7 options in each optgroup. If you have fewer than 7 options things will break and unicorns will cry.

### Usage
* Add JavaScript file for the component and a reference to arrow object asset
* Add the `select-bar` component to an element in your scene, recommended as a child beneath an element with `oculus-touch-controls` or `vive-controls` components
* Hook into your code somehow so it does something. [Check out this example](https://github.com/kfarr/aframe-select-bar-component/blob/master/examples/basic/debug-controls.js), using code in `debug-controls` component to show how it might be used in an app
* Make some changes to improve this component, [see open issues](https://github.com/kfarr/aframe-select-bar-component/issues)

### Installation

#### Browser

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
  <script src="https://rawgit.com/ngokevin/aframe-animation-component/master/dist/aframe-animation-component.js"></script>
  <script src="https://rawgit.com/kfarr/aframe-select-bar-component/master/dist/aframe-select-bar-component.min.js"></script>
</head>

<body>
  <a-scene>

    <a-assets>
      <a-asset-item id="env_arrow" src="https://rawgit.com/kfarr/aframe-select-bar-component/master/examples/assets/env_arrow.obj"></a-asset-item>
    </a-assets>

    <a-entity id="leftController" oculus-touch-controls="hand: left" vive-controls="hand: left" >
      <a-entity select-bar="controllerID: leftController" id="menuActions" scale="0.7 0.7 0.7" position="0 0.05 0.08" rotation="-85 0 0">
        <optgroup label="Actions" value="actions">
          <option value="teleport" src="icon_teleport.png" selected>Teleport</option>
          <option value="save" src="icon_save.png">Save</option>
          <option value="saveAs" src="icon_saveAs.png">Save As Copy</option>
          <option value="new" src="icon_new.png">New</option>
          <option value="erase" src="icon_erase.png">Erase</option>
          <option value="inspect" src="icon_inspect.png">Inspect</option>
          <option value="exit" src="icon_exit.png">Exit</option>
        </optgroup>
      </a-entity>
    </a-entity>

  </a-scene>
</body>
```


### API

| Property | Description | Default Value |
| -------- | ----------- | ------------- |
|          |             |               |
