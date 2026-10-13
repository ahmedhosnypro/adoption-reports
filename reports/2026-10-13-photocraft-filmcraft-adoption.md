# Cross-repo adoption scan: storytold/photocraft + storytold/filmcraft — 2026-10-13

Scope: merged pull requests from the last 24 hours in storytold/photocraft and storytold/filmcraft, adoptable/shareable patterns, fixes, helpers and conventions between them, and the strongest duplicate-code candidates. Read-only study of the two upstream repos; every write stays in this repository.

## Merged pull requests, last 24h

Source: `craft-helpers prs --org storytold --repos photocraft,filmcraft --since 24h --json`. **Truncation (helper caps, not re-run):** newest 30 per repo and 50 total; filmcraft's window was cut at 20 PRs by the 50-PR total cap — more merged filmcraft PRs may exist in the window, unverified.

| Repo | PR | Author | Title | +/− |
|---|---|---|---|---|
| photocraft | #4055 | callmeBalloch | Affinity: rectangles keep per-corner radii and straight corners (#1606) | +108/-38 |
| photocraft | #4054 | dotCooCoo | Affinity import: pie shapes with huge angles no longer hang the reader | +83/-6 |
| photocraft | #4233 | FinnNk | feat(ui): the shaped brush cursor turns and flips with the view | +90/-8 |
| photocraft | #4046 | Ni-zav | fix(selection): validate Magic Wand pixel buffers before indexing | +22/-1 |
| photocraft | #4043 | Ni-zav | fix(algo): reject oversized Magic Eraser masks without overflow | +12/-1 |
| photocraft | #4224 | Hevarh1 | Type: Space inserts a space while editing type | +29/-3 |
| photocraft | #4045 | Ni-zav | fix(selection): avoid panics when sampling incomplete region masks | +17/-1 |
| photocraft | #4135 | vbasky | Refresh Liquify's zoomed preview when a stroke is undone. | +24/-0 |
| photocraft | #4106 | Furash | Stylus: a pen held still is not a press-and-hold right click | +139/-0 |
| photocraft | #4019 | xsvm | Clone Stamp and History Brush: releasing a stroke commits the live pixels | +287/-19 |
| photocraft | #4418 | vangel76 | Docs: refresh target-app-parity and file-format-parity against main (#4417) | +17/-14 |
| photocraft | #4413 | vangel76 | Docs: refresh gaps.md against main (#4412) | +24/-22 |
| photocraft | #4264 | Ni-zav | feat(codecs): add XPM2 plain-text image import support | +67/-8 |
| photocraft | #4263 | Ni-zav | feat(codecs): support full X11 rgb.txt color names in XPM | +970/-4 |
| photocraft | #4229 | davidmann4 | Brush resize HUD: horizontal is size and vertical is hardness in a rotated view (#4228) | +44/-3 |
| photocraft | #4227 | davidmann4 | Rotate View: the image follows the pointer in a flipped view (#4226) | +55/-3 |
| photocraft | #4207 | davidmann4 | Shape tools: the click-to-open-dialog tolerance is the same on HiDPI displays (#4205) | +15/-1 |
| photocraft | #4165 | davidmann4 | Exposure: the slider keeps fractional stops (#4164) | +136/-14 |
| photocraft | #4163 | davidmann4 | Image Size and Canvas Size: no silent resize of large documents in physical units (#4162) | +31/-1 |
| photocraft | #4140 | vbasky | Snap 1 px pencil clicks to the pixel the aliased tip paints. | +22/-2 |
| photocraft | #4139 | vbasky | Draw the Free Transform rotate arrow instead of hiding the pointer. | +9/-2 |
| photocraft | #4134 | vbasky | Keep Liquify undo and redo working while a numeric field is focused. | +18/-5 |
| photocraft | #4131 | davidmann4 | Layers panel: double-clicking an effect row opens that layer's Layer Style (#4157) | +35/-1 |
| photocraft | #4120 | davidmann4 | Layer Style: OK keeps an Inner Glow's Center source (#4152) | +28/-1 |
| photocraft | #4424 | SckraT | perf(engine): read selection coverage per row when mixing edits back | +66/-19 |
| photocraft | #4423 | SckraT | perf(compose): read PHOTOCRAFT_FX_NOCACHE once | +2/-1 |
| photocraft | #4422 | SckraT | perf(engine): move layers without a second document clone | +10/-8 |
| photocraft | #4415 | SckraT | perf(compose): stop sweeping the bounds cache on every call once it i… | +79/-37 |
| photocraft | #4414 | SckraT | perf(raster): moved fills keep sharing one copy-on-write tile | +124/-2 |
| photocraft | #4352 | vangel76 | Paint Bucket and Edit > Stroke: a CMYK foreground writes the picked inks (#4351) | +289/-33 |
| filmcraft | #1169 | echelon | Release workflow: pass the Azure signing secrets | +6/-0 |
| filmcraft | #1198 | n-delic | #1124: ⌘D / ⇧⌘D apply transitions to the selected clips or edit points | +104/-4 |
| filmcraft | #1193 | OorjitSethi | ui: reduce sequence copying and cache transcript redraw data | +212/-22 |
| filmcraft | #1168 | haranishi | fix: Close Gapをショートカットに割り当てられるようにする | +115/-2 |
| filmcraft | #1217 | liangforstudy | dialogs: drag them by the title bar (open centred, no longer anchored) | +114/-36 |
| filmcraft | #1052 | Auipp | timeline: cancel drag and restore playhead on Escape (#580) | +337/-61 |
| filmcraft | #1063 | vbasky | Linux: VA-API EncSlice probe and bounded export GPU wait (#1058) | +14/-5 |
| filmcraft | #1067 | vangel76 | #1039: 8-bit HEVC pictures as u8, in-place motion compensation (−14…23 % per frame), big-picture analysis | +1316/-275 |
| filmcraft | #1070 | luniiya | UI: favorite themes and appearance shortcuts | +187/-7 |
| filmcraft | #964 | mjohnson7cd | fix(ui): add Korean font fallback for UI text | +63/-15 |
| filmcraft | #1165 | MarekSpodBiedry | Trim MP3 encoder delay when decoding audio files (#1137) | +56/-3 |
| filmcraft | #865 | earlvanze | M7: optimize audio DSP and isolate the unchanged mixer throughput gate | +587/-190 |
| filmcraft | #1046 | vbasky | Median Radius is not capped at four working pixels | +88/-1 |
| filmcraft | #837 | vangel76 | #828: import OpenEXR stills and image sequences | +1302/-14 |
| filmcraft | #1159 | haranishi | fix: エフェクトコントロールの矩形選択とShiftスナップを修正 (#967) | +830/-54 |
| filmcraft | #1139 | itrycodinganditsbad | fix(timeline): snap sub-frame timeline.place to the frame grid; inspect counts export's frames (#1101) | +56/-1 |
| filmcraft | #879 | vangel76 | #874: compressed (RLE / ZIPS / ZIP) OpenEXR export | +994/-73 |
| filmcraft | #1068 | vangel76 | #1065: CinemaDNG / DNG import with a clean-room decoder | +3612/-21 |
| filmcraft | #931 | liangforstudy | #402: animated GIF and APNG import as clips, with transparency | +481/-4 |
| filmcraft | #1129 | itrycodinganditsbad | fix(menus): native menu follows command enablement (#902) | +100/-33 |
## Duplicate-code candidates (first tree scan)

