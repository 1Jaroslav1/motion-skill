# Ready-made 3D models and bringing them into a scene

For a personal task you may find and download suitable ready-made free models within the current request. Prefer GLB/glTF when it suits the chosen renderer and export. Check the specific object and its terms; "free" does not mean every right. Don't impose a blanket download ban because of hypothetical future commercial use or source distribution, and don't forbid the user from showing devices in a video.

Use a genuinely available source and an ordinary permitted download. Don't bypass access restrictions and don't present missing access as an obtained model. Don't turn the search into self-registration or installing integrations. Choose from the [3D source registry](3d-sources.md); don't invent unknown services, terms or prices.

## Before the scene

1. Check the exact model/variant, format and completeness: mesh, UVs, textures, materials, rig/animations and external dependencies. Open/render the actual file, not just the page preview.
2. Normalise units and scale, axes, position, orientation, origin/pivot. Check normals, edges, thickness, topology, transparency, roughness/metalness, texture colour space and renderer compatibility. Don't substitute WebGPU/TSL material properties with those of a plain WebGL material (or vice versa).
3. Check that textures are available after loading, their sizes, paths and alpha correctness. Make sure the model doesn't fall apart at the chosen shot size. Reduce heavy meshes/textures while keeping the silhouette and needed detail; check the real render speed and export path.
4. Set light, environment, exposure, camera, shadows and contact for the chosen material. Plastic, metal and glass must differ in surface behaviour. A bright highlight and a generic gradient don't fix wrong form.
5. For a laptop, check the separate lid/base and the hinge axis. Opening is a relative rotation of the lid around the hinge, not rotating the whole body. Check the closed/open states, the screen, the initial orientation and that the underside isn't accidentally shown.

Required hiding/reveals, labels and the camera serve one spatial scene. On a close pass keep focus on the hero and the correct scale; don't let surfaces cross the near plane. When replacing a model, re-check orientation, pivot, light, contact and animation.

## Short notes at the end of the result

List the sites/pages and specific files actually used: author/title, link, format, stated licence or terms with the check date, required attribution and modifications. Rights to code, model, textures, font and music may differ. If the needed scope of use is genuinely limited, state that precisely and pick an allowed alternative; don't turn an ordinary personal download into a legal barrier. Never call a right to view/download a right to resell or redistribute the asset.
