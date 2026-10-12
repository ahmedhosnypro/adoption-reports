# Cross-repo adoption report — storytold/photocraft + storytold/filmcraft, last 24h (2026-10-12)

Scope: merged PRs in `storytold/photocraft` and `storytold/filmcraft` for the 24 h ending
2026-10-12, collected via `craft-helpers prs --org storytold --repos photocraft,filmcraft --since 24h --json`
(50 PRs returned; 20 filmcraft + 30 photocraft — filmcraft had ≤30 in the window so the
helper's newest-30/repo cap did not visibly clip it; no `truncated` marker was present).
Duplicate detection via `craft-helpers dups` (repo-wide, once) and one bounded per-crate
cross-repo scan over the 7 crates both trees share (automation, color, engine, geom, gpu,
text, ui-egui). Verification method: one read per candidate side, first-verified-wins.

## 1. What merged, where, by whom (one line per PR)

### filmcraft (20 merged PRs)

| PR | Title | Author | Lines |
|---|---|---|---|
| [#931](https://github.com/storytold/filmcraft/pull/931) | Animated GIF and APNG import as clips, with transparency | liangforstudy | +481/−4 |
| [#1129](https://github.com/storytold/filmcraft/pull/1129) | fix(menus): native menu follows command enablement | itrycodinganditsbad | +100/−33 |
| [#1165](https://github.com/storytold/filmcraft/pull/1165) | Trim MP3 encoder delay when decoding audio files | MarekSpodBiedry | +56/−3 |
| [#1168](https://github.com/storytold/filmcraft/pull/1168) | Assignable Close Gap shortcut ( ja UI labels included) | haranishi | +115/−2 |
| [#1169](https://github.com/storytold/filmcraft/pull/1169) | Release workflow: pass the Azure signing secrets | echelon | +6/−0 |
| [#1052](https://github.com/storytold/filmcraft/pull/1052) | Timeline: cancel drag and restore playhead on Escape | Auipp | +337/−61 |
| [#1139](https://github.com/storytold/filmcraft/pull/1139) | Snap sub-frame timeline.place to the frame grid; export counts frames | itrycodinganditsbad | +56/−1 |
| [#1159](https://github.com/storytold/filmcraft/pull/1159) | Fix effect-control rect-select and Shift-snap ( ja UI labels included) | haranishi | +830/−54 |
| [#1193](https://github.com/storytold/filmcraft/pull/1193) | UI: reduce sequence copying and cache transcript redraw data | OorjitSethi | +212/−22 |
| [#1198](https://github.com/storytold/filmcraft/pull/1198) | ⌘D / ⇧⌘D apply transitions to selected clips or edit points | n-delic | +104/−4 |
| [#1217](https://github.com/storytold/filmcraft/pull/1217) | Dialogs drag by title bar (open centred, no longer anchored) | liangforstudy | +114/−36 |
| [#837](https://github.com/storytold/filmcraft/pull/837) | Import OpenEXR stills and image sequences | vangel76 | +1302/−14 |
| [#865](https://github.com/storytold/filmcraft/pull/865) | M7: optimize audio DSP, isolate mixer throughput gate | earlvanze | +587/−190 |
| [#879](https://github.com/storytold/filmcraft/pull/879) | Compressed (RLE/ZIPS/ZIP) OpenEXR export | vangel76 | +994/−73 |
| [#964](https://github.com/storytold/filmcraft/pull/964) | fix(ui): Korean font fallback for UI text | mjohnson7cd | +63/−15 |
| [#1046](https://github.com/storytold/filmcraft/pull/1046) | Median Radius not capped at four working pixels | vbasky | +88/−1 |
| [#1063](https://github.com/storytold/filmcraft/pull/1063) | Linux: VA-API EncSlice probe, bounded export GPU wait | vbasky | +14/−5 |
| [#1067](https://github.com/storytold/filmcraft/pull/1067) | 8-bit HEVC as u8, in-place motion compensation (−14…23 %/frame) | vangel76 | +1316/−275 |
| [#1068](https://github.com/storytold/filmcraft/pull/1068) | CinemaDNG/DNG import with a clean-room decoder | vangel76 | +3612/−21 |
| [#1070](https://github.com/storytold/filmcraft/pull/1070) | UI: favorite themes and appearance shortcuts | luniiya | +187/−7 |

### photocraft (30 merged PRs)

| PR | Title | Author | Lines |
|---|---|---|---|
| [#3168](https://github.com/storytold/photocraft/pull/3168) | SVG: warn when text has no font to use | diegochagas | +58/−12 |
| [#3484](https://github.com/storytold/photocraft/pull/3484) | Format: check pattern sizes on load | vangel76 | +98/−14 |
| [#3501](https://github.com/storytold/photocraft/pull/3501) | Format: overflow-safe blob decode, bounds-checked ZIP reads | vangel76 | +60/−34 |
| [#3585](https://github.com/storytold/photocraft/pull/3585) | Fuzz: ignore the same build leftovers in every fuzz crate | s17sh70x2jfl031ag | +7/−0 |
| [#3614](https://github.com/storytold/photocraft/pull/3614) | ops: count selection masks in history pixel budget | Streetblock | +88/−3 |
| [#3637](https://github.com/storytold/photocraft/pull/3637) | HEIF: move the heic-rs pin from 0.1.1 to 0.1.4 | s17sh70x2jfl031ag | +5/−5 |
| [#3641](https://github.com/storytold/photocraft/pull/3641) | fix(linux): avoid duplicate AppImage desktop launcher | Korg1ch | +61/−18 |
| [#3654](https://github.com/storytold/photocraft/pull/3654) | PSD: don't preallocate knots from untrusted path length counts | vangel76 | +15/−1 |
| [#3722](https://github.com/storytold/photocraft/pull/3722) | Codecs: decode only the requested EXR part | vangel76 | +61/−16 |
| [#3725](https://github.com/storytold/photocraft/pull/3725) | Photoshop tool keys (arrows turn brush, Shift-click type, Space+F) | FinnNk | +185/−6 |
| [#3727](https://github.com/storytold/photocraft/pull/3727) | Codecs: decode JPEG/CCITT G3/G4 TIFF | vangel76 | +56/−1 |
| [#3785](https://github.com/storytold/photocraft/pull/3785) | Drag a document tab off the strip to float its window | bommerts | +189/−31 |
| [#3794](https://github.com/storytold/photocraft/pull/3794) | Release workflow: pass the Azure signing secrets | echelon | +6/−0 |
| [#3808](https://github.com/storytold/photocraft/pull/3808) | Remove tool: new layer per stroke toggles | diegochagas | +414/−19 |
| [#3809](https://github.com/storytold/photocraft/pull/3809) | i18n(tr): Turkish UI translation catalog | yeniufuklar-com | +3800/−3 |
| [#3831](https://github.com/storytold/photocraft/pull/3831) | i18n: Hungarian (hu) UI translation | Skaywalker | +4006/−5 |
| [#3869](https://github.com/storytold/photocraft/pull/3869) | fix(io): preserve indexed BMP color tables | Sir-Starch | +67/−2 |
| [#3871](https://github.com/storytold/photocraft/pull/3871) | Alt+Cancel → Reset for opt-in command dialogs | seandellis | +646/−54 |
| [#3886](https://github.com/storytold/photocraft/pull/3886) | Merged/stamped layers keep content bounds in CMYK and Lab | dgliwa | +185/−1 |
| [#3887](https://github.com/storytold/photocraft/pull/3887) | Preserve surviving channel targets and visibility on deletion | jonathanwxh-cell | +54/−0 |
| [#3888](https://github.com/storytold/photocraft/pull/3888) | Layers: Merge Group for a selected group | FredApps | +135/−0 |
| [#3890](https://github.com/storytold/photocraft/pull/3890) | test(cms): validate profile-specific CMYK endpoints | FredApps | +68/−1 |
| [#3894](https://github.com/storytold/photocraft/pull/3894) | Count video footage in history memory budgets | jonathanwxh-cell | +90/−0 |
| [#3895](https://github.com/storytold/photocraft/pull/3895) | Mix filtered selection edges with premultiplied alpha | jonathanwxh-cell | +139/−25 |
| [#3900](https://github.com/storytold/photocraft/pull/3900) | Color: convert input-only embedded profiles on open | HEOJUNFO | +66/−3 |
| [#3909](https://github.com/storytold/photocraft/pull/3909) | Layer › Export As exports every selected layer/artboard | fabianghe | +111/−10 |
| [#3973](https://github.com/storytold/photocraft/pull/3973) | Verify PngSuite archives and cached corpus files | zenjabba | +696/−24 |
| [#4147](https://github.com/storytold/photocraft/pull/4147) | Fix main: wasm size cap, Windows Export As test, filter preview crash, CLI font warnings | echelon | +79/−6 |
| [#4253](https://github.com/storytold/photocraft/pull/4253) | Web: wasm back under the 24 MiB gate with ~1 MiB headroom (25.38 → 24.17 MB) | bommerts | +304/−51 |

Both repos also merged the identical release-workflow PR ("pass the Azure signing
secrets", fc #1169 / pc #3794, author echelon) in the same hour — a visible same-day
cross-repo convention sync.

## 2. Adoptable / shareable findings

These are patterns, fixes, helpers and conventions observed in one repo's last-24h
activity that the other could adopt, or that both share and could consolidate.

### 2.1 Verified by direct file reading

- **Shared credits/contributors build pipeline (dup candidate #1, VERIFIED).**
  `fc/crates/ui-egui/build.rs:11` vs `pc/crates/ui-egui/build.rs:16+147`: filmcraft's file
  is 102 lines, photocraft's 225; the shared core — reading craft-fonts/credits input,
  `name()`/`s()`/`n()` normalization, `rows()` assembly, `generate()` — is identical in
  both, while photocraft adds `pack_catalogs()` (i18n tsv packing) and
  `deflate_egui_fonts()`. A shared build-helper crate would eliminate the double
  maintenance and let filmcraft inherit pc #4253's packing/deflation for free.
- **Identical i18n catalog parser (dup #5, VERIFIED).**
  `fc/crates/ui-egui/src/i18n/catalog.rs:12` vs `pc/crates/ui-egui/src/i18n/catalog.rs:16`:
  `parse_entries()` and the Entry/placeholder logic are identical; photocraft extends the
  `Catalog` with `@id` and `@plural` maps (used by pc #3831's Hungarian catalog with
  `plural_none`) while filmcraft keeps plain + contextual entries only. The additive
  divergence means filmcraft can adopt pc's catalog wholesale and gain plural support.
- **Identical CommandSpec + cmd! macro in both engines (dup #7, VERIFIED).**
  `fc/crates/engine/src/commands.rs:19` vs `pc/crates/engine/src/commands.rs:11+127`: the
  `CommandSpec` struct (id/label/menu/shortcut/params/enabled/run/journal) and the `cmd!`
  declaration macro are field-for-field the same. Any spec-level improvement (e.g. the
  enablement wiring fc #1129 just fixed) lands twice today.
- **Same craft-fonts protocol in both text crates (dup #6 + #10, VERIFIED).**
  `fc/crates/text/build.rs:23/44/53` vs `pc/crates/text/build.rs:28/62`, and
  `fc/crates/text/src/fonts.rs:28` vs `pc/crates/text/src/craft_fonts.rs:9` — the same
  `CRAFT_FONTS_DIR` / `fonts/manifest.txt` (" | " separated) build protocol and the same
  `CraftFont` struct + doc comment. Divergence: filmcraft embeds BIZ UDPGothic on wasm32,
  photocraft embeds no fonts on wasm (see #4253's size gate). A shared craft-fonts
  build/input crate would keep the protocol from drifting.
- **gpu `tex_entry()` helper (dup #8, VERIFIED).**
  `fc/crates/gpu/src/lib.rs:96` vs `pc/crates/gpu/src/lib.rs:448`: byte-identical wgpu
  `BindGroupLayoutEntry` boilerplate helper (field order only). A small shared
  gpu-common crate or vendored snippet would do; low urgency.
- **geom `Affine` — same math, divergent storage (dup #9, VERIFIED).**
  `fc/crates/geom/src/lib.rs:95,133` vs `pc/crates/geom/src/lib.rs:140,176`: identical
  2D affine semantics and identical determinant/inverse math (both use the 1e-12
  epsilon), but filmcraft stores named fields `{a..f}` while photocraft stores
  `[f64;6]` and derives `Serialize/Deserialize`. Consolidation would force one
  representation; the serialization boundary is the blocker to check first.
- **Per-frame sequence copying / transcript caching (fc #1193, deep-read).**
  fc #1193 removes per-frame deep copies of the active sequence in Timeline, Effect
  Controls, Markers, Captions and mixers by borrowing from an immutable shared project
  snapshot, and adds a transcript cache keyed on (project, sequence, query). If
  photocraft's layer/document UI keeps mutable per-frame copies of document state for
  redraw, the same borrowing pattern applies.

### 2.2 Observed in PR metadata (not deep-read)

- **wasm size gate discipline (pc #4253 + #4147, pc-side).** pc now measures the
  trunk/wasm-opt build against a 24 MiB gate and landed ~1 MiB headroom via: deflating
  egui's default fonts (from `epaint_default_fonts` as a build-dep, no font files
  committed), storing i18n English keys once + deflated catalogs, and `opt-level "z"`
  for workspace crates. filmcraft runs a 48-crate WASM check (fc #1193 body) but shows
  no equivalent gate in this window; pc's approach ports directly, especially since the
  two ui-egui build.rs files are already near-identical (§2.1).
- **i18n translation + coverage-gate convention (pc #3809, #3831).** Both repos ship
  per-language `.tsv` catalogs; pc adds a complete-language registration step, a
  clean-room attestation in the PR body, and an `xtask/src/i18n_coverage.rs` gate. The
  identical catalog parser (§2.1) makes this convention directly shareable — filmcraft
  just added ja UI labels in #1168/#1159 the same day.
- **Untrusted-input hardening in file decoders (pc #3484, #3501, #3654; fc #837/#879/#1068 are the import side).**
  pc spent the window bounds-checking pattern sizes, ZIP reads and PSD path counts from
  untrusted files; fc spent it adding EXR/DNG/HEVC importers. fc's new decoders should
  get the same untrusted-count treatment before pattern-size and blob-length classes of
  bug appear there.
- **History/memory budget accounting (pc #3614, #3894).** Selection masks and video
  footage now count toward history memory budgets; if fc's undo system has a budget, the
  same accounting (media-heavy objects first) applies.
- **Dialog window behavior (fc #1217).** fc made dialogs draggable by title bar and
  open-centred; pc #3785 made document tabs floatable. Different features, but both
  touch window/dialog management in the shared egui shell — worth watching for
  convergence.
- **Same-day release-workflow sync (fc #1169 = pc #3794).** Already synced; listed as
  evidence the repos do copy each other's infra changes quickly.

## 3. Verified duplicate-code candidates

Method reminder: `craft-helpers dups` was run once per crate pair with `--cross-only`
(one invocation per shared crate), ranked by repeated lines; each top candidate got
exactly one read of both sides. Everything below marked VERIFIED was read; the rest is
helper output only.

| # | Lines | filmcraft side | photocraft side | Reading |
|---|---|---|---|---|
| 1 | 82 | `crates/ui-egui/build.rs:11` | `crates/ui-egui/build.rs:16` | VERIFIED — identical credits/credits-baking core; pc adds pack_catalogs() + deflate_egui_fonts() |
| 2 | 61 | `crates/ui-egui/src/credits.rs:150` | `crates/ui-egui/src/credits.rs:163` | VERIFIED — identical compare()/dated()/sorted()/group()/signed()/day() helper formatting; pc wraps the row in a `tl!()` i18n template |
| 3 | 59 | `crates/ui-egui/src/credits.rs:351` | `crates/ui-egui/src/credits.rs:546` | VERIFIED — same region as #2, same family |
| 4 | 30 | `crates/ui-egui/src/credits.rs:57-140` | `crates/ui-egui/src/credits.rs:50-146` | VERIFIED — SortKey/NameMode enums, ALL consts, `default_ascending`, `name()`, `lines_delta()` identical; pc labels via `tl!()` |
| 5 | 44 | `crates/ui-egui/src/i18n/catalog.rs:12` | `crates/ui-egui/src/i18n/catalog.rs:16` | VERIFIED — parse_entries() + Entry/placeholder identical; pc extends with @id/@plural (additive) |
| 6 | 24 | `crates/text/build.rs:23/44/53` | `crates/text/build.rs:28/62` | VERIFIED — same craft-fonts manifest parser + env protocol; fc embeds BIZ UDPGothic on wasm32, pc embeds none on wasm |
| 7 | 17 | `crates/engine/src/commands.rs:19` | `crates/engine/src/commands.rs:11,127` | VERIFIED — CommandSpec + cmd! identical field-for-field |
| 8 | 25 | `crates/ui-egui/src/lib.rs:1603,1624` | `crates/ui-egui/src/lib.rs:1501` | VERIFIED — same command-wiring block (`s.edit(label, |pr, _| …)` wrappers) around settings/menu handlers |
| 9 | 24 | `crates/gpu/src/lib.rs:96` (+fx.rs:272) | `crates/gpu/src/lib.rs:448` | VERIFIED — tex_entry() byte-identical (field order only) |
| 10 | 9 | `crates/geom/src/lib.rs:95,133` | `crates/geom/src/lib.rs:140,176` | VERIFIED — Affine: same math/inverse/epsilon, divergent storage (named fields vs [f64;6] + serde) |
| 11 | 7 | `crates/text/src/fonts.rs:28` | `crates/text/src/craft_fonts.rs:9` | VERIFIED — CraftFont struct + doc comment identical |
| 12 | 8 | `crates/automation/src/server.rs:39` | `crates/automation/src/server.rs:200` | VERIFIED — ListParams near-identical (pc adds `deny_unknown_fields`); similar-but-low-value |
| 13 | 6 | `crates/automation/src/server.rs:241` | `crates/automation/src/server/transport.rs:65` | VERIFIED — stdio transport loop same shape; fc orders err_rx first, pc uses `biased;` with error first — a real micro-divergence |
| 14 | 9 | `crates/geom/src/polygon.rs:12` (helper ref) | — | REJECTED — `src/polygon.rs` does not exist in fc HEAD; stale/unmatched helper reference, one attempt, moved on |

Unverified remainder (helper output, not verified): the remaining cross candidates in
cross-text (fonts.rs:400/548, :120/580, :412/560), cross-color
(`fc/crates/color/src/lib.rs:176` vs `pc/crates/color/src/convert.rs:146`), and the
long tail of ≤6-line matches in every crate pair. The repo-wide `dups` scan also
returned candidates from the first tree only (its normal window behavior; the filmcraft
side of repo-wide non-cross duplicates was not enumerated by the helper and is therefore
not claimed).

## 4. Recommendations

1. **Extract a shared ui-egui build/credits/i18n crate first.** Dup candidates #1–#5 and
   the packed-catalog logic (pc #4253) are one coherent unit — identical code that pc has
   already extended. filmcraft inherits wasm savings + plural support by adopting it.
2. **Fence the craft-fonts protocol.** Dup #6/#11: one crate owning the manifest parser +
   CraftFont struct removes the drift risk between the two build.rs files (they already
   diverge on wasm embedding).
3. **Port the wasm size gate to filmcraft.** pc #4253's gate + deflation pattern is the
   direct model; fc's 48-crate wasm check exists but no size gate appears in this window
   (unverified — fc-side CI not inspected).
4. **Give fc's new decoders pc's untrusted-input treatment** (§2.2): bounds-check counts
   and sizes before the pattern-size/blob-length bug classes arrive.
5. **Watch the Affine consolidation (dup #10) but don't force it:** the math is already
   identical; the blocker is the serde boundary on pc's side, so pick the storage
   representation before extracting a shared geom crate.
6. **Adopt pc's i18n coverage-gate convention in fc** (xtask-based completeness check)
   before the next fc language lands — the parser being identical (dup #5) makes the
   gate a drop-in.

## Appendix — method + caveats

- PR list: `craft-helpers prs --org storytold --repos photocraft,filmcraft --since 24h --json`,
  50 PRs, no `truncated` marker. Raw JSON kept in `$RUNNER_TEMP/prs.json`.
- Duplicates: `craft-helpers dups --roots pc,fc --min-lines 6 --json` once (repo-wide;
  first-tree window as documented), then one `--cross-only` invocation per shared crate
  (7 crates), `--max-candidates 500`, ranked by repeated lines. No re-runs, no flag tuning.
- Deep-inspected PRs (cap 3): pc #4253, fc #1193, pc #3831 (`gh pr view`, read-only).
  Every other PR's line comes from the prs JSON alone.
- Not verified: fc-side CI workflows, any repo not listed, and all candidates in the
  unverified remainder. The filmcraft merged-PR window is complete only if fc merged ≤30
  PRs in 24 h (helper cap); nothing suggests otherwise.
- No claims in this report extend beyond helper output, file reads at fc/pc HEAD
  (shallow clones, 2026-10-12), and the three deep-read PR bodies.