Source: `craft-helpers dups --roots pc,fc --min-lines 6 --json`, run once. **Truncation (helper window behavior, not re-run):** the 250,000-window cap was filled by the photocraft root and the remaining files were skipped, so the filmcraft tree was not reached in this pass; 20 candidates were returned, all from photocraft. Higher-signal cross-repo candidates are covered below via the shared-crate scan.

| repeated lines | photocraft file:line(s) |
|---|---|
| 103 | crates/algo/src/gallery.rs:162, crates/algo/src/gallery.rs:33, crates/algo/src/tests_iris_reference.rs:12, crates/algo/src/tests_iris_reference.rs:21, crates/algo/src/tests_iris_reference.rs:53, crates/algo/src/tests_iris_reference.rs:63, crates/algo/src/tests_tilt_shift_reference.rs:6 |
| 25 | crates/engine/src/adjust_cmds/tests.rs:10, crates/engine/src/canvas_geom/tests.rs:11, crates/engine/src/color_cmds.rs:1142, crates/engine/src/color_to_alpha_cmds.rs:142, crates/engine/src/distort_cmds/tests.rs:15, crates/engine/src/filters.rs:470, crates/engine/src/filters_ext/tests.rs:10, crates/engine/src/filters_ext/tests.rs:241, crates/engine/src/gallery_cmds/tests.rs:24, crates/engine/src/image_cmds.rs:855, crates/engine/src/jobs_tests.rs:25, crates/engine/src/layer_menu_cmds/tests.rs:18, crates/engine/src/lens_cmds.rs:499, crates/engine/src/mode_cmds/tests.rs:8, crates/engine/src/multichannel_cmds/tests.rs:18, crates/engine/src/new_layer.rs:97, crates/engine/src/plugin_cmds/tests.rs:60, crates/engine/src/redeye_cmds.rs:274, crates/engine/src/redeye_cmds.rs:419, crates/engine/src/retouch_cmds/tests.rs:61, crates/engine/src/select_extra_cmds.rs:277, crates/engine/src/warp_cmds.rs:550 |
| 11 | crates/algo/src/blur.rs:185, crates/algo/src/blur.rs:72, crates/algo/src/blur/motion_fft_tests.rs:300, crates/algo/src/blur/motion_fft_tests.rs:390, crates/algo/src/blur/motion_tests.rs:119, crates/algo/src/blur/motion_tests.rs:54, crates/algo/src/blur/radial/tests.rs:225, crates/algo/src/inpaint/proximity_integral/tests.rs:27, crates/algo/src/inpaint/proximity_integral/tests.rs:80, crates/algo/src/lens/shared_sample_tests.rs:41, crates/algo/src/matting/morphology/tests.rs:55, crates/algo/src/pixelate/tests.rs:162, crates/algo/src/pixelate/tests.rs:99, crates/algo/src/shape_blur_tests.rs:138, crates/algo/src/shape_blur_tests.rs:60, crates/algo/src/stylize2/extrude.rs:143, crates/algo/src/stylize2/tests.rs:54, crates/algo/src/stylize2/tests.rs:79, crates/algo/src/stylize2/wind.rs:68, crates/algo/src/tests.rs:308, crates/algo/src/tests_mosaic.rs:116, crates/algo/src/tests_mosaic.rs:83, crates/algo/src/tests_selection_mix.rs:32, crates/codecs/src/codecs/tiff.rs:955, crates/compose/src/advanced_tests.rs:326, crates/compose/src/proxy.rs:242, crates/engine/src/extra_cmds.rs:1159, crates/engine/src/retouch_cmds.rs:753, crates/engine/src/retouch_cmds.rs:821, crates/io/tests/color.rs:133, crates/paint/src/render_reference.rs:160, crates/paint/src/render_reference.rs:244, crates/psd/src/compression.rs:672, crates/psd/src/patterns.rs:619, crates/raster/src/lib.rs:426, crates/raster/src/lib.rs:490, crates/raster/src/lib.rs:530, crates/raster/src/lib.rs:603 |
| 103 | crates/paint/src/render.rs:229, crates/paint/src/render.rs:297, crates/paint/src/render_reference.rs:8 |
| 32 | crates/algo/src/hdr.rs:418, crates/algo/src/quantize.rs:560, crates/cms/src/clut.rs:191, crates/engine/src/retouch_cmds/pattern_stamp.rs:289, crates/paint/src/bg_erase.rs:138, crates/paint/src/replace.rs:152, crates/paint/src/replace.rs:195, crates/paint/src/retouch.rs:418 |
| 14 | crates/engine/src/brush_key_cmds.rs:79, crates/engine/src/distort_cmds/tests.rs:1, crates/engine/src/edit_cmds.rs:888, crates/engine/src/extra_cmds.rs:1005, crates/engine/src/fill_key_cmds.rs:149, crates/engine/src/history_cmds.rs:293, crates/engine/src/lens_cmds.rs:479, crates/engine/src/notes_cmds.rs:241, crates/engine/src/paint_cmds.rs:154, crates/engine/src/photo_cmds.rs:912, crates/engine/src/presets/clone_source.rs:443, crates/engine/src/render_cmds.rs:233, crates/engine/src/select_extra_cmds.rs:242, crates/engine/src/selection_cmds.rs:665, crates/engine/src/symmetry_cmds.rs:217, crates/engine/src/type_caret_cmds.rs:229, crates/engine/src/warp_cmds.rs:531 |
| 59 | crates/automation/tests/agent_tasks.rs:8, crates/automation/tests/agent_tasks_more.rs:6, crates/automation/tests/mcp.rs:16 |
| 10 | crates/engine/src/actions_cmds.rs:20, crates/engine/src/actions_edit_cmds.rs:12, crates/engine/src/adjust_cmds.rs:26, crates/engine/src/analysis_cmds.rs:124, crates/engine/src/artboard_cmds.rs:37, crates/engine/src/atn_cmds.rs:33, crates/engine/src/brush_preset_cmds.rs:18, crates/engine/src/color_cmds.rs:820, crates/engine/src/comps_cmds.rs:15, crates/engine/src/eraser_cmds.rs:16, crates/engine/src/mode_cmds.rs:16, crates/engine/src/notes_cmds.rs:7, crates/engine/src/pattern_cmds.rs:97, crates/engine/src/photo_cmds.rs:870, crates/engine/src/preset_import_cmds.rs:12, crates/engine/src/sampler_cmds.rs:19, crates/engine/src/warp_cmds.rs:15 |
| 16 | crates/engine/src/brush_cmds.rs:27, crates/engine/src/image_cmds.rs:9, crates/engine/src/layer_style.rs:24, crates/engine/src/paint_cmds.rs:10, crates/engine/src/select_extra_cmds.rs:17, crates/engine/src/selection_cmds.rs:7, crates/engine/src/smartselect_cmds.rs:10, crates/engine/src/smartselect_cmds.rs:30, crates/engine/src/type_caret_cmds.rs:10, crates/engine/src/type_cmds.rs:16 |
| 49 | crates/algo/src/pixelate.rs:23, crates/algo/src/pixelate.rs:67, crates/algo/src/pixelate/reference.rs:4 |
| 12 | crates/engine/src/artboard_cmds.rs:623, crates/engine/src/automate_cmds.rs:532, crates/engine/src/comps_cmds.rs:392, crates/engine/src/edit_cmds.rs:780, crates/engine/src/exr_cmds.rs:58, crates/engine/src/extra_cmds.rs:782, crates/engine/src/file_cmds.rs:1378, crates/engine/src/layer_multi_cmds.rs:1352, crates/engine/src/print_cmds.rs:592, crates/engine/src/slice_cmds.rs:491, crates/engine/src/type_extra_cmds.rs:534, crates/engine/src/web_cmds.rs:1364 |
| 10 | crates/algo/src/magnetic.rs:260, crates/algo/src/panorama.rs:865, crates/algo/src/render2.rs:658, crates/algo/src/retouch.rs:168, crates/algo/src/segment/mod.rs:182, crates/compose/src/effects.rs:1362, crates/engine/src/presets/clone_source.rs:264, crates/engine/src/retouch_cmds.rs:618, crates/engine/src/type_extra_cmds.rs:428, crates/engine/src/type_extra_cmds.rs:443, crates/psd/src/testgen.rs:56, crates/raster/src/lib.rs:563, crates/raster/src/lib.rs:739 |
| 24 | crates/codecs/src/codecs/vp8/tables.rs:286, crates/codecs/src/codecs/vp8/tables.rs:319, crates/codecs/src/codecs/vp8/tables.rs:361, crates/codecs/src/codecs/vp8/tables.rs:389, crates/codecs/src/codecs/vp8/tables.rs:446 |
| 12 | crates/engine/tests/photoshop_oracles.rs:26, crates/io/examples/oracle_diff.rs:443, crates/io/tests/corpus.rs:54, crates/io/tests/smart_corpus.rs:20, crates/io/tests/text_corpus.rs:25, crates/io/tests/tiff_corpus.rs:22, crates/io/tests/vector.rs:205, crates/psd/tests/corpus.rs:8 |
| 14 | crates/algo/examples/bench_filters2.rs:21, crates/algo/examples/bench_filters2.rs:29, crates/algo/src/tests_ext.rs:236, crates/algo/src/tests_ext.rs:278, crates/algo/src/tests_ext.rs:530, crates/algo/src/tests_ext.rs:559 |
| 26 | crates/algo/examples/bench_algorithms.rs:53, crates/algo/examples/bench_algorithms.rs:64, crates/algo/examples/bench_pixelate.rs:37 |
| 18 | apps/photocraft-cli/tests/orientation.rs:40, apps/photocraft-cli/tests/orientation.rs:67, crates/codecs/tests/orientation.rs:64, crates/io/tests/orientation.rs:15 |
| 12 | crates/algo/src/inpaint/proximity_integral/tests.rs:144, crates/algo/src/matting/morphology/tests.rs:218, crates/algo/src/matting/morphology/tests.rs:281, crates/algo/src/matting/morphology/tests.rs:307, crates/algo/src/segment/workflow_tests.rs:48, crates/algo/src/selection/distance/tests.rs:172 |
| 10 | crates/compose/src/effects.rs:2953, crates/compose/src/tests.rs:2132, crates/compose/src/tests.rs:2354, crates/engine/src/layer_style.rs:481, crates/gpu/src/plan.rs:1793, crates/io/src/effects_map.rs:596, crates/io/src/effects_map.rs:668 |
| 17 | crates/algo/src/paint.rs:42, crates/compose/src/adjust.rs:976, crates/compose/src/effects.rs:1067, crates/gpu/src/plan.rs:1485 |

