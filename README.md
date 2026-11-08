# Darks 3DViewer

Darks 3DViewer is a free and open source web solution to visualize and explore 3D models in your browser. This repository contains the source code of the website and the engine behind it.

[Live website](https://3dviewer.net) &nbsp;-&nbsp; [Website manual](https://3dviewer.net/info) &nbsp;-&nbsp; [Developer documentation](docs/index.html) &nbsp;-&nbsp; [Report an issue](https://github.com/DarkLabsStudio/Darks-3DViewer/issues)

## Engine

The engine can be used on any website to embed 3D models. It is distributed as the `darks-3dviewer` package and as a browser-ready bundle attached to every release.

```bash
npm install darks-3dviewer
```

```js
import * as OV from 'darks-3dviewer';
```

See the [developer documentation](docs/index.html) for the full API, embedding options and the migration guide.

## Supported file formats

* **Import**: 3dm, 3ds, 3mf, amf, bim, brep, dae, fbx, fcstd, gltf, ifc, iges, step, stl, obj, off, ply, wrl.
* **Export**: 3dm, bim, gltf, obj, off, stl, ply.

## Development

Install the dependencies, then start the development build and the local web server:

```bash
npm install
npm start
```

Useful scripts:

* `npm run build_dev` - build the engine and the website in development mode.
* `npm run build_engine` - build the minified engine bundle.
* `npm run build_website` - build the minified website bundle.
* `npm test` - run the test suite.
* `npm run lint` - run the linter.

The build requires Node.js and Python 3.

## External libraries

Darks 3DViewer uses these wonderful libraries: [three.js](https://github.com/mrdoob/three.js), [pickr](https://github.com/Simonwep/pickr), [fflate](https://github.com/101arrowz/fflate), [draco](https://github.com/google/draco), [rhino3dm](https://github.com/mcneel/rhino3dm), [web-ifc](https://github.com/tomvandig/web-ifc), [occt-import-js](https://github.com/kovacsv/occt-import-js).

## Credits

Darks 3DViewer is a rebranded fork of [Online 3D Viewer](https://github.com/kovacsv/Online3DViewer), created by Viktor Kovács and released under the MIT license. The original project is the foundation of this codebase, and its copyright notice is preserved in [LICENSE.md](LICENSE.md).

## License

MIT. See [LICENSE.md](LICENSE.md) for details.
