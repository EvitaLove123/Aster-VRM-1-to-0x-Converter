# Aster VRM 1.0 → 0.0 Converter

A browser-based Android-friendly converter that loads a VRM 1.0 file and exports VRM 0.0.

## Use
1. Open the GitHub Pages site.
2. Choose a `.vrm` file containing the `VRMC_vrm` extension.
3. Wait for the model to load in the preview.
4. Select **Export VRM 0.0**.

The model is processed locally in the browser; this project does not upload model files to a server.

## Compatibility notes
- Output is **VRM 0.0** (the legacy VRM 0.x schema); there is no separate VRM 0.1 target in this tool.
- VRM 1.0 features that have no direct VRM 0.0 equivalent may be omitted or approximated. In particular, node constraints are not represented in VRM 0.0.
- Always validate the exported file in the target app. This tool cannot guarantee acceptance by every VRM application.
- The exporter does not claim to be UniVRM and does not fabricate UniVRM metadata.

## GitHub Pages
In the repository, open **Settings → Pages** and set the build/deployment source to **GitHub Actions**. The workflow in `.github/workflows/pages.yml` publishes the root site.

## Exporter attribution
The conversion/export core in `src/VRMExporter.js` is adapted from **Ringo3apples/vrm-exporter**, licensed under MIT. See `THIRD_PARTY_LICENSES.md` and `LICENSE.vrm-exporter`.

## Dependencies
- Three.js 0.184.0
- @pixiv/three-vrm 3.5.3