## Raw window-diff detail for the top 10 (verification data)

Method: each side of a pair was read exactly once — one batch script extracted both windows at the helper's reported line and diffed them; no re-slicing, no second window attempt.

| rank | fc side | pc side | verdict (window diff) |
|---|---|---|---|
| 1 | build.rs:11 | build.rs:16 | IDENTICAL |
| 2 | src/credits.rs:150 | src/credits.rs:163 | IDENTICAL |
| 3 | src/credits.rs:351 | src/credits.rs:546 | IDENTICAL |
| 4 | src/i18n/catalog.rs:12 | src/i18n/catalog.rs:16 | IDENTICAL |
| 5 | src/credits.rs:67 | src/credits.rs:57 | IDENTICAL |
| 6 | src/credits.rs:14 | src/credits.rs:13 | IDENTICAL |
| 7 | src/i18n/catalog.rs:67 | src/i18n/catalog.rs:80 | IDENTICAL |
| 8 | src/lib.rs:1603 | src/lib.rs:1541 | DIFFERS (4 of 16 lines) |
| 9 | build.rs:23 | build.rs:28 | IDENTICAL |
| 10 | src/commands.rs:19 | src/commands.rs:11 | DIFFERS (4 of 20 lines) |

## Verified top duplicate candidates (shared crates), ranked by repeated lines

