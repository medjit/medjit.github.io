# JSketcher on GitHub Pages

This repository is solely for hosting the JSketcher app via GitHub Pages, allowing everyone to access and use it directly in their browser. It is not the original source repository.

The original JSketcher project was created by [xibyte](https://github.com/xibyte/jsketcher). A big thank you to xibyte for developing this amazing parametric 2D and 3D CAD modeler!

For the full source code, please visit the [original repository](https://github.com/xibyte/jsketcher). The source code is also available in this repo as `jsketcher-main.zip`.

## About JSketcher

JSketcher is a **parametric** 2D and 3D CAD modeler written in pure JavaScript.

<a href='https://www.youtube.com/watch?v=Vk3TTp8hNxQ&list=PLeoCiKHizvH8PZEyFvThHzVlnTF5XaL-R'> 
    <img src='https://raw.githubusercontent.com/xibyte/jsketcher/main/web/img/sample2d.png' width='400px'>
    <img src='https://raw.githubusercontent.com/xibyte/jsketcher/main/web/img/sample3d.png' width='400px'> 
</a>

[YouTube Tutorial Video](https://www.youtube.com/watch?v=Vk3TTp8hNxQ&list=PLeoCiKHizvH8PZEyFvThHzVlnTF5XaL-R)

[Live Sample Demo](http://web-cad.org/?com.github.jsketcher-sample-models.MODELS.Flag-Holder)

[2D Sketcher](http://web-cad.org/sketcher.html#__sample2D__)

[Help Docs](https://github.com/xibyte/jsketcher/blob/main/web/docs/index.md)

[Workbench Dev Guide](https://github.com/xibyte/jsketcher/blob/main/dev-guide/index.md)

[Commercial Licensing](https://www.autodrop3d.com/parametric-cad-beta.html) 

Please consider supporting the original project by becoming a backer.

<a href="https://opencollective.com/jsketcher-ad3d/"><img src="https://opencollective.com/jsketcher-ad3d/tiers/backer.svg?avatarHeight=300&width=3000"><img src="https://opencollective.com/jsketcher-ad3d/tiers/badge.svg"></a>

### Current Status

JSketcher is a parametric 3D modeler employing a 2D constraint solver for sketches and the feature/history metaphor to build models. The 2D constraint solver is completely written in JavaScript/TypeScript and is implemented in both the 3D CAD and the 2D sketcher. Originally developed by xibyte to make models for 3D printing. Today, JSketcher provides a rich set of tools for visualizing, selecting/interacting with 3D geometry, tracking and storing model history, all built on the foundation of the 2D sketcher engine and employing OpenCascade for solid modeling operations.

### Major Components and Features

* **Geometric Constraint Solver**: This is the most crucial component, allowing the solving of a system of geometric constraints applied to a sketch. See below for the list of supported constraints.
* **2D Sketcher**: Allows designing 2D sketches with geometric constraints. Uses HTML5 canvas for rendering.
* **3D Boolean Engine**: OpenCascade is used to perform booleans on BREP objects.
* **Feature History**: Accumulates features to build a 3D model step by step. A compare step propagates edge/face IDs forward for stability.
* **Export**: To **STL**, **DWG**, and **SVG** formats.
* **Saving Projects**: In the browser's local storage.
* **Repository of Dimensions**: Symbolic dimensions for constraints, allowing dynamic updates.
* **2D Measurement Tool**: Adds dimensions on 2D drawings (Linear, Vertical, Horizontal, Arc/Circle).
* **No Server-Side Needed**: Only client-side JavaScript and WASM.

This modeler is used for:
* Designing 3D models for 3D printing, based on parametric 2D sketches, exportable as STL.
* Creating 2D parametric sketches, exportable to DWG or SVG.

### Supported Constraints

* Coincident
* Vertical
* Horizontal
* Parallel
* Perpendicular
* Point to Line Distance
* Point to Object Distance
* Entity Equality (radius/length)
* Tangent
* Radius
* Point On Line
* Point On Arc / Ellipse
* Point In Middle
* Angle
* Symmetry
* Lock Convexity
* Fillet Meta Constraint

### Get Started With the Code

To work with the source code from the original repo:

Install Node.js

* `$ cd <jsketcher folder>`
* `$ npm install`
* `$ npm start`

Contributing: Please see the [original contributing guide](https://github.com/xibyte/jsketcher/blob/main/.github/CONTRIBUTING.md).