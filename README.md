# TEER Lab v0.1.0

Interactive 3D educational simulator for transcatheter edge-to-edge repair.

Unofficial educational geometry prototype. Not for clinical use or a substitute for supervised device training. No patient data. No affiliation with Abbott.

## Run
Open `index.html` in a modern browser. No installation, build, server or external dependencies are required. WebGL is preferred; Canvas is the fallback. Browser rendering has not been independently verified.

## Repository and deployment
- Repository: https://github.com/jorge0061/teer-lab
- GitHub Pages target: https://jorge0061.github.io/teer-lab/
- Under Settings → Pages, select Deploy from a branch → main → / (root).
- The repository root contains the buildless application. `.nojekyll` disables Jekyll processing.
- Publication is complete only after GitHub Pages deploys successfully.

## Test
Run `node test.cjs`. This checks the JavaScript syntax and numerical model invariants, not anatomical or clinical accuracy.

## v0.1.0
- Initial standalone port of the conversation prototype.
- System push/pull translates the entire distal system along a fixed septal entry axis; curvature, orientation and puncture point remain unchanged in this approximation.
- Independent guide and sleeve axial frames, simplified straddle, independent grippers, geometric TEE slices and WebGL/Canvas view.
- Selected dimensions referenced from the SlicerHeart research model (not manufacturer specifications). The numerical model is independently implemented; no SlicerHeart source code or mesh is bundled.

## References
- [SlicerHeart ValveClipDeviceSimulator](https://github.com/SlicerHeart/SlicerHeart/blob/master/ValveClipDeviceSimulator/ValveClipDevices/devices.py) (BSD-3-Clause)
- [Simulation of Delivery of Clip-based Therapies within Multimodality Images](https://pmc.ncbi.nlm.nih.gov/articles/PMC8492527/)
- [Advanced Steering Maneuvers](https://pmc.ncbi.nlm.nih.gov/articles/PMC11588182/)

## Limitations / next steps
Anatomy and TEE projection are schematic. Steering signs, curvature, dimensions, friction, straddle exposure and grasping behavior require validation by experienced operators and reference data. The push/pull model does not simulate contact, constraints or secondary motion. No clinical validation. A distribution license for this project has not yet been selected.