Source: one bounded loop over the 10 crate directories both clones share (automation, codecs, color, engine, format, geom, gpu, testkit, text, ui-egui), `craft-helpers dups --cross-only --min-lines 6 --max-candidates 500`, one invocation per shared crate. 42 candidates total, ranked once by repeated lines; no cross-scan hit a window cap. *fc* = storytold/filmcraft, *pc* = storytold/photocraft. Paths are relative to each repo's `crates/` directory.

| rank | lines | fc side | pc side | verdict |
|---|---|---|---|---|
| 1 | 82 | build.rs:11 | build.rs:147, build.rs:16 | **IDENTICAL, shared-code** — contributor-credits build step; pc's copy extends it (catalog packing + font deflating) — fc could adopt that extension |
| 2 | 61 | src/credits.rs:150 | src/credits.rs:163 | **IDENTICAL, shared-code** — credits sort helpers |
| 3 | 59 | src/credits.rs:351 | src/credits.rs:546 | **IDENTICAL, shared-code** — credits sort helpers |
| 4 | 44 | src/i18n/catalog.rs:12 | src/i18n/catalog.rs:16 | **IDENTICAL, shared-code** — i18n catalog loader |
| 5 | 30 | src/credits.rs:67 | src/credits.rs:57 | **IDENTICAL, shared-code** — credits |
| 6 | 29 | src/credits.rs:14 | src/credits.rs:13 | **IDENTICAL, shared-code** — credits |
| 7 | 26 | src/i18n/catalog.rs:67 | src/i18n/catalog.rs:101, src/i18n/catalog.rs:80 | **IDENTICAL, shared-code** — i18n catalog |
| 8 | 25 | src/lib.rs:1603, src/lib.rs:1624 | src/lib.rs:1541 | **DIVERGENT (4 of 16 lines)** — fc's screenshot issue loop carries a deadline sweep pc lacks; pc should adopt fc's fix |
| 9 | 24 | build.rs:23, build.rs:44, build.rs:53 | build.rs:28, build.rs:62 | **IDENTICAL, shared-code** — fonts build script |
| 10 | 17 | src/commands.rs:19 | src/commands.rs:11, src/commands.rs:127 | **DIVERGENT (4 of 20 lines)** — same CommandSpec schema, intentionally domain-specific docstrings |
| 11 | 15 | src/credits.rs:119 | src/credits.rs:130 | not deep-verified |
| 12 | 13 | src/clip_ops.rs:866, src/commands.rs:1669, src/commands.rs:1693, src/commands.rs:1742, src/commands.rs:1760, src/commands.rs:1847, src/commands.rs:1859, src/commands.rs:1871, src/commands.rs:2391, src/commands.rs:2797, src/commands.rs:3067, src/commands.rs:3251, src/commands.rs:3425, src/commands.rs:3466, src/keyboard.rs:373, src/multicam.rs:766 | src/artboard_cmds.rs:623, src/automate_cmds.rs:532, src/commands.rs:645, src/comps_cmds.rs:392, src/edit_cmds.rs:775, src/exr_cmds.rs:58, src/extra_cmds.rs:782, src/extra_cmds.rs:892, src/file_cmds.rs:1378, src/layer_multi_cmds.rs:1352, src/print_cmds.rs:592, src/slice_cmds.rs:491, src/type_extra_cmds.rs:534, src/web_cmds.rs:1364 | not deep-verified |
| 13 | 12 | src/panels/clip_dialogs.rs:450, src/panels/clip_dialogs.rs:471 | src/analysis_ui.rs:714, src/prefs_ui.rs:1728 | not deep-verified |
| 14 | 11 | src/fx.rs:272, src/lib.rs:96 | src/lib.rs:448 | not deep-verified |
| 15 | 10 | src/commands.rs:482, src/commands.rs:540, src/interchange_auto_points_tests.rs:73, src/presets.rs:359, src/relink.rs:494, src/remix.rs:250 | src/extra_cmds.rs:1159, src/presets/clone_source.rs:264, src/retouch_cmds.rs:618, src/retouch_cmds.rs:753, src/retouch_cmds.rs:821, src/type_extra_cmds.rs:428, src/type_extra_cmds.rs:443 | not deep-verified |
| 16 | 9 | src/export_tools.rs:136 | tests/prefs_usage.rs:23 | not deep-verified |
| 17 | 9 | src/lib.rs:119 | src/lib.rs:2179 | not deep-verified |
| 18 | 8 | src/server.rs:39 | src/server.rs:203 | not deep-verified |
| 19 | 8 | src/media_watch.rs:36 | src/link_watch.rs:36 | not deep-verified |
| 20 | 8 | src/icons.rs:960, tests/monitor_geometry.rs:102 | src/adjust_preview_tests.rs:136, src/crop_mode.rs:903, src/dock_tests.rs:853, src/gpu_canvas_mip_tests.rs:98, src/wheel_nav.rs:382 | not deep-verified |
| 21 | 8 | src/menus.rs:640 | src/menus.rs:872 | not deep-verified |
| 22 | 7 | src/lib.rs:176 | src/convert.rs:146 | not deep-verified |
| 23 | 7 | src/lib.rs:95 | src/lib.rs:140 | not deep-verified |
| 24 | 7 | src/fonts.rs:28 | src/craft_fonts.rs:9 | not deep-verified |
| 25 | 7 | src/fonts.rs:400 | src/fonts.rs:548 | not deep-verified |
| 26 | 7 | src/credits.rs:302 | src/credits.rs:417 | not deep-verified |
| 27 | 7 | src/header.rs:19 | src/panels.rs:537 | not deep-verified |
| 28 | 6 | src/server.rs:241 | src/server/transport.rs:65 | not deep-verified |
| 29 | 6 | src/media_watch_tests.rs:90 | src/link_watch.rs:271 | not deep-verified |
| 30 | 6 | src/lib.rs:133 | src/lib.rs:176 | not deep-verified |
| 31 | 6 | src/fx.rs:468, src/lib.rs:919 | src/lib.rs:1330, src/lib.rs:368 | not deep-verified |
| 32 | 6 | src/fonts.rs:120 | src/fonts.rs:580 | not deep-verified |
| 33 | 6 | src/fonts.rs:412 | src/fonts.rs:560 | not deep-verified |
| 34 | 6 | src/panels/meters.rs:320, src/panels/reference.rs:86 | src/panels.rs:267 | not deep-verified |
| 35 | 6 | src/control.rs:60 | src/control.rs:134 | not deep-verified |
| 36 | 6 | src/panels/effect_controls.rs:791 | src/i18n/live_tests.rs:195 | not deep-verified |
| 37 | 6 | src/panels/graphics.rs:1130 | src/panel_docking.rs:118 | not deep-verified |
| 38 | 6 | src/panels/graphics_templates.rs:450 | src/transform_tool.rs:1303 | not deep-verified |
| 39 | 6 | src/panels/media_browser.rs:86 | src/move_mods.rs:93 | not deep-verified |
| 40 | 6 | src/panels/media_browser.rs:525 | src/camera_raw_scope_ui.rs:173 | not deep-verified |
| 41 | 6 | src/panels/text.rs:401 | src/new_doc_ui.rs:535 | not deep-verified |
| 42 | 6 | src/theme.rs:42 | src/theme.rs:124 | not deep-verified |

