# pyVideoTrans official CLI references

Use these upstream references for command syntax and requirements; they can change between releases.

- Repository: https://github.com/jianchang512/pyvideotrans
- CLI user guide: https://pyvideotrans.com/cli
- Installation and desktop/WebUI guide: https://pyvideotrans.com/
- Windows releases: https://github.com/jianchang512/pyvideotrans/releases

## Task mapping

The current CLI guide documents four task types:

| Task | Purpose |
| --- | --- |
| `stt` | Speech recognition and SRT subtitle generation |
| `tts` | Generate speech from text/subtitles |
| `sts` | Translate subtitles |
| `vtv` | Full video translation, dubbing, and synthesis |

The source-install examples use `uv run cli.py`. A sample documented STT invocation is:

```powershell
uv run cli.py --task stt --name "D:\videos\demo.mp4" --detect_language zh-cn --cuda
```

Check the installed version's `--help` and the current CLI guide before using optional flags. TTS voices depend on the selected provider and target language; do not invent a voice identifier. Source deployment requires `uv` and FFmpeg; the packaged Windows release has its own bundled requirements. Do not install dependencies, models, or providers unless the user requests that setup.
