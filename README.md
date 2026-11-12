# Etsy HyperFrames Video

An installable Agent Skill for the complete Etsy product-video workflow: listing and SKU research, buyer-focused narration, faithful image preparation, TTS, HyperFrames motion design, and final quality review.

## Install in Codex

In Codex, use the built-in `$skill-installer` and provide this skill folder:

`https://github.com/haitao338241-collab/etsy-hyperframes-video-skill/tree/main/skills/etsy-hyperframes-video`

Or download the repository ZIP, then copy `skills/etsy-hyperframes-video` into your Codex skills directory (normally `~/.codex/skills/etsy-hyperframes-video`). Restart or start a new Codex conversation so the skill is discovered.

## Adapt it to your setup

This public package contains no personal paths, TTS endpoints, tokens, cookies, or voice-model settings. Copy `references/local-profile.template.md` to `references/local-profile.local.md` on your own machine and fill in your project folder and approved TTS defaults. Keep that `.local.md` file private. HyperFrames and a compatible TTS route are needed to produce a rendered, narrated video; the skill uses other installed browser/media skills when available.

## Files

- `skills/etsy-hyperframes-video/SKILL.md` — skill entry point and production sequence.
- `skills/etsy-hyperframes-video/references/production-workflow.md` — detailed research, writing, art direction, TTS, rendering, and review checklist.
- `skills/etsy-hyperframes-video/references/local-profile.template.md` — private setup template.

## English

This skill turns a specific Etsy listing into a fact-checked, buyer-focused product video. It checks variations and SKU logic, writes natural narration, protects product details during image edits, uses varied focal-point-aware motion, and reviews the final rendered file. It does not publish to social accounts unless the user explicitly requests publication.