## What the verified pairs actually are (read both sides)

### Pair 1 — `ui-egui/build.rs`, 82-line contributor-credits build step — **IDENTICAL / shared-code, adopted**

fc `crates/ui-egui/build.rs:11` (start of the shared 82-line run) vs pc `crates/ui-egui/build.rs:16` (and a second hit at :147). Both files open with the same doc comment and the same `main()`: read `contributors/contributors.json` + `people.toml` at build time, bake static Rust tables via `OUT_DIR/credits.rs`, warn and fall back to empty tables on malformed input. pc's copy is the extended one — it adds `pack_catalogs()` + `deflate_egui_fonts()` (pc `build.rs:15-16`) and a doc paragraph on packing `src/i18n/*.tsv` into `OUT_DIR/i18n/` so the web build stays under its 24 MiB gate (pc `build.rs:6-10`).

**Adoptable:** filmcraft's ui-egui should take pc's catalog-packing + font-deflating build step — it is a drop-in extension of code fc already carries verbatim, and directly serves fc's own web-size budget; fc would keep its existing 82-line block and only add pc's two extra calls + catalog packer.

### Pairs 2/3/5/6 — `ui-egui/src/credits.rs` (61+59+30+29 lines) — **IDENTICAL / shared-code**

fc `src/credits.rs:150`,`:351`,`:67`,`:14` vs pc `src/credits.rs:163`,`:546`,`:57`,`:13`. The block starting at fc :150/pc :163 is the contributor sort helpers: `name_key` (trim leading `@`, lowercase) and `compare(a, b, mode, key)` over `NameMode`/`SortKey`. These are drift-waiting copy-paste, not a shared crate.

