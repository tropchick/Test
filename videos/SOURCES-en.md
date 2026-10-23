# What if water started falling upwards? — 63-second film

Original stylized town geometry was created procedurally in Blender. The approved eight-second scene is preserved in `/workspace/water-up-preview/`. `assets/town.glb` contains its exported geometry. `film.js` contains the full camera, character, water, bird and lighting timeline. `plan_people.py` generates pedestrian trajectories and `path-validation.json` records the geometric checks. All visible animation is original code; no external AI video or paid Runway generation was used.

## Changes following the preview review

- People use paths around the fountain, benches, trees, cafe furniture and buildings.
- The walking area ends before the railing. Escape routes lead to three open exits at the front of the square.
- The main water lift from the glass takes 7.5 seconds instead of 1.9 seconds.
- All 14 pedestrians were checked against the obstacle map at all 1512 frames. All reach an exit.
- The town, slow glass shot, fountain reversal, rising river, suspended ocean, quiet final drop and returning water form a continuous 63-second film.

## Sound sources

There is no music and no narrator. The edit layers the following CC0 field recordings and foley with original non-musical wind/water textures and a final impact. Source-page copies for newly downloaded recordings are retained under `sources/`; the earlier source pages are retained in `/workspace/water-up-preview/sources/`.

- **Fountain**, Sandermotions: https://freesound.org/people/Sandermotions/sounds/275593/
- **Sparrows.wav**, JKata: https://freesound.org/people/JKata/sounds/626174/
- **Cafe' Atmosphere.wav**, Nautzera: https://freesound.org/people/Nautzera/sounds/478115/ — explicitly described as having no music.
- **Man Gasping**, ranman22: https://freesound.org/people/ranman22/sounds/677888/
- **Strong Wind**, florianreichelt: https://freesound.org/people/florianreichelt/sounds/459981/
- **RUNNING 1.wav**, vmgraw: https://freesound.org/people/vmgraw/sounds/257700/
- **Crowd in panic**, IENBA: https://freesound.org/people/IENBA/sounds/491405/ — performed by animation and video-game students during a sound-design workshop.

All seven source pages identify their license as Creative Commons Zero. Public high-quality preview audio was downloaded from the Freesound CDN. `mix_full_audio.py` creates the 63-second stereo sound edit. `encode_english.py` adds the English hook and three brief English story captions, then exports H.264/AAC with a streaming-friendly MP4 header.

## Output

- 720×1280, vertical 9:16
- 24 original rendered frames per second, no motion interpolation
- 63 seconds total, including the intentional final cut to black
- Stereo sound at 48 kHz; no music

Applied guidance: Blender Cameras and Blender Animation modules from https://github.com/CheshireJCat/blender/tree/main/skills/create-3d-model/references/modules and the frame-driven animation practices in https://github.com/remotion-dev/skills/blob/main/skills/remotion-markup/3d.md . The production renderer uses Three.js directly; it is not a Remotion project.
