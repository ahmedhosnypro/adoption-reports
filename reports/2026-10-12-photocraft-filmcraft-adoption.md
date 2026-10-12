# Cross-repo adoption report — photocraft + filmcraft (last 24h)

Scope: merged pull requests in storytold/photocraft and storytold/filmcraft within the last 24 hours, scanned for adoptable/shared patterns, fixes, helpers, and conventions, plus top duplicate-code candidates. Read-only study; findings delivered via PR on this repository.

## Merged PRs (last 24h)

(The full 50-PR listing appears in the "All 50 merged PRs" section below.)


Note: helper caps hit (prs-per-repo 30, prs-total 50 — more merged PRs may exist per repo). One API fetch error: photocraft PR #4147.

| Repo | PR | Author | Title | +/− |
|---|---|---|---|---|
| photocraft | #3979 | jonathanwxh-cell | Make channel filter previews match the committed edit | +388 / -20 |
| photocraft | #4396 | aweussom | Windows: keep full screen and maximized apart; never restore full screen | +100 / -2 |
| photocraft | #4465 | FabioLissi | .atn: map the remaining frequent Photoshop events (#219) | +689 / -21 |
| photocraft | #4145 | FredApps | View: Esc leaves full screen modes (part of #4116) | +60 / -12 |
| photocraft | #3955 | Erica4fr | File Handling: wire Maximize PSD and PSB File Compatibility (#204) | +268 / -34 |
| photocraft | #4109 | vbasky | Fix multi-layer Delete and Move drags on a locked Background | +41 / -2 |
| photocraft | #4078 | marcoarnulfo | Delete with several layers selected deletes them, not the active layer's targeted mask (#4025) | +36 / -2 |
| photocraft | #4456 | FabioLissi | Actions panel: set folders, dialog toggle, Insert Stop (#219) | +897 / -30 |
| photocraft | #4079 | marcoarnulfo | Properties: a new adjustment or fill layer brings Properties to the front (#4028) | +40 / -0 |
| photocraft | #3931 | zenjabba | fix(gpu): preflight compositor uniform buffer limits | +192 / -3 |
| photocraft | #4093 | mroxso | fix(ui): default the Move tool Auto-Select target to Group | +5 / -4 |
| photocraft | #3925 | Gotix-eg | feat(engine): recolor vector shape layer fill with Alt+Backspace and Cmd+Backspace | +78 / -2 |
| photocraft | #4434 | FabioLissi | Load and save Photoshop Actions (.atn) (#4356, #219) | +4091 / -79 |
| photocraft | #3924 | zenjabba | fix(color): validate RGB working profiles atomically | +300 / -14 |
| photocraft | #3970 | jonathanwxh-cell | Fix group transform bounds with active pixel selections | +80 / -8 |
| photocraft | #3959 | xsvm | Selection: lasso polygons scan only the edges that cross each row | +167 / -29 |
| photocraft | #3571 | switch87 | Save As: a saved .pcraft manifest reports the file it was saved under | +58 / -3 |
| photocraft | #3978 | jonathanwxh-cell | Preserve grayscale appearance in profileless exports | +71 / -1 |
| photocraft | #3990 | cloudalister | Pencil: no 8-bit dither on aliased strokes, one flat colour at partial opacity | +20 / -2 |
| photocraft | #3917 | buivanvu94 | feat(automation): allow Crop and Straighten Photos through automation (#1052) | +3 / -0 |
| photocraft | #4362 | vangel76 | Tests: allow-list language-invariant bit-depth labels, add missing tr/hu 'Enable animations' (#4359) | +8 / -1 |
| photocraft | #3872 | skylartaylor | Use craft-print for system printing | +434 / -209 |
| photocraft | #4253 | bommerts | Web: wasm back under the 24 MiB gate with ~1 MiB headroom (25.38 → 24.17 MB) | +304 / -51 |
| photocraft | #3794 | echelon | Release workflow: pass the Azure signing secrets | +6 / -0 |
| photocraft | #3831 | Skaywalker | i18n: add Hungarian (hu) UI translation | +4006 / -5 |
| photocraft | #3809 | yeniufuklar-com | i18n(tr): add Turkish UI translation catalog | +3800 / -3 |
| photocraft | #3871 | seandellis | feat: Alt+Cancel → Reset for opt-in command dialogs | +646 / -54 |
| photocraft | #3641 | Korg1ch | fix(linux): avoid duplicate AppImage desktop launcher (#3623) | +61 / -18 |
| photocraft | #3808 | diegochagas | Remove tool: Create a new layer, and Remove after each stroke off | +414 / -19 |
| filmcraft | #1169 | echelon | Release workflow: pass the Azure signing secrets | +6 / -0 |
| filmcraft | #1198 | n-delic | #1124: ⌘D / ⇧⌘D apply transitions to the selected clips or edit points | +104 / -4 |
| filmcraft | #1193 | OorjitSethi | ui: reduce sequence copying and cache transcript redraw data | +212 / -22 |
| filmcraft | #1168 | haranishi | fix: Close Gapをショートカットに割り当てられるようにする | +115 / -2 |
| filmcraft | #1217 | liangforstudy | dialogs: drag them by the title bar (open centred, no longer anchored) | +114 / -36 |
| filmcraft | #1052 | Auipp | timeline: cancel drag and restore playhead on Escape (#580) | +337 / -61 |
| filmcraft | #1063 | vbasky | Linux: VA-API EncSlice probe and bounded export GPU wait (#1058) | +14 / -5 |
| filmcraft | #1067 | vangel76 | #1039: 8-bit HEVC pictures as u8, in-place motion compensation (−14…23 % per frame), big-picture analysis | +1316 / -275 |
| filmcraft | #1070 | luniiya | UI: favorite themes and appearance shortcuts | +187 / -7 |
| filmcraft | #964 | mjohnson7cd | fix(ui): add Korean font fallback for UI text | +63 / -15 |
| filmcraft | #1165 | MarekSpodBiedry | Trim MP3 encoder delay when decoding audio files (#1137) | +56 / -3 |
| filmcraft | #865 | earlvanze | M7: optimize audio DSP and isolate the unchanged mixer throughput gate | +587 / -190 |
| filmcraft | #1046 | vbasky | Median Radius is not capped at four working pixels | +88 / -1 |
| filmcraft | #837 | vangel76 | #828: import OpenEXR stills and image sequences | +1302 / -14 |
| filmcraft | #1159 | haranishi | fix: エフェクトコントロールの矩形選択とShiftスナップを修正 (#967) | +830 / -54 |
| filmcraft | #1139 | itrycodinganditsbad | fix(timeline): snap sub-frame timeline.place to the frame grid; inspect counts export's frames (#1101) | +56 / -1 |
| filmcraft | #879 | vangel76 | #874: compressed (RLE / ZIPS / ZIP) OpenEXR export | +994 / -73 |
| filmcraft | #1068 | vangel76 | #1065: CinemaDNG / DNG import with a clean-room decoder | +3612 / -21 |
| filmcraft | #931 | liangforstudy | #402: animated GIF and APNG import as clips, with transparency | +481 / -4 |
| filmcraft | #1129 | itrycodinganditsbad | fix(menus): native menu follows command enablement (#902) | +100 / -33 |
| filmcraft | #1033 | ReReddo | export: type the file name and pick the location in Quick Export | +166 / -19 |

