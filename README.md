## ricoh-theta-viewer (Not maintained)

This is a [npm package](https://www.npmjs.com/package/ricoh-theta-viewer) which I used for rendering 360 degree images onto my ionic mobile project. The images were captured using a Ricoh Theta S.
Major portion of this repo was copied from [Aike-thview.js](https://github.com/aike/thview.js). I have created this new repository because, the old one did not have some of the components like touch event handlers and disposing of the renderer object. On a device, the renderer, if kept running will eat up the GPU memory and the application will crash at some point of time (for my device, it took only 4 images to crash). Let me know if you need more help on this.

### How to use?

Since the three.min.js is already bundled with this npm package, do the following - 

`import { RicohView } from 'ricoh-theta-viewer';`

`this.ricohView = new RicohView({ id: "ricoh-360-viewer", file: <fileName>, rendererType: 0, height: window.innerHeight, width: window.innerWidth, zoom: 130 });`

`<div id="ricoh-360-viewer"></div>` on your html page.

- Use _ricohView_ object to call the _stopRendering()_ from your code.

Find the app at [Google Drive](https://drive.google.com/open?id=0B_Li6uw9FByMd19kamlDOS13YkU)


### Note

I am only supporting the WebGL renderer for now. Aike's repo supported Canvas and CSS3D as well. Also, the [repo](https://github.com/aike/thview.js) did not have any provision for stopping the renderer animation. So added _stopRendering()_.
