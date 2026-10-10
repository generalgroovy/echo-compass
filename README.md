# Echo Compass

Listen to a sound and find its position between your left and right audio channels.

## Run and play

Run `python -m http.server 8000`, then open http://localhost:8000. No build or dependencies. Press **Listen**, wait for the tone to finish, then choose its position. A completed round keeps the correct position sequence visible and offers **Hear answer** and **Next sound**. After a mismatch, **Hear my choice** plays your guessed positions with the same tone, so you can compare directly instead of reading only a correction. Replays are unlimited.

**Practice settings** offers 3, 5 or 9 stereo positions, and one-, two- or three-sound sequences. Choose sequence positions in order. **Undo last choice** recovers an incomplete answer. Completed answers cannot be changed; they can be replayed for comparison. **Show the answer while exploring** exposes the positions and does not count the answer in practice totals. Changing settings begins a new round while preserving the current session totals.

Stop cancels unfinished playback; an unfinished initial listen cannot be answered. Hiding the tab stops audio. No audio starts on load or restore. Settings save locally when possible; rounds and session totals reset on reload.

## Verify and interpret

Run `npm test` with Node 18+. Model tests cover symmetric positions, seeded sequences, unheard/completed answer guards, order-sensitive scoring, partial Undo, exploration score exclusion invalid settings, exact answer/guess replay order and incomplete-comparison guards.

The browser's stereo panner controls left/right balance. The compact left–right strip shows stereo balance, not physical angles or distance. Answer text remains available to screen readers during and after comparison playback. Headphones, browser output, volume and hearing affect results. This is stereo listening practice, not a hearing assessment or calibrated spatial model. It uses no microphone. Browser audio scheduling and actual listening require separate acceptance beyond model tests.

## Originality and possible depth

Original implementation inspired by Speaker Simulator's spatial experiments. This is a listening game rather than a virtual-room editor. Future possibilities, not shipped: adaptive challenge formats, timbre distractors, custom audio and user-controlled difficulty progression.
