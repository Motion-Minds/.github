<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Motion-Minds/.github/main/profile/assets/motionmind-horizontal-on-dark.svg">
  <img src="https://raw.githubusercontent.com/Motion-Minds/.github/main/profile/assets/motionmind-horizontal.svg" alt="MotionMind" width="320">
</picture>

### Make videos with your AI agent. Every version tracked.

An open-source agent skill, CLI and local Studio for making HyperFrames videos with the AI coding agent you already use.

[![npm](https://img.shields.io/npm/v/motionmind?color=c9f24d&labelColor=0e0f11&style=flat-square)](https://www.npmjs.com/package/motionmind)
[![License: MIT](https://img.shields.io/badge/license-MIT-c9f24d?style=flat-square&labelColor=0e0f11)](https://github.com/Motion-Minds/motionmind-video/blob/main/LICENSE)
[![Format: Agent Skills](https://img.shields.io/badge/format-Agent%20Skills-c9f24d?style=flat-square&labelColor=0e0f11)](https://github.com/Motion-Minds/motionmind-video#install)
[![Engine: HyperFrames](https://img.shields.io/badge/engine-HyperFrames-c9f24d?style=flat-square&labelColor=0e0f11)](https://github.com/heygen-com/hyperframes)

[Website](https://motionmind.dev) · [Repository](https://github.com/Motion-Minds/motionmind-video) · [Documentation](https://github.com/Motion-Minds/motionmind-video#readme) · [npm](https://www.npmjs.com/package/motionmind) · [Report an issue](https://github.com/Motion-Minds/motionmind-video/issues)

<img src="https://raw.githubusercontent.com/Motion-Minds/motionmind-video/main/docs/gallery/walkthrough.gif" alt="30-second walkthrough: install and setup, brief the agent and pick a concept, approve the storyboard, the agent builds, checks and renders, then review, compare and promote in MotionMind Studio" width="100%">

<sub>30-second walkthrough, made with MotionMind itself.</sub>

</div>

## Why MotionMind

AI agents can already write a motion graphic. What goes wrong is everything around it: the agent skips straight to code, a "small change" overwrites the version the client approved, nobody knows which render was the good one, the audio sits at a random level, and the next chat starts from zero.

MotionMind gives the agent a **production process** and gives you a **record of it**. The agent works like a studio (concepts, storyboard, build, review, render) and stops for your approval at each step. Every render becomes a frozen, measured version that you can compare, edit without code in HyperFrames Studio, and promote to production.

## What's inside

One npm package, [`motionmind`](https://www.npmjs.com/package/motionmind), with four parts. The agent uses all of them, and so can you.

| Part | What it does |
|---|---|
| **The `motionmind` skill** | Four-gate workflow, HyperFrames rules, motion and sound guidance and a QA checklist. Works with any agent that reads `SKILL.md`: Claude Code, Codex, Gemini CLI, OpenCode and others. |
| **The `motionmind` CLI** | `setup`, `init`, `render`, `log`, `compare`, `promote`, `track`, `music`, `sfx`, `doctor`. The agent calls it; you can too. |
| **A local Studio** | `motionmind ui` opens a dashboard on `127.0.0.1`, like MLflow for renders. Every version has a player, a 4:5 safe-area overlay, a contact sheet, loudness, side-by-side compare and a one-click promote. |
| **Music and SFX** | Deterministic 120 BPM music beds generated from code, plus 22 CC0 sounds: clicks, pops, chimes, whooshes, risers, impacts. |

Every version is a HyperFrames project (HTML + GSAP) rendered to an H.264 MP4, so it can be reopened, edited visually and re-rendered identically later. Already working in HyperFrames Studio, Premiere or CapCut? `motionmind track` logs every render or export as a version.

## How it works

1. **Brief, then pick a concept.** Describe the product, format, length and call to action. The agent writes two or three genuinely different concepts, and you pick one.
2. **Approve the storyboard.** A per-second table, with the style locked in `TASTE.md` (palette, type, easing, music) so later versions look and move the same.
3. **The agent builds and renders.** One scene per file. The agent runs HyperFrames `check` and `snapshot` after every change and looks at the frames itself.
4. **Review and promote.** Watch it in the Studio or edit it in HyperFrames Studio. After QA (−14 LUFS, true peak ≤ −1 dBFS, phone safe area), promote it to production. The previous production version is archived, never deleted.

## Quick start

Requirements: Node.js 22+, `ffmpeg` and `ffprobe` on `PATH`, and an agent CLI. HyperFrames and its headless Chrome are fetched on first use.

```bash
npm i -g motionmind
motionmind setup my-studio   # workspace + the motionmind skill + the official HyperFrames skills
cd my-studio
motionmind doctor            # checks Node, ffmpeg, Chrome, HyperFrames, the skill and your agent CLI
motionmind ui                # Studio at http://127.0.0.1:4310
```

Then, in a second terminal in the same folder, start your agent and brief it:

```text
Use the motionmind skill. I want a 15-second 9:16 promo for my coffee shop "Kopi Senja",
message "great coffee, friendly prices", CTA kopisenja.id, music + SFX, no voice-over.
```

## Who it's for

- **Content creators:** promos and reels with text inside the phone safe area and audio at a measured level.
- **Agencies and marketing teams:** the version the client approved is never overwritten. Compare v1 and v2, then promote the one that wins.
- **Developers and AI agent users:** the skill is a plain Agent Skills folder and the CLI works from any agent, with whichever model you prefer.
- **Video editors:** keep your own editor and let MotionMind keep the record.

## Repositories

| Repository | What it is |
|---|---|
| [**motionmind-video**](https://github.com/Motion-Minds/motionmind-video) | The open-source package: agent skill, CLI and Studio. Published to npm as `motionmind`. MIT licensed. |

## Contributing and security

- Bugs and feature requests: [open an issue](https://github.com/Motion-Minds/motionmind-video/issues).
- Security problems: please don't open a public issue. Report them privately via **Security → Report a vulnerability** on [motionmind-video](https://github.com/Motion-Minds/motionmind-video/security).

## License

MotionMind is [MIT licensed](https://github.com/Motion-Minds/motionmind-video/blob/main/LICENSE). The MotionMind name and logo are not covered by the MIT licence.

HyperFrames and HeyGen are trademarks of HeyGen. MotionMind is not affiliated with HeyGen. HyperFrames is licensed under Apache 2.0.
