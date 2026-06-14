# Webgentools

A small collection of browser-based creative utilities for image conversion, looping video generation, pattern layout, and procedural texture creation. Each tool is a standalone HTML file with its own CSS and JavaScript, designed to run locally in a modern browser.

All tools are client-side: files are processed in the browser and are not uploaded to a server.

## Tools

| File | Tool | Purpose |
| --- | --- | --- |
| `batch-convert.html` | `BATCH//CONVERT` | Batch-normalize images to PNG with naming, resize, watermarking, and metadata wiping. |
| `loop-logo.html` | `LOGO//LOOP` | Animate a single logo or image into a looping video, GIF, and optional icon pack. |
| `loop-reel.html` | `LOOP//REEL` | Turn image sets into looping screensaver-style videos with drift, scatter, and grid motion modes. |
| `step-repeat.html` | `STEP//REPEAT` | Build print-ready repeated image layouts with seeded randomization. |
| `texture.html` | `TEX//TURE` | Generate seamless procedural textures and material maps as PNG files. |

## Quick Start

Open any `.html` file directly in a browser:

```text
batch-convert.html
loop-logo.html
loop-reel.html
step-repeat.html
texture.html
```

## Tool Details

### BATCH//CONVERT

Batch image conversion and normalization.

Features:
- Drag-and-drop multiple source images.
- Converts common image formats to PNG.
- Includes HEIC/HEIF decode support and a single-file HEIC diagnostic test.
- Custom output naming with prefix, start number, padding, and separator options.
- Resize modes with width/height controls and no-upscale protection.
- Optional watermark image with position grid, size, opacity, margin, and tiling.
- Optional file shuffle.
- Option to preserve transparent/background handling.
- Wipes metadata during conversion.
- Downloads converted PNG files from the browser.

Use it for:
- Preparing normalized image batches.
- Removing metadata before upload or delivery.
- Applying consistent filenames and watermarks.

### LOGO//LOOP

Animated logo and brand loop generator.

Features:
- Upload a single logo/image.
- Choose animation behavior, placement, size, and padding.
- Background modes: solid, gradient, radial, and grid.
- Effects: recolor, black-and-white, grading, vignette, CRT, grain, letterbox, and image overlay.
- Output formats: video and animated GIF.
- GIF-specific controls for width, frame rate, and color count.
- Video controls for resolution, FPS, and duration.
- Live preview with play/pause.
- Icon pack generation with transparent or solid background and square, rounded, or circle shapes.

Use it for:
- Social/video logo loops.
- Stream or reel intro graphics.
- Quick app/social icon exports from a source logo.

### LOOP//REEL

Photo screensaver video generator.

Features:
- Upload images individually or by folder.
- Optional library workflow for adding and clearing image sets.
- Preview playback and restart controls.
- Motion modes: Drift, Scatter, and Grid.
- Timing controls for duration, speed, FPS, and easing.
- Output resolution control.
- Look controls for image size, size variation, rotation, jitter, edge behavior, screen fill, border styles, shuffle, use-every-image, and shadow.
- Background modes including solid color, gradient, and blurred-image styles.
- Optional vignette and grain.
- Mode-specific controls:
  - Drift direction and path.
  - Scatter arrangements, entry styles, hold time, and max visible items.
  - Grid tile count, gap, pan intensity, sync mode, and grid lines.
- Browser-rendered video export.

Use it for:
- Ambient photo loops.
- Event screensavers.
- Reel backgrounds and simple montage videos.

### STEP//REPEAT

Pattern layout engine for repeated image compositions.

Features:
- Drag-and-drop multiple source images.
- Canvas width and height controls.
- Background color swatches and custom color picker.
- Layout mode and image order controls.
- Image size, columns, rows, horizontal/vertical gap, base rotation, and opacity.
- Jitter toggles for position, scale, rotation, opacity, and hue.
- Seeded randomization for reproducible layouts.
- Live canvas preview.
- PNG export.

Use it for:
- Sticker-sheet style layouts.
- Textile or print pattern experiments.
- Seeded randomized compositions.

### TEX//TURE

Seamless procedural texture and material-map generator.

Features:
- Pattern generators: fractal noise, cells/dots, stripes, grid/checkers, bricks/blocks, weave/fabric, wood/rings, scratches/dust.
- Custom/Mix mode with layer weights, blend modes, invert toggles, search/filter, active-only view, presets, solo, quick weights, expand/collapse, reset, randomize, mix contrast, mix bias, posterize, normalize, and domain warp.
- Tiling controls for both axes, horizontal, vertical, or none.
- Export resolutions from 64px to 4096px.
- Preview quality controls with preview sample readout.
- Resolution-linked detail controls.
- Domain transform controls: repeat, rotation, offset, mirroring, and global warp.
- Color ramps, two-color mode, brightness, contrast, transparency, and invert.
- Surface shaping: low/high clip, gamma, posterize, threshold, micro detail, and detail scale.
- Output map types: color/alpha, height, normal, roughness, and ambient occlusion mask.
- Seeded generation for repeatable outputs.
- PNG export.

Use it for:
- Tileable procedural texture masks.
- Quick material-map generation.
- Pattern and surface experiments before moving into a heavier material tool.

## Browser Requirements

Recommended:
- Latest Chrome, Edge, or another Chromium-based browser.
- Modern Firefox should work for most image/canvas workflows.

Notes:
- Video export depends on browser media APIs and codec support.
- HEIC/HEIF decoding support may vary by browser and included decoder behavior.
- Large 4K exports and long videos can be CPU/RAM intensive because everything runs locally.

## Privacy

The tools are designed to process assets locally in the browser:
- No account is required.
- No backend server is required.
- Files are not intentionally uploaded anywhere.
- Downloads are generated from browser memory using Canvas, Blob, and Media APIs.

## Development Notes

This repo is intentionally simple:
- No build step.
- No package manager required.
- Each tool is self-contained in one HTML file.
- Shared visual language is repeated across files rather than imported from a framework.
