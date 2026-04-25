---
notion_id: 336755ec-7e2c-810d-978a-fa1251b0ebec
created: 2026-04-02
date: null
platform: null
device: null
momentum: null
energy: null
tags: [LiveNotes, ScreenAnnotation, AI, Android, Kotlin, JetpackCompose]
---

# LiveNotes — Screen Annotation + AI Spark

## Session Summary

Built a live video annotation app called **LiveNotes** — a tool for annotating over live video (webcam, screen capture, or video file) with drawing tools, sticky notes, and an AI-powered **Spark** feature that converts annotated frames into interactive widgets.

## What Was Built

- **ScreenNotes v1** — static screenshot version with paste/drop support, pen/erase/note/text tools, and Spark (Claude API generates widgets from annotated screenshots)
- **LiveNotes v2** — upgraded to live video with three source modes:
  - Webcam capture
  - Screen capture  
  - Video file playback

## Android Exploration

Discovered that `getDisplayMedia` (screen capture) is **not supported on Android Chrome**, blocking the core use case of annotating over live YouTube etc.

Sketched a native Android app architecture:

- **MediaProjection API** — the unlock for screen capture on Android (what screen recorder apps use, requires foreground service + user permission prompt)
- **Camera2 API** — webcam/camera feed
- **SurfaceView** — video rendering
- **Canvas/Bitmap** — annotation layer
- **Stack:** Kotlin + Jetpack Compose + Coroutines + Retrofit
- **Spark flow:** freeze frame → composite Bitmap → encode JPEG → Anthropic API → render HTML in WebView

## Artifacts Created

- `screen-notes.jsx` — static screenshot annotation tool
- `live-notes.jsx` — live video annotation tool
- Excalidraw architecture diagram of Android app

## Next Steps (if revisiting)

- [ ] Scaffold Kotlin project with MediaProjection foreground service
- [ ] Implement Canvas overlay on SurfaceView
- [ ] Wire Spark button → Anthropic API → WebView render
- [ ] Consider deploying web version to Zo for Android browser use

---
Source: Notion Session Log (ID: 336755ec-7e2c-810d-978a-fa1251b0ebec)
Synced: 2026-04-25
