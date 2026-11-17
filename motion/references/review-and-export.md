# Iteration, review and export

This is the working check of mechanic 3, not a quality certificate based on the existence of code.

## After the first build

The first result is an internal unfinished draft. Do a full viewing at normal speed, then a targeted pass over each scene and seam. With sound, listen to the full mix and the necessary individual stems. Record significant notes as: **interval → observation → cause → concrete fix → re-check**. Don't fake rework to inflate the number of iterations; if no defects are found, record exactly what was checked.

Check:

- does the idea and causal thread read; is the hero recognisable; is there development instead of dull hanging;
- do camera, shot size, perspective and layers direct attention; are speeds and seams smooth;
- does typography perform an action; are mandatory words readable without a pause;
- are form, light, shadows, material, identity and contact preserved; no artifacts, accidental crops or layer conflicts;
- do blur and focus match motion/depth without hiding what matters;
- do music and SFX support style, rhythm and events; no desync, clicks or abrupt cut-offs;
- are format, duration, fps, silent/offline and other explicit requirements met.

Fix significant causes, review the changed places together with neighbouring phases, then the whole video again. After simplifying, compare with the brief: "cleaner" is not acceptable if required characters, text, environment or actions disappeared. Finish when the mandatory items are done and verified, significant defects are fixed and what remains are taste alternatives beyond the necessary rework.

## Implementation and the default MP4

When the task can be solved well with plain HTML/CSS/JavaScript, SVG/Canvas and your own controlled timeline, prefer that simple path. Don't require Remotion, Hyperframes or another framework up front and don't install dependencies by template. This is a preference, not a ban: Three.js, Remotion, Lottie, audio libraries and other suitable tools are allowed when genuinely needed. Choose by result quality, required capabilities, the available environment and the cost of complexity; don't promise vanilla is always better.

The Web Audio API is a built-in browser API, not a synonym for the audio.js library. No particular music generator or synthesiser is fixed: use a suitable allowed method, and audio libraries when they are genuinely needed. Don't rebuild an existing project or a stack the user explicitly chose for the sake of this preference.

Standard deliverable: a finished MP4 with video **1920×1080, constant 60 fps, H.264 and compatible yuv420p**, with **AAC** audio unless the user requested silence. Keep HTML/JS and other editable sources as an additional result. 4K on request; explicit size, fps, duration, codec or no-audio in the brief take priority. Don't call a file 4K/60 fps or a finished MP4 if the actual file differs.

Reliable export path without a mandatory framework:

1. Fix a controlled time and frame grid. Deterministically render **all** frames at time `i / fps`, including complex phases and transitions — for example with headless Chromium/Playwright screenshots or canvas capture driven by the timeline. Check that the sequence is complete and ordered. If another engine is used, ensure the same reproducibility instead of recording random real-time playback with dropped frames.
2. Prepare and mix music, SFX and speech (when present) into a real exportable track. Account for start, offsets, accents and endings on the shared timeline. A real-time Web Audio preview by itself does not guarantee sound in the MP4: produce a usable audio file/buffer via OfflineAudioContext, a Python/numpy synth, recording or an equivalent reliable method, and check its actual content.
3. Assemble the frames and the full audio mix into an MP4 with FFmpeg or an equivalent reliable pipeline. Keep the set frame rate and timing. When muxing, map the intended video and audio streams explicitly: don't lose speech, music or SFX and don't replace the full mix with a single effect. In silent mode don't add audio on your own. A typical command:

   ```
   ffmpeg -framerate 60 -i frames/%05d.png -i mix.wav \
     -map 0:v -map 1:a -c:v libx264 -preset veryfast -crf 18 \
     -pix_fmt yuv420p -r 60 -c:a aac -b:a 192k -movflags +faststart out.mp4
   ```

   Use a slower preset only when best quality is requested.
4. Align the start and the final tails with the brief before muxing. Don't cut the last scene, speech or the ending of the music to mechanically match durations, and don't extend the video with a stray audio tail. Don't use `-shortest` blindly if the shorter stream would cut off the intended ending; instead trim or pad the audio to the exact video duration.
5. Check the **finished decoded MP4** (e.g. `ffprobe` plus decoding): the real codec/pixel format, resolution, constant fps and timestamps, frame count and exact duration, AAC and presence of the intended audio, A/V sync, start, end and scene boundaries. Watch and listen to the final mix together with the video; the source preview does not prove a successful audio export.

If the environment genuinely does not allow rendering, encoding/FFmpeg or an equivalent, or delivering the file, report the specific blocker, the completed parts and the actual format. Keep and hand over the sources and available playback/export instructions; don't present HTML as the finished video. This is an exception for confirmed unavailability, not a routine shortcut instead of the mandatory MP4. Don't automatically install an unavailable framework to get around the limit.

## Check the delivered result

After encoding, open and decode the final export and check its motion and sound, not only the HTML or the source PNG/WAV. Check start/end, adjacent frames before and after every scene boundary, readable holds and the fastest phases. A contact sheet helps judge compositions, a dense frame sequence a specific seam, full playback the rhythm and smoothness, listening the sound. These kinds of evidence are not interchangeable.

If musical sync was used, compare the chosen transitions/actions with the timecodes of perceived accents of the **real track** and with frames of the decoded export, including the audio offset after mux. Watch and listen to them at speed, then check the full mix together with the video: no drift, no annoying repetition of SFX, no loss of meaning/reading/speech for the sake of the beat. Matching numeric markers is not proof of perfect sync; if viewing/listening is unavailable, this item stays unverified.

At exactly 20 s and 60 fps, 1200 frames are expected on the grid 0..1199/60; the endpoint `renderAt(20)` is not an additional video frame. 20 seconds here is a counting example, not a fixed duration for all videos. The 60 fps default changes with an explicit brief. Distinguish the presence of an audio stream from sound quality: a silent stream never gets a PASS as a scored result, and an AAC stream alone doesn't confirm audible music/speech and their balance.

For a controlled timeline, re-render a frame after a cold seek, after seeking backwards and after jumping from elsewhere — it must be identical. Simulations and cumulative effects need an analytic state, a bake or a reproducible replay; a single random seed is not enough. Compare source and output by hash if a version must be preserved. Don't call a previous weak result "without the skill" if the skill was applied.

## Honest statuses

Distinguish: **implemented**, **verified by running**, **seen in frames**, **verified in motion**, **listened to**. Nothing unverified gets a PASS from parameters or general impression. If a tool is unavailable, name the specific check not performed and the reason; show the available artifact with the matching label, without presenting it as having passed artistic acceptance. Never invent viewing, running or skill effectiveness.

If the required quality is genuinely impossible in the available conditions, report the exact blocker and the finished parts. Don't hide it after declaring readiness. If the outcome of an external action is uncertain, find out first; don't duplicate the write. Don't ask for new permission for ordinary reversible work that is already allowed.

Don't use repeated strobing as a substitute for energy. Check risky brightness changes in the output; reduced-motion support and absence of errors don't prove formal flash safety. Don't claim compliance with a standard without the corresponding analysis.