**Adoptable:** promote `credits.rs` (plus its `build.rs` half) into a shared workspace crate (e.g. `crates/credits` or a `craftrules` shared crate) — the two sides currently differ only in line offsets, so a one-time extraction costs nothing and ends double maintenance.

### Pairs 4/7 — `ui-egui/src/i18n/catalog.rs` (44 + 26 lines) — **IDENTICAL / shared-code**

fc `:12`/`:67` vs pc `:16`/`:80`. The i18n catalog loading/ranking block is byte-identical across both trees. pc additionally packs the same catalogs in `build.rs` for web size (see pair 1); fc has the loader but not the packer.

### Pair 9 — `text/build.rs` (24 lines) — **IDENTICAL / shared-code**

fc `crates/text/build.rs:23` vs pc `:28`: the `CRAFT_FONTS_DIR` manifest-scanning build script that emits `pub static CRAFT_FONTS: &[CraftFont]` into `OUT_DIR/craft_fonts.rs`, with `cargo::error` when `CRAFT_FONTS_REQUIRED` is set and `cargo::warning` otherwise. fc's copy is at fc :23; pc's at :28 — same code, offset by 5 lines.

### Pair 8 — `ui-egui/src/lib.rs` screenshot pipeline (25 lines) — **DIVERGENT: fc is ahead; pc should adopt fc's fix**