## Duplicate scan status

- Global scan (pc tree first, fc): 20 candidates; window cap 250000 reached during root pc, remaining files skipped (filmcraft largely skipped in the global pass).
- Cross-repo pass: 10 shared crates scanned (`automation, codecs, color, engine, format, geom, gpu, testkit, text, ui-egui`) with `--cross-only`; all 10 crates completed, no skipped note on any.
- 62 ranked candidates total; ranking is by repeated-lines, descending, done once into $RUNNER_TEMP.

## Adoptable / shareable findings - from PR titles plus stats

- photocraft #4434 + #4456 - FabioLissi: Photoshop .atn load/save plus Actions panel features, +4091/-79 and +897/-30. A large self-contained import/export feature; the shape to copy if filmcraft needs preset/action import.
- photocraft #3931 zenjabba: fix gpu preflight compositor uniform-buffer limits, +192/-3. Defensive GPU-limits preflight; both repos share a gpu crate.
- photocraft #3924: fix color validate RGB working profiles atomically, +300/-14. Atomic validation pattern in the shared color area.
- photocraft #4253: wasm back under the 24 MiB gate, +304/-51. Wasm size-gate discipline relevant to any web builds.
- photocraft #3872: adopt craft-print for system printing, +434/-209. craft-* shared-utility adoption; check whether filmcraft also uses craft-print.
- filmcraft #1067: 8-bit HEVC pictures as u8 with in-place motion compensation, minus 14-23 percent per frame, +1316/-275. Perf pattern for sibling image-processing paths in photocraft.
- filmcraft #865: audio DSP optimization plus isolating a mixer throughput gate, +587/-190. Perf-gate isolation pattern.
- filmcraft #1068: CinemaDNG/DNG import with a clean-room decoder, +3612/-21. Big import-feature pattern like the .atn work.
- filmcraft #1139: snap sub-frame timeline.place to the frame grid, +56/-1. Small precise grid-snapping fix.
- filmcraft #964: Korean font fallback for UI text, +63/-15. Font-fallback convention; pairs with photocraft hu/tr i18n PRs #3831/#3809.
- Both repos merged an identical Release workflow change: pass the Azure signing secrets. photocraft #3794 and filmcraft #1169, both by echelon, +6/-0, same 24h window. Same CI change applied to both repos; convention-level sync worth a look.

