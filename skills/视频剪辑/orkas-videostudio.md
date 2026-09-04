# OrkasVideoStudio Agent Video Workflow

> Plan, compose, edit, generate, and assemble video through a local-first CLI and MCP toolkit.

## When to Use

- Use when a coding agent must deliver a finished video, not just advice.
- Use when the workflow needs an editable and reviewable `plan.json` timeline.
- Use when supplied footage needs trimming, captions, audio work, or reframing.
- Use when a brief needs deterministic motion graphics or HTML composition.
- Use when optional provider-backed footage must be combined with local editing.
- Use when the same workflow should be available through a CLI or MCP server.
- Do not use it as a claim that unpublished npm packages are available.

## Instructions for AI Assistant

1. Read the brief and identify the required duration, aspect ratio, language, and output.
2. Choose one primary route: compose, edit, generate, or an end-to-end combination.
3. Keep edit as the primary route when the request starts from supplied footage.
4. Use compose for deterministic typography, diagrams, captions, and motion graphics.
5. Use generate only when the brief genuinely needs new imagery or footage.
6. State the chosen route before editing files or spending provider credits.
7. Build a `plan.json` timeline so every segment remains editable and diffable.
8. Use the zero-key local trunk for composition, editing, and transcription where possible.
9. Ask before using a provider-backed generation step that can incur cost.
10. Render a draft, inspect it, fix concrete defects, and run the delivery checks.
11. Return the final video together with the editable plan and any caption files.

### Install from Source

The working installation path is the source repository:

```bash
git clone https://github.com/Orkas-AI/Orkas-VideoStudio.git
cd Orkas-VideoStudio
pnpm install
pnpm build
node packages/cli/dist/index.js doctor
```

For the examples below, define a shell alias after building:

```bash
alias ovs="node $PWD/packages/cli/dist/index.js"
ovs doctor
```

## Templates

### Template 1: Inspect and trim supplied footage

```bash
ovs edit probe input.mp4
ovs edit trim input.mp4 --start 3 --end 28 --out trimmed.mp4
ovs quality trimmed.mp4
```

Use probe output to confirm streams and duration before choosing cut points.

### Template 2: Create captions from local media

```bash
ovs transcribe interview.mp4 --out transcript.json
ovs edit burnsubs interview.mp4 --srt subtitles.srt --out captioned.mp4
ovs quality captioned.mp4
```

Review names, numbers, timing, and line breaks before burning captions.

### Template 3: Validate an editable production plan

```bash
ovs plan validate plan.json
ovs plan summarize plan.json
ovs plan promise-check plan.json
```

The validation step checks structure; the promise check verifies the planned output still matches the brief.

### Template 4: Draft before final delivery

```bash
ovs draft composition --out draft.mp4 --report draft-report.json
ovs quality draft.mp4
ovs render composition --out final.mp4
```

Inspect the draft at representative frames before starting the final render.

## Common Patterns

### Compose-first explainer

1. Convert the brief into timed scenes.
2. Build deterministic HTML composition assets.
3. Keep visible copy concise and inside safe areas.
4. Add narration and captions against the same timing plan.
5. Render a draft and inspect transitions and text legibility.

### Source-led edit

1. Probe every source clip.
2. Preserve the requested content and speaker intent.
3. Remove only approved dead space or filler material.
4. Add captions, loudness normalization, and reframing as separate operations.
5. Keep an evidence trail for cut decisions.

### Hybrid end-to-end production

1. Name the dominant route in the delivery promise.
2. Put all compose, edit, and generate segments in one `plan.json`.
3. Generate only the shots that cannot be made deterministically.
4. Assemble the segments in timeline order.
5. Run the promise check before delivery.

## Pitfalls to Avoid

| Pitfall | Why It's Bad | Solution |
|---------|--------------|----------|
| Switching routes silently | The output can drift from the approved brief | State and lock the primary route before production |
| Treating supplied footage as disposable | Regeneration can replace material the user wanted preserved | Keep the job edit-first and define preservation boundaries |
| Claiming npm installation works now | The packages are still being published | Use the documented source-install path |
| Spending provider credits implicitly | Generation may create unapproved cost | Confirm provider-backed steps before execution |
| Delivering only a rendered file | The production becomes hard to revise | Include `plan.json`, captions, and source references |
| Skipping draft inspection | Timing and readability defects reach the final render | Inspect frames and run quality checks before delivery |
| Hiding failed checks | Reviewers cannot tell whether the result is trustworthy | Report failed checks and remaining limitations clearly |

## Quality Checklist

- [ ] The primary route is explicit.
- [ ] The timeline validates.
- [ ] Source media boundaries are preserved.
- [ ] Captions match the spoken content.
- [ ] Text stays within safe areas.
- [ ] Audio levels are consistent.
- [ ] The draft was visually inspected.
- [ ] The delivery promise passes.
- [ ] The final file plays from start to finish.
- [ ] Editable artifacts are included.

## Source and License

Adapted from the OrkasVideoStudio `video-router` workflow at immutable commit
[`d5197ab5e625fc44ab719a940711d82b46c16ef5`](https://github.com/Orkas-AI/Orkas-VideoStudio/tree/d5197ab5e625fc44ab719a940711d82b46c16ef5/packages/skills/video-router).
OrkasVideoStudio and this adaptation are available under the MIT License.