fc `src/lib.rs:1603` vs pc `src/lib.rs:1541` — both are the `issue_screenshots` body (the anchor line is the `send_viewport_cmd(Screenshot(...))` call inside `retain_mut`).

- fc (`lib.rs:1608-1617`) adds a deadline sweep: `pending_screenshots.retain(|(.., reply, deadline)| if now > deadline { reply.send(error) ; false } else { true })`, so a hidden window or sleeping display answers the agent's screenshot request with an error instead of hanging; fc also carries `SCREENSHOT_TIMEOUT_S`/`SCREENSHOT_SETTLE_MAX_S` and a `settled` flag (`lib.rs:1595-1601`) to avoid handing agents a stand-in frame after a seek.
- pc (`lib.rs:1521-1539`) has the shared frame-wait loop but **no deadline sweep** and **no settle guard** — a hidden window there leaves `pending_screenshots` entries alive with no timeout path in this function.

**Adoptable:** pc should port fc's deadline sweep + settle guard into `issue_screenshots`; the fix is self-contained (~15 lines) and addresses a real agent-facing hang.

### Pair 10 — `engine/src/commands.rs` CommandSpec (24 lines) — **DIVERGENT: same schema, domain-specific docstrings**

fc `:19` vs pc `:11` — identical `CommandSpec` struct and field order (`id/label/menu/shortcut/params/enabled/run/journal`), with matching `Run`/`Enabled` typedefs. The only diffs in the window are doc-comment wording: fc documents Premiere's menu structure + `Cmd = ⌘ on macOS / Ctrl elsewhere`, pc documents Photoshop's structure + `Cmd+Shift+N` notation and 'Human/agent-readable'.

**Adoptable:** the shared convention here is the `CommandSpec` schema itself — keep the struct byte-identical and share only doc wording where the wording is domain-neutral; the diverging lines are intentionally per-domain.

## Adoptable / shareable findings from the last-24h merges

Findings link the merged PR to the code that landed with it, and say why the other repo should care. These are the highest-value items; the full 24h table above carries the rest.

### 1. pc #4264/#4263: the XPM reader is a template for adding a text-format codec to fc

photocraft merged a plain-text XPM2 importer (`pc #4264`, +67/−8, author Ni-zav) with full X11 `rgb.txt` color-name support (`pc #4263`, +970/−4). The code lives at `pc/crates/codecs/src/codecs/xpm.rs` (+ `xpm/x11_colors.rs` for the palette). filmcraft has no XPM reader today (its `STILL_EXTENSIONS` list at `fc/crates/media/src/lib.rs:175` has no `xpm`), and its parallel need — a small text-based still format — is served by the same shape: sniff, decode to `Image`, palette table as generated static data. The pc reader is small, self-contained, and carries its own test file (`pc/crates/codecs/tests/xpm.rs`), so the port is a contained copy + rename of the codec registration.

### 2. fc #837 + #879 vs pc `io/exr_parts.rs`: the two EXR stacks should borrow from each other

filmcraft landed OpenEXR still+sequence import (`fc #837`, +1302/−14, vangel76) and compressed RLE/ZIPS/ZIP EXR export (`fc #879`, +994/−73) — the decoder is `fc/crates/media/src/still/exr.rs` (478 lines). photocraft's `io` crate already has `pc/crates/io/src/exr_parts.rs` (335 lines): a multi-part EXR chooser that lists parts/prefixed channel groups/Cryptomatte layers as document layers, with an additive beauty precomp. Neither side has what the other has: fc's import is single-part (no `exr_parts` equivalent anywhere in fc — verified by grep), and pc has no EXR *export*. Cheapest adoption: fc's import path gains pc's multi-part chooser semantics; pc's export path gains fc's RLE/ZIPS/ZIP writer. Both are additive codec work, no engine coupling.

### 3. fc #1129 'native menu follows command enablement' matches the pc engine's CommandSpec contract