## Verified duplicate-code candidates (top 10, in ranked order; each side read once, diffed in one batch)

Cross-repo, verified identical:

- fc crates/ui-egui/src/credits.rs#150 vs pc crates/ui-egui/src/credits.rs#163 - 61 lines, diff EMPTY (identical).
- fc crates/ui-egui/src/credits.rs#351 vs pc crates/ui-egui/src/credits.rs#546 - 59 lines, diff EMPTY (identical).
- fc crates/ui-egui/src/credits.rs#67 vs pc crates/ui-egui/src/credits.rs#57 - 30 lines, diff EMPTY (identical).
- fc crates/ui-egui/src/i18n/catalog.rs#12 vs pc crates/ui-egui/src/i18n/catalog.rs#16 - 44 lines; only difference is a doc-comment line rewrap (6 diff lines, code identical).

Normalized near-duplicates (same code, intentional drift):

- pc crates/paint/src/render.rs#229 vs pc crates/paint/src/render_reference.rs#8 - 103-line window, 38 diff lines; the reference file tracks production render code but omits the newer vectorised fast-path branch (comment: keep computed tips separate for vectorisation). Reference-copy pattern.
- pc crates/automation/tests/agent_tasks.rs#8 vs pc crates/automation/tests/agent_tasks_more.rs#6 - 59 lines, 18 diff lines; a test server/harness block copied between the two agent-task test files, pc side carries extra Windows directory-handle cleanup comments. Harness duplication.
- pc crates/algo/src/pixelate.rs#23 vs pc crates/algo/src/pixelate/reference.rs#4 - 49 lines, 18 diff lines; production adds stack-allocated screen cache metadata the reference copy lacks. Reference-copy drift.

Diverged shared scaffold:

- fc crates/ui-egui/build.rs#11 vs pc crates/ui-egui/build.rs#16 - 82-line window, 131 diff lines; shared build.rs skeleton but pc additionally calls pack_catalogs() and deflate_egui_fonts(). The two repo-local ui-egui crates have drifted.

