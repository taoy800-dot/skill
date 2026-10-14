---
name: pyvideotrans
description: Help use the pyVideoTrans application for video/audio transcription, subtitle translation, dubbing, and end-to-end video translation. Use when the user asks to process media with pyVideoTrans or run one of its documented CLI tasks.
---

# pyVideoTrans

Use pyVideoTrans as the user's local video translation and dubbing tool. This Skill is a Codex usage guide; it does not install or bundle the pyVideoTrans application.

## Workflow

1. Identify the requested operation and media path. Map it to the documented task: `stt` for speech-to-subtitles, `sts` for subtitle translation, `tts` for voice generation from subtitles, or `vtv` for the full video translation workflow.
2. Check only the installation path the user supplied or a likely, specific location. Confirm the CLI entry point (`cli.py` in a source checkout or the packaged CLI executable) and its runtime before invoking it. If pyVideoTrans is not installed, explain the official install options instead of silently installing dependencies or downloading models.
3. Read [official CLI notes](references/official-cli.md) and the linked current upstream CLI guide before choosing arguments. Use the installed version's `--help` when available; do not carry flags across versions without checking.
4. Preserve the user's requested source/target languages, voice, output location, and processing preferences. Ask for missing choices that materially affect the result. Do not select a paid API, enter credentials, or expose keys without the user's direction.
5. Quote absolute file paths, especially paths containing spaces. Prefer a new output location and avoid overwriting existing media or subtitles.
6. Run the smallest requested task, report the produced file paths, and verify that expected output files exist and are non-empty. If the app reports failure, relay the relevant error and next useful step without claiming a successful conversion.

## Boundaries

- Use only media the user is authorized to process. Do not bypass DRM, paywalls, private access, or platform restrictions.
- Do not publish or expose the local WebUI to the network. In particular, do not use a public share option when API keys or private settings could be visible.
- Installing the Skill does not install pyVideoTrans, FFmpeg, Python, `uv`, speech models, or provider credentials. Treat those as separate setup tasks.
- For exact options and version-specific behavior, prefer the official documentation linked in [official CLI notes](references/official-cli.md).
