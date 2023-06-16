# A-Frame-Component: Simplify-Modifier 
<img src="img/screenshot.gif" title="Video screen capture" alt="Video screen capture" height="400">

### **Description / Rationale**
This is A-Frame component for simplification of GLTF meshes. It is the adaptation of similar <a href="https://threejs.org/examples/webgl_modifier_simplifier.html">example</a> made in Three.js with additional features:
* Simplification of multiple gltf meshes
* Assigning color to simplified mesh
* Enabling wireframe of simplified mesh.


### **Instructions**
In order to use the component attach "simplify-modifier" to a-entity with gltf-model component. The component has the following attributes: 
* <b>color: { type: 'color', default: '#ffffff' }</b> - Color of the simplified mesh
* <b>wireframe: { type: 'boolean', default: false }</b> - Whether to show wireframe of simplified mesh or not
* <b>count: { type: 'number', default: 0.7 }</b> - Vertices to remove. Accepts values from 0 to 1. 
* <b>offset: { type: 'number', default: 1 }</b>

The code below shows the sample implementation of the component:
```
<html>
<head>
    <meta charset='utf-8' />
    <title>A-Frame Component: Mapbox</title>
    <meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
    <script src="https://aframe.io/releases/1.4.2/aframe.min.js"></script>
    <script src="js/mapbox-component.js">
    </script>
</head>
<body>
     <a-scene>
        <a-plane mapbox-component="attach: true" position="0 0 -3" rotation="0 0 0" width="8" height="5"
            color="#ddd"></a-plane>       
        <a-camera position="0 0 0" cursor="rayOrigin: mouse;" raycaster="objects: .clickable"></a-camera>
        <a-sky color="#ECECEC"></a-sky>
    </a-scene>
</body>
</html>
```
Please note that a-camera primitive is used with raycast and rayorigin to enable click events. Without it navigation buttons will not work! 
If you want to use it in VR, just attach laser pointer with raycaster showing to .clickable class.

### **Tech Stack**
The project is powered by AFrame and Three.js.

### **Demo**
See demo of the component here: [Demo](mapbox-component.glitch.me/)