Inconclusive on first diff (recorded from collect-phase data, not deep-verified):

- pc crates/algo/src/gallery.rs#33 vs pc crates/algo/src/tests_iris_reference.rs#12 - ranked 103 lines; diff window partially misaligned (125 diff lines with leading-context offset), so verdict unknown beyond the helper's 103-line match across gallery.rs, tests_iris_reference.rs and tests_tilt_shift_reference.rs.
- pc crates/algo/src/hdr.rs#418 vs pc crates/compose/src/adjust.rs#976 - ranked 32 lines; window misaligned (56 diff lines, offset insertion). Collect data shows the same 32-line block across 8 pc files (algo/hdr.rs, algo/quantize.rs, cms/clut.rs, engine/retouch_cmds/pattern_stamp.rs, paint/bg_erase.rs, paint/replace.rs x2, paint/retouch.rs) - likely a copied gradient-stop interpolation helper; not deep-verified.

Whole-file read (both sides, read once each): pc credits.rs is 621 lines vs fc 422 - the same credits panel component living in both repos. pc's copy routes labels through tl! i18n (Username / Merged PRs / Lines added ...), fc's copy instead attaches automation::Registry id suffixes (id() returning username / displayName / realName). The three identical 30-61-line blocks above are this component's common core; the repos have diverged around it. Strongest single extraction candidate: a shared credits component (or generated-from-one-source approach) instead of two drifting copies.
- craft-print check: pc Cargo.toml line 41 pins craft-print from git storytold/craft-libs rev d991bf6; fc has no craft-print dependency in its workspace manifests (grep over fc Cargo.toml and crate manifests found nothing) - pc #3872 adopted a shared lib that filmcraft has not.

## Adoptable / shareable findings (deep inspection, budget 3)

### PC #3931 - fix gpu preflight compositor uniform-buffer limits (+192/-3, zenjabba)
File: crates/gpu/src/lib.rs, +192/-3. Adds a preflight that enumerates wgpu device Limits and fails early when the compositor needs more uniform-buffer storage than the device reports (e.g. bindless slices). Adoptable in fc's shared engine/gpu path: the same preflight guard belongs in filmcraft's render setup, since both repos carry a gpu crate with compositor-style uniform buffers. Why: cheap defense at init time against device-dependent uniform-buffer overruns, exactly the class of bug that otherwise shows up only on users' GPUs.

### PC #3924 - fix color validate RGB working profiles atomically (+300/-14)
File: crates/color/src/working.rs (+ helpers). Reads and writes WORKING_PROFILES atomically under a single lock, validates on load, never mutates the global in place, and pairs decode with encode consistently. Adoptable pattern for fc's color handling (shared color crate): validate-then-install for process-wide profile tables. Why: prevents torn state where one thread reads a half-registered profile.

### FC #1067 - HEVC u8 in-place motion compensation, -14..23% per frame (+1316/-275)
File: crates/codec-hevc/src/motion_comp.rs. Splits 8-bit vs 16-bit luma paths, stores 8-bit planes as u8 (half the bandwidth), and compensates in place to avoid a full-plane copy per frame. Why adoptable: photocraft's image-processing paths (paint/compose loops over Image) have the same 8-bit-vs-16-bit split opportunity, and the in-place-write trick is a direct transfer.

## All 50 merged PRs (one line each, from the prs JSON)

### photocraft (25 of its merged PRs in this window; helper cap 30/repo and 50 total hit)



### filmcraft (remaining 25)



## All 50 merged PRs - one line each, from the prs JSON

### photocraft

