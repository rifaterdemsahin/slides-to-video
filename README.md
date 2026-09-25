# 🎬 slides-to-video

**Google's new video *document* type — a fully narrated, captioned and scored video built from a 🧠 Gemini conversation and a 🎨 Google Slides deck, without touching an editor.**

📺 **Live:** https://rifaterdemsahin.github.io/slides-to-video/

---

## 📦 What this repository contains

| Page | What it is |
|---|---|
| 🎬 [`index.html`](index.html) | **The video** — the 10-scene storyboard, Google Vids feature breakdown, publish-to-Skool guide |
| 📹 [`how-to-google-vids.html`](how-to-google-vids.html) | **How to use Google Vids** — step-by-step walkthrough grounded in the real UI, plus a verified YouTube watch list |
| 💰 [`costs.html`](costs.html) | **The Cost Ledger** — recurring agent API burn vs the one-off production spend of the video |
| 🎥 [`scaling-ai-agents-chief-of-staff-and-cost-governance.mp4`](scaling-ai-agents-chief-of-staff-and-cost-governance.mp4) | The exported video — 1920×1080, 30 fps, 2 min 10 s, 3.8 MB, H.264 + AAC stereo |

🔗 Pages: [🎬 video](https://rifaterdemsahin.github.io/slides-to-video/) · [📹 how-to](https://rifaterdemsahin.github.io/slides-to-video/how-to-google-vids.html) · [💰 costs](https://rifaterdemsahin.github.io/slides-to-video/costs.html)

## 🎥 The video

**🚀 Scaling AI Agents: Chief of Staff & Cost Governance** — *⚙️ Bulk orchestration via Chief of Staff and cost-governed human oversight.*

Ten scenes arguing one position: you can let a fleet of agents run unsupervised, but not unverified. A single **Chief of Staff** agent receives a unified spec and provisions five specialist workers in parallel — prospecting, outreach, engagement, human gate — while API spend is held down by keeping deterministic work on rules and reserving generative calls for real reasoning.

The two rules the film ends on:

> 💸 Do not spend API dollars on predictable logic.

> 🔒 Do not spend API dollars on unreviewed output.

## 📹 How to use Google Vids

A click-path walkthrough — create the doc, import a deck as scenes, AI-narrate each scene, score it and run **Balance sound**, switch captions on, revise with **Reimagine your video**, export MP4. Includes a map of the real menu bar and media tray (📁 File / 🎞️ Scene / ▶️ Play / ✨ AI video / 🎙️ Voiceover / 🎚️ Balance sound), the seven gotchas, and the pricing reality: **Vids ships inside paid Google Workspace, it is not a free standalone tool**.

**🎥 Watch list — 19 embedded videos, every one verified.** Grouped into 📹 official intro, 🛠️ full tutorials, ⚙️ multi-agent orchestration, and 💰 token economics. Each was confirmed to exist *and* permit embedding via YouTube's oEmbed API before being placed on the page — titles, channels and durations read back from source, not copied from search results. Thumbnails are click-to-play (a facade swaps in the `youtube-nocookie` iframe on demand), so the page loads without 19 iframes and the links still work with JavaScript disabled.

## 🧭 How the video was made

Four moves. 🚫📷 No camera, 🚫✂️ no editor, 🚫🎞️ no timeline software.

```
1. 🧠 GEMINI       raw dictated brain-dump  →  "rewrite this in a presentation form"
                                              →  slide-shaped script
2. 🎨 SLIDES       16:9 dark deck, one visual language
3. 🎬 GOOGLE VIDS  import deck → scenes → AI voiceover + music + captions → balance sound
4. 🚀 EXPORT       MP4 → commit → GitHub Pages
```

**1. 🧠 Create the script with Gemini.** Dictate the idea as if explaining it to a colleague — real numbers, real objections — then ask for it in presentation form.
↳ 🔗 [source conversation](https://gemini.google.com/share/d/1AXSsTFxFefXaasYa4QUk_aoN_-uHKR_5)

**2. 🎨 Design the deck — Google Slides, 16:9.** That aspect ratio becomes the video frame, so it must be set here. Hold one visual language across every slide: monospace all-caps eyebrow, heavy white title, grey one-line deck, and a 🔵🔴 blue + red two-bar accent.
↳ 🔗 [source deck](https://docs.google.com/presentation/d/1LxohuJdkUOFROYpKfol89acD-YIetO_Xwq0KiUtpcFo/edit)

**3. 🎬 Assemble the video in Google Vids.** Each slide becomes a timed scene. Add 🎙️ AI voiceover, a 🎵 licensed music bed, 💬 captions, then *Improve sound quality → 🎚️ Balance sound*.
↳ 🔗 [Vids document](https://docs.google.com/videos/d/1AWB8ILIC7G9ZK4cJNznjJeK7Tn_sBF7gsOlEwxm1IGs/edit)

**4. 🚀 Export, then publish.** MP4 → commit → GitHub Pages → paste the storyboard into Skool as a classroom lesson.

### 🛠️ What Google Vids actually is

A Workspace **document** type, not a Drive video. 📍 `docs.google.com/videos/<id>`. The scene timeline *is* the document body; the media tray is the toolbar — ✨ AI video, 🧑‍💼 avatar, 🎙️ voiceover, 🎵 music, 🖼️ image, ⏺️ record, 📤 uploads, 📚 stock, 💬 captions, 🔤 text, 🧩 templates, 🔷 shapes, plus **🪄 Reimagine your video**. Because it imports Slides natively and exports a plain MP4, it drops into a pipeline that already starts in Docs or Slides.

## 💰 The cost ledger

Two columns that must never be confused.

- 💸 **Column A — recurring burn.** Per-token API calls, per agent, per day. Compounds with headcount, and never arrives as a decision anyone approved. This is the column the **$20 → $100+** curve lives in.
- 🎬 **Column B — one-off production.** One Workspace seat, Gemini free tier, GitHub Pages free. No editor, no studio, no separately-bought music licence. **0 timeline hours.**

Includes guardrail levers, a budget-sheet template, and a provenance block naming what is verified versus what is not. **No per-token rates are published** — rates move per model, provider and region, and a stale rate on a cost page is worse than a blank cell.

## 📣 Publishing to Skool

Destination: the **Delivery Pilot** community classroom — the Step 0 → Step 9 course ladder. This belongs with the **Hands-On DO Sessions → Advanced** track, as a sibling lesson to the existing *🎬 GrokBot Chief Of Staff* lesson.

1. ✅ Publish the GitHub Pages URL first; paste *that* link into Skool so the lesson body stays short and the canonical version lives at one stable URL.
2. 🛠️ Admin tools → Classroom → **Hands-On DO Sessions** → **Add lesson**.
3. 🏷️ Title: *Scaling AI Agents — Bulk Provisioning via Chief of Staff*.
4. 📝 Body: paste the 10-scene storyboard table from `index.html` — Skool lessons are markdown (the lesson URL carries it as `?md=<hash>`).
5. 📎 Attach the MP4. Post a short community announcement pointing at the lesson.

💸 Lead with the cost curve (**$20 → $100+**) — the constraint the audience has already felt — then present the deterministic/generative split as the fix.

---

✍️ *Rifat Erdem Sahin — built with 🧠 Gemini + 🎬 Google Vids.*
