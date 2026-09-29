# SfM Pipeline Explorer

An interactive, browser-based lab that walks students through the drone photogrammetry pipeline. It shows how overlapping photos become a 3D point cloud and then an orthomosaic using Structure from Motion (SfM).

## What it covers

The page follows one simulated survey flight through six steps:

1. **Capture:** plan a lawnmower flight and adjust altitude, front overlap and side overlap. See the photo footprints, an overlap-count map, photo spacing and ground sample distance (GSD).
2. **Match:** feature detection (for example with SIFT) and tie points. Rays link one ground point to every camera that photographed it.
3. **Align:** triangulation and bundle adjustment. Camera poses and the sparse point cloud settle as the reprojection error falls.
4. **Densify:** multi-view stereo builds a dense point cloud.
5. **Surface:** a Digital Surface Model (DSM), shown by elevation or in true colour.
6. **Orthomosaic:** a raw perspective photo next to the orthomosaic, showing relief displacement (d = r · h / H) and mosaic seamlines.

Each step has a short explanation and a "Try this" prompt that can be used as a lab question.

## Using it

- Open `index.html` in any modern browser. There is no installation, build step or server.
- Drag to orbit the 3D view and scroll to zoom.
- To host it, enable GitHub Pages under **Settings → Pages → Deploy from a branch** (`main`, `/ (root)`).
- To embed it in Canvas, link to the live page or add it with an iframe.

## Notes

- The site, terrain, building, flight and camera are **simulated for teaching**. The example camera has a 1-inch, 20 MP sensor (13.2 × 8.8 mm, 5472 px wide) with an 8.8 mm lens.
- Point densities are kept far lower than in a real project so the page runs smoothly on any device.
- Some values on the page are teaching rules of thumb, not fixed standards, for example "at least 5 photos per spot" and "RMS reprojection error under about 1 px".
- The page is a single self-contained HTML file. It only loads Google Fonts from outside, and falls back to system fonts if those are unavailable.
- References are listed at the bottom of the page.

## Author

Jon Caris, Tufts University. Developed with assistance from Claude (Anthropic).

## License

Add a license of your choice, for example CC BY 4.0 for the teaching content or MIT for the code.