```
photocraft #3979 | jonathanwxh-cell | Make channel filter previews match the committed edit | +388/-20
photocraft #4396 | aweussom | Windows: keep full screen and maximized apart; never restore full screen | +100/-2
photocraft #4465 | FabioLissi | .atn: map the remaining frequent Photoshop events (#219) | +689/-21
photocraft #4145 | FredApps | View: Esc leaves full screen modes (part of #4116) | +60/-12
photocraft #3955 | Erica4fr | File Handling: wire Maximize PSD and PSB File Compatibility (#204) | +268/-34
photocraft #4109 | vbasky | Fix multi-layer Delete and Move drags on a locked Background | +41/-2
photocraft #4078 | marcoarnulfo | Delete with several layers selected deletes them, not the active layer's targeted mask (#4025) | +36/-2
photocraft #4456 | FabioLissi | Actions panel: set folders, dialog toggle, Insert Stop (#219) | +897/-30
photocraft #4079 | marcoarnulfo | Properties: a new adjustment or fill layer brings Properties to the front (#4028) | +40/-0
photocraft #3931 | zenjabba | fix(gpu): preflight compositor uniform buffer limits | +192/-3
photocraft #4093 | mroxso | fix(ui): default the Move tool Auto-Select target to Group | +5/-4
photocraft #3925 | Gotix-eg | feat(engine): recolor vector shape layer fill with Alt+Backspace and Cmd+Backspace | +78/-2
photocraft #4434 | FabioLissi | Load and save Photoshop Actions (.atn) (#4356, #219) | +4091/-79
photocraft #3924 | zenjabba | fix(color): validate RGB working profiles atomically | +300/-14
photocraft #3970 | jonathanwxh-cell | Fix group transform bounds with active pixel selections | +80/-8
photocraft #3959 | xsvm | Selection: lasso polygons scan only the edges that cross each row | +167/-29
photocraft #3571 | switch87 | Save As: a saved .pcraft manifest reports the file it was saved under | +58/-3
photocraft #3978 | jonathanwxh-cell | Preserve grayscale appearance in profileless exports | +71/-1
photocraft #3990 | cloudalister | Pencil: no 8-bit dither on aliased strokes, one flat colour at partial opacity | +20/-2
photocraft #3917 | buivanvu94 | feat(automation): allow Crop and Straighten Photos through automation (#1052) | +3/-0
photocraft #4362 | vangel76 | Tests: allow-list language-invariant bit-depth labels, add missing tr/hu 'Enable animations' (#4359) | +8/-1
photocraft #3872 | skylartaylor | Use craft-print for system printing | +434/-209
photocraft #4253 | bommerts | Web: wasm back under the 24 MiB gate with ~1 MiB headroom (25.38 → 24.17 MB) | +304/-51
photocraft #3794 | echelon | Release workflow: pass the Azure signing secrets | +6/-0
photocraft #3831 | Skaywalker | i18n: add Hungarian (hu) UI translation | +4006/-5
```

### filmcraft

