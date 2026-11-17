# Motion, optics, typography and sound

Apply according to the chosen storyboard. The goal is the quality of core mechanic 1, not demonstrating every technique at once.

## Camera and depth

Separate path, speed, orientation, target, FOV and focus. Design a long coherent trajectory with speed waves; don't chain identical ease-in-outs with zero velocity at every accent. At seams check position, direction, screen speed and acceleration. In the readable phase of an active scene a big move settles into a calm arc/drift. Following the hero is compatible with strong parallax of the environment. A meaningful edit cut does not require continuous world coordinates between different locations.

Fore-, mid- and background differ in scale, relative motion, occlusion and perspective. Protect silhouettes and text from accidental overlap. Anchor a label next to a moving 3D object to the projection of its anchor; keep frame margins with no jitter or lag.

## Optics and material

- Motion blur reflects relative on-screen motion during the exposure. A tracked sharp hero may have a blurred background. Sub-frame sampling or a suitable renderer are means, not proof of the effect. Blur weakens on deceleration.
- DOF isolates the chosen depth. When approaching, focus follows the meaningful detail without random defocus. Near and far layers may go soft; text and hero stay recognisable. In flat UI don't create artificial illegibility just to tick a box.
- Radial/zoom blur is a separate stylised accent suited to depth or fast cards. Don't pass it off as depth of field or temporal blur. Don't apply maximum blur to the whole video.
- Form reads through geometry, light, normals, thickness, contact shadow and occlusion. Highlights, grain and particles don't fix wrong construction. Texture and shadow must follow the object and the light.

## Typography and rhythm

Choose an expressive available typeface or a consistent pair; check the specific glyphs (including Cyrillic or any other script needed), weights, line breaks and whether the font file may be used. If external fonts are prohibited, use allowed system fonts or custom geometry. First design a readable final layout, then the action of letters/words: assembly, width change, masks, spatial relationships, interaction with an object. Every effect must have a semantic role.

Combine anticipation, action, contact, reaction and decay with different masses and curves. One main accent allows coordinated secondary layers. If everything competes for attention, vary phase, scale, depth and contrast. Don't rescue the pacing by deleting mandatory elements or speeding up to illegibility. Avoid repetitive flashes as a substitute for energy.

## Music and sound design

Unless the user set silent mode, music and SFX are part of the staging from the start. Choose how to obtain them by allowed means and the task: musical character and the result matter, not a specific service or synthesiser. Music needs a fitting motif/groove, development, contrast and resolution; a set of whooshes and hits does not replace a composition. Tie SFX to motion, contact, material and transitions, not randomly.

Optional external services (e.g. VidIQ for voice or music) may be used only when already available and allowed for the task. Don't assume they are free, don't make them a universal dependency, and don't pick a voice on the user's behalf.

Drive sound and picture from the same events. After a speed ramp recompute the actual moment of the accent; don't unintentionally change the whole music tempo/pitch. Listen to the full mix and the needed stems; check balance, clipping, clicks, sync and the tail. Technical metrics don't prove musical quality. If audio was not created or not listened to, state those statuses explicitly.

### Editing to expressive accents

Account for musical points already when planning the sound and animation: a highlighted note, a hit, a change of phrase or harmony, a pause or the return of the groove can support a cut, a scene reveal, a change of angle, a contact or the end of a move. This is a periodic meaningful device, not a requirement to cut on every beat. A piano note is one possible example of an accent, not a required instrument or genre.

After choosing/creating the **actual audio track**, mark the timecodes of noticeable accents and the matching visual events. For the chosen points record the perceived peak/onset of the accent, the target visual action and the nearest suitable frame: `frame / fps`. Account for the real audio start/offset and edit shifts. The same BPM, a computed grid or the start of an SFX file are not enough: the musical peak, the attack and the visual climax can sit elsewhere. Verify by ear and in motion at frame accuracy, not from a waveform alone.

If a sync point doesn't work, gently adjust the shot length, trajectory, reveal/landing timing or the arrangement within the brief. Don't create unnatural speed or hurt the tempo/intelligibility of speech for the grid. Meaningful story events, reading time, voice and an explicit no-music brief outrank mechanical beat-matching; in silent mode musical sync does not apply.

Coordinate SFX with the musical gesture: a sound can support, complement or leave room for an accent. Don't layer the same whoosh on every transition or double every musical hit with an effect. After replacing/trimming the track or a speed ramp, update the accent map. Check the chosen sync points and the final mix together with the video; don't claim perfect sync without that check.
