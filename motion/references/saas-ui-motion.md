# SaaS/UI motion — product interface animation

An optional module inside `vizavi_motion`, not a separately installed skill. Apply it to product or interface demos and to the corresponding parts of the tutorial demo. Here "SaaS/UI motion" is a short name for staging an interface, not a claim that the SaaS business model dictates a strict art style.

## Origin and limits

Adapted from user-supplied archives `higgsfield-motion-saas.skill` and `higgsfield-motion.skill` (handed over 15.10.2026, read for this edition). This is not a claim of official Higgsfield authorship. The source's `techniques.md` names MahdiEdits tutorials "Top 3 Most Used SaaS Video Transitions", "Overlapping Keyframes" and "Overlapping Keyframes in 3D"; their public URLs are not confirmed. Measurement/review statuses stated in the archive belong to its author and were not independently verified here. Transfer principles only — not others' implementations, brand palette, project tastes, mandatory durations, BPM, engine or tool installs. The spatial-mode rules and the tutorial demo below were added from the user's current assignment.

## Action and result

For each episode pick a clear task: select an element, change a setting, drag a card, rearrange a panel, start a process or show a result. Show one plausible application with consistent data and states, not an unrelated decorative card under a new heading in every scene. Keep the cards/panels/buttons hierarchy and consistent radii, shadows and stroke widths. Emphasise few main controls per action (the source suggests 1–3 as a guide, not a universal quota). Don't present demo data as real properties or metrics of an existing service.

The cursor drives the action: hover → target reaction → press/grab → change → readable result. It must not fly randomly over a passive screen. Hit-testing uses the arrow tip/hotspot, not the sprite centre. Give a short readable hover before a click and a visible causal state change after. The cursor stays sharp and fully visible while pressing and doesn't cover the button label, the result or readable numbers.

Button and object states are causally linked: hover, pressed/dragging, processing, success/selected or another meaningful set. Don't show success before the process completes. A chart, percentage and any other indicator of one operation share one progress value. Don't present edited-down waiting as the product's real speed; mark it as shortened/demo when needed.

On drag, fix the grab point and the cursor–object offset: the card lifts and follows an arc, the drop zone highlights, on drop the card gently shrinks and settles into the slot. Follow/lag may convey weight and inertia but must not look like losing the grip: the main object stays controlled, lags or catches up for a reason, neighbours react after the event. Drop, snap and residual damping end in a stable clear layout. Don't apply the same spring to every layer.

Tune durations and amplitudes to the tempo, frame size and reading window. The source's `client-taste.md` has a preset: cursor travel 0.6–0.9 s along a small arc, a slight squash on click and recovery after, entering/exiting off-frame. It is a tuning example, not a universal norm; off-frame entry/exit is compatible with full visibility at the moment of the click. Don't copy numeric presets mechanically into every scene.

Show a few functional micro-reactions: target highlight, state change, a neighbouring card's response, a panel opening. They support the main point rather than compete with it. Motivate a cut to a detail by action; give text reading time. Tie individual expressive cuts, reveals and ends of moves to real music/SFX accents per the [motion and sound module](motion-and-sound.md), not to every beat.

When passing an object between scenes, match its screen position, size and state; leave no duplicate or ghost. A result emerges from the element that caused it; cards separate along soft arcs. In a morph change the real dimensions of the shape/layout; don't stretch the whole UI together with text and radii. Preserve the interface's identity when going from a flat view to a spatial one.

The camera helps the action: it can follow the caret, push in to a click, pull out for the result or orbit separated layers. A close-up lets you read a detail, a wide shot gives the app context. Choose a meaningful camera gesture; don't do all of these moves in every episode.

## One interface in 2D, 2.5D and 3D

| Mode | What must actually change |
|---|---|
| 2D + SaaS/UI | Flat panels, cards, buttons and content. Volume is not faked with random thickness; cursor action and state change remain the centre of meaning. |
| 2.5D + SaaS/UI | The same flat panels separated in depth. The camera reveals relative placement, perspective, occlusion and parallax. Panels get no real sides or extrusion. |
| 3D + SaaS/UI | Recognisable objects gain real geometric thickness, edges and side faces. Volume is confirmed by light, normals, shadows and a spatial orbit/fly-through, not just scale or a drop shadow. |

For the selected tutorial demo carry the same object IDs, compositional anchors, colours, content and operation result across the last three parts. The viewer should see the spatial model of one interface change. This is a condition of that demo, not a ban on changing the interface in another brief.

## Coordinates and reproducibility

Clearly separate world-space UI and screen-space overlay. If the cursor works on an object in the world, compute its screen point from the current projection of the anchor, accounting for camera, viewport, aspect ratio and window scale. If the cursor is entirely screen-space, test the target in the same screen space too. Never mix CSS pixels, video-frame coordinates and world units without conversion.

A screen label for a demo part keeps its position and styling while the camera moves. Labels on world-space objects may follow their projection; check margins, overlap, depth and leaving the camera. A volumetric panel must not accidentally hide a cursor that is an overlay by design, or cross mandatory text.

For reproducible video, animate the cursor, grab, states and delays on one controlled timeline. Real user input is not needed for playback. Compute states from time or a reproducible bake/replay, including seeking backwards; leave no dependency on the previous mouse event or the number of frames already played. Full functional QA of rapid repeated clicks, resize and reduced motion is needed only if you are building a live app; don't turn an ordinary video demo into interactive product development.

## Check

Check at speed and at seams: clarity of the action, grab accuracy, drop completion, sync of progress/states, identical interface identity where required, distinguishability of the three spatial modes, projection under camera motion and seeking, overlay legibility. Then check the final decoded export together with the sound. A cursor, `translateZ` or an extrusion parameter in the code does not prove the visual result.