```
photocraft #3809 | yeniufuklar-com | i18n(tr): add Turkish UI translation catalog | +3800/-3
photocraft #3871 | seandellis | feat: Alt+Cancel → Reset for opt-in command dialogs | +646/-54
photocraft #3641 | Korg1ch | fix(linux): avoid duplicate AppImage desktop launcher (#3623) | +61/-18
photocraft #3808 | diegochagas | Remove tool: Create a new layer, and Remove after each stroke off | +414/-19
filmcraft #1169 | echelon | Release workflow: pass the Azure signing secrets | +6/-0
filmcraft #1198 | n-delic | #1124: ⌘D / ⇧⌘D apply transitions to the selected clips or edit points | +104/-4
filmcraft #1193 | OorjitSethi | ui: reduce sequence copying and cache transcript redraw data | +212/-22
filmcraft #1168 | haranishi | fix: Close Gapをショートカットに割り当てられるようにする | +115/-2
filmcraft #1217 | liangforstudy | dialogs: drag them by the title bar (open centred, no longer anchored) | +114/-36
filmcraft #1052 | Auipp | timeline: cancel drag and restore playhead on Escape (#580) | +337/-61
filmcraft #1063 | vbasky | Linux: VA-API EncSlice probe and bounded export GPU wait (#1058) | +14/-5
filmcraft #1067 | vangel76 | #1039: 8-bit HEVC pictures as u8, in-place motion compensation (−14…23 % per frame), big-picture analysis | +1316/-275
filmcraft #1070 | luniiya | UI: favorite themes and appearance shortcuts | +187/-7
filmcraft #964 | mjohnson7cd | fix(ui): add Korean font fallback for UI text | +63/-15
filmcraft #1165 | MarekSpodBiedry | Trim MP3 encoder delay when decoding audio files (#1137) | +56/-3
filmcraft #865 | earlvanze | M7: optimize audio DSP and isolate the unchanged mixer throughput gate | +587/-190
filmcraft #1046 | vbasky | Median Radius is not capped at four working pixels | +88/-1
filmcraft #837 | vangel76 | #828: import OpenEXR stills and image sequences | +1302/-14
filmcraft #1159 | haranishi | fix: エフェクトコントロールの矩形選択とShiftスナップを修正 (#967) | +830/-54
filmcraft #1139 | itrycodinganditsbad | fix(timeline): snap sub-frame timeline.place to the frame grid; inspect counts export's frames (#1101) | +56/-1
filmcraft #879 | vangel76 | #874: compressed (RLE / ZIPS / ZIP) OpenEXR export | +994/-73
filmcraft #1068 | vangel76 | #1065: CinemaDNG / DNG import with a clean-room decoder | +3612/-21
filmcraft #931 | liangforstudy | #402: animated GIF and APNG import as clips, with transparency | +481/-4
filmcraft #1129 | itrycodinganditsbad | fix(menus): native menu follows command enablement (#902) | +100/-33
filmcraft #1033 | ReReddo | export: type the file name and pick the location in Quick Export | +166/-19
```

## Recommendations

1. Extract the credits panel core. The three verified identical 30-61-line blocks plus the whole-file drift (pc 621 lines with tl! i18n, fc 422 with automation ids) point at one shared component in storytold/craft-libs or a generated-from-one-source setup, before the two copies drift further.
2. Sync the ui-egui build.rs skeleton. pc's copy calls pack_catalogs() and deflate_egui_fonts(); fc's does not. If those steps are generally useful (catalog packing, font deflation for wasm size), fc should get them - 131 diff lines and growing.
3. Port pc #3931's GPU preflight guard into fc's gpu/engine setup. Both repos carry a gpu crate with compositor-style uniform buffers; failing fast on device Limits is cheap and device-independent to test.
4. Port the validate-atomically pattern from pc #3924 into fc's color/profile handling: read-validate-install under one lock, never mutate the global in place.
5. Adopt craft-print in fc or document why not. pc #3872 wired it; fc has no dependency on it today, so printing behavior will silently diverge.
6. Transfer fc #1067's 8-bit u8 in-place motion-compensation trick to photocraft's hot image loops where an 8-bit path can be split from 16-bit.
7. Keep the release-workflow sync going: the identical Azure signing-secrets workflow change (#3794 pc, #1169 fc, same author, same day) shows the two repos' CI is being changed in lockstep - a shared reusable workflow would make that the default instead of an accident.

## Verification statement

- Top 10 ranked candidates verified: 4 confirmed cross-repo identical/near-identical, 3 normalized near-duplicates inside pc, 1 diverged shared scaffold, 2 inconclusive on first window (recorded from collect data, marked not deep-verified).
- 3 of 3 allowed deep PR inspections used (pc #3931, pc #3924, fc #1067). Every other PR carries its one line from the prs JSON only.
- Helper caps: prs 30/repo, 50 total (truncated:true); global dups window cap hit at root pc; cross-repo scans all 10 crates completed. Findings above are bounded by those windows.