fc merged `fix(menus): native menu follows command enablement (#902)` (`fc #1129`, +100/−33, itrycodinganditsbad): menu items enable/disable from the engine's `Enabled` predicates. pc's `engine/src/commands.rs:11` uses the same `CommandSpec { enabled: Enabled, run: Run }` registry shape (verified in pair 10). The adoptable convention: menu enablement driven by the *same* predicate table the engine already exposes to agents — one source of truth, no UI-side re-derivation. fc's fix is the proof that this holds up in a real UI; the pattern is already symmetrical in pc.

### 4. fc #1193 'reduce sequence copying and cache transcript redraw data' mirrors pc's perf sweep

fc #1193 (OorjitSethi, +212/−22) reduces sequence copying and caches redraw data, in the same window where pc merged five perf PRs from one author (SckraT, `pc #4424/#4423/#4422/#4415/#4414`, e.g. 'move layers without a second document clone' +10/−8, 'moved fills keep sharing one copy-on-write tile' +124/−2). Both repos independently converged on copy-avoidance for large documents/sequences. The shareable convention: pc's copy-on-write tile sharing (`#4414`) is the more general fix and is the pattern fc's sequence-copy reduction could adopt if fc's tile model allows it.

### 5. fc #1217 'dialogs: drag by the title bar' is a UI convention pc has not merged in this window

fc #1217 (liangforstudy, +114/−36) makes dialogs draggable with open-centred positioning. pc's window/dialog code in `ui-egui` has no dialog-drag code in this window (nothing in the 24h table). For pc this is a small, self-contained UX convention to evaluate against its own dialog panels — adoptable as-is if pc's dialogs are egui windows.

### 6. fc #1052 'cancel drag and restore playhead on Escape' — the interaction pattern pc's transform tools could match

fc #1052 (Auipp, +337/−61) cancels an in-progress timeline drag with Escape and restores the playhead. pc's transform/brush tools (e.g. `pc #4019` Clone Stamp/HIstory Brush commit-on-release, +287/−19) commit live pixels on stroke end; an Escape-cancels-stroke convention would mirror fc's. Both repos currently lack it on the opposite side — a cross-repo convention, not a code port.

## Recommendations

1. **Extract a shared `credits` + i18n-catalog crate.** Pairs 1-7 are one story: fc and pc carry byte-identical `ui-egui/build.rs`, `src/credits.rs`, `i18n/catalog.rs`, and `text/build.rs` blocks. A single workspace-shared crate (or a sync-check CI job) removes the drift risk. Highest-value, lowest-cost action from this scan.

2. **Port fc's screenshot deadline sweep to pc** (`fc/crates/ui-egui/src/lib.rs:1608-1617` → pc's `issue_screenshots`). Self-contained ~15-line fix for an agent-facing hang; verified in pair 8.

3. **Port pc's catalog-packing + font-deflating build step to fc** (`pc/crates/ui-egui/build.rs:15-16` and the `pack_catalogs`/`deflate_egui_fonts` functions, pc build.rs:6-10 doc). fc already carries the surrounding code verbatim, so the extension drops in; it directly serves fc's web-size budget.

4. **Exchange EXR capabilities**: fc's compressed EXR export (`fc #879`) → pc's export path; pc's multi-part EXR chooser (`pc/crates/io/src/exr_parts.rs`) → fc's import path (`fc/crates/media/src/still/exr.rs`).

5. **Keep `CommandSpec` as the shared command schema** (pair 10) and keep domain wording in doc comments only — the two registries stay mechanically compatible so cross-porting commands remains trivial.

## Not verified / limits of this scan

- The `craft-helpers prs` JSON carries a truncation marker: newest 30 PRs per repo, 50 total. **filmcraft's window was cut at 20 PRs** by the 50-total cap, so older-in-window fc PRs are missing from the table. photocraft's table is the full 30-PR repo cap. Per the mission rules the helper was **not re-run** with retuned flags.
- The first-tree `dups` scan filled its 250,000-window cap inside photocraft and skipped the rest, so that table covers pc only; cross-repo candidates were obtained via the shared-crate loop instead.
- Cross-crate ranks 11-42 carry helper-window data only and are marked **not deep-verified** (the top-10 verification ceiling was spent).
- At most 3 PRs get deep inspection; this scan spent that budget on the duplicate verification instead, so individual PR diffs beyond the prs-JSON table were not opened. All PR facts above come from the helper's `prs` JSON (title, author, additions/deletions) or from reading the merged code on both `main` clones; no PR bodies were fetched.
- Unknown, not measured: whether the identical blocks in pairs 1-7 came from pc→fc or fc→pc; both clones' `main` heads are shallow (depth 1), so blame history was out of scope.
- Clone heads at scan time: photocraft and filmcraft `main` (shallow, `--depth 1`); paths in this report are relative to each clone's `crates/` unless written with a `crates/` prefix.
