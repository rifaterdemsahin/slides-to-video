# 🎬 slides-to-video

**Google's new video *document* type — a fully narrated, captioned and scored video built from a 🧠 Gemini conversation and a 🎨 Google Slides deck, without touching an editor.**

📺 **Live:** https://rifaterdemsahin.github.io/slides-to-video/
💰 **Cost breakdown:** https://rifaterdemsahin.github.io/slides-to-video/costs.html

---

## 📦 What this repository contains

| File | What it is |
|---|---|
| 🎬 [`index.html`](index.html) | One-page site — the video, the 10-scene storyboard, Google Vids feature breakdown, publish-to-Skool guide |
| 💰 [`costs.html`](costs.html) | **The Cost Ledger** — recurring agent API burn vs the one-off production spend of the video |
| 📹 [`scaling-ai-agents-chief-of-staff-and-cost-governance.mp4`](scaling-ai-agents-chief-of-staff-and-cost-governance.mp4) | The exported video — 1920×1080, 30 fps, 2 min 10 s, 3.8 MB, H.264 + AAC stereo |

## 🎥 The video

**🚀 Scaling AI Agents: Chief of Staff & Cost Governance** — *⚙️ Bulk orchestration via Chief of Staff and cost-governed human oversight.*

Ten scenes arguing one position: you can let a fleet of agents run unsupervised, but not unverified. A single **Chief of Staff** agent receives a unified spec and provisions five specialist workers in parallel — prospecting, outreach, engagement, human gate — while API spend is held down by keeping deterministic work on rules and reserving generative calls for real reasoning.

The two rules the film ends on:

> 💸 Do not spend API dollars on predictable logic.

> 🔒 Do not spend API dollars on unreviewed output.

## 🧭 How it was made

Four moves. 🚫📷 No camera, 🚫✂️ no editor, 🚫🎞️ no timeline software.

```
1. 🧠 GEMINI       raw dictated brain-dump  →  "rewrite this in a presentation form"
                                              →  slide-shaped script
2. 🎨 SLIDES       16:9 dark deck, one visual language
3. 🎬 GOOGLE VIDS  import deck → scenes → AI voiceover + music + captions → balance sound
4. 🚀 EXPORT       MP4 → commit → GitHub Pages
```

**1. 🧠 Create the script with Gemini.** Dictate the idea as if explaining it to a colleague — real numbers, real objections — then ask for it in presentation form. Gemini turns the rambling transcript into a title, a subtitle and 3–4 bolded points per slide.
↳ 🔗 [source conversation](https://gemini.google.com/share/d/1AXSsTFxFefXaasYa4QUk_aoN_-uHKR_5)

**2. 🎨 Design the deck — Google Slides, 16:9.** Paste the script into a **16:9** deck; that aspect ratio becomes the video frame, so it must be set here. Hold one visual language across every slide: monospace all-caps eyebrow, heavy white title, grey one-line deck, and a 🔵🔴 blue + red two-bar accent.
↳ 🔗 [source deck](https://docs.google.com/presentation/d/1LxohuJdkUOFROYpKfol89acD-YIetO_Xwq0KiUtpcFo/edit)

**3. 🎬 Assemble the video in Google Vids.** Import the deck; each slide becomes a timed scene. Add 🎙️ AI voiceover per scene, a 🎵 licensed music bed, 💬 auto-captions, then run *Improve sound quality → 🎚️ Balance sound*. You fix the video the way you edit a deck, not footage.
↳ 🔗 [Vids document](https://docs.google.com/videos/d/1AWB8ILIC7G9ZK4cJNznjJeK7Tn_sBF7gsOlEwxm1IGs/edit)

**4. 🚀 Export, then publish.** Export MP4 → commit → serve from GitHub Pages → paste the storyboard into Skool as a classroom lesson.

### 🛠️ What Google Vids actually is

A Workspace **document** type, not a Drive video. 📍 It lives at `docs.google.com/videos/<id>`. The scene timeline *is* the document body; the media tray is the toolbar — ✨ AI video, 🧑‍💼 avatar, 🎙️ voiceover, 🎵 music, 🖼️ image, ⏺️ record, 📤 uploads, 📚 stock, 💬 captions, 🔤 text, 🧩 templates, 🔷 shapes, plus **🪄 Reimagine your video** (describe a change in a sentence and Gemini re-cuts). Because it imports Slides natively and exports a plain MP4, it drops into a pipeline that already starts in Docs or Slides.

## 💰 The cost ledger

Two columns, and they must never be confused.

- 💸 **Column A — recurring burn.** Per-token API calls, per agent, per day. Grows with activity, compounds with headcount, and never arrives as a decision anyone approved. This is the column the **$20 → $100+** curve lives in.
- 🎬 **Column B — one-off production.** One Workspace seat (Google Vids ships *inside* paid Workspace — UK list £11.80/user/month ex-tax at time of capture), Gemini free tier, GitHub Pages free. No editor, no studio, no separately-bought music licence. **0 timeline hours.**

The page also carries the guardrail levers (route-before-prompt, context caps, model laddering, cache, retry budgets, the human gate), a budget-sheet template, and a provenance block naming what is verified versus what is not.

➡️ **[Open costs.html](costs.html)**

## 📣 Publishing to Skool

Destination: the **Delivery Pilot** community classroom — the Step 0 → Step 9 course ladder. This belongs with the **Hands-On DO Sessions → Advanced** track, as a sibling lesson to the existing *🎬 GrokBot Chief Of Staff* lesson.

1. ✅ Publish the GitHub Pages URL first; paste *that* link into Skool so the lesson body stays short and the canonical version lives at one stable URL.
2. 🛠️ Admin tools → Classroom → **Hands-On DO Sessions** → **Add lesson**.
3. 🏷️ Title: *Scaling AI Agents — Bulk Provisioning via Chief of Staff*.
4. 📝 Body: paste the 10-scene storyboard table from `index.html` — Skool lessons are markdown (the lesson URL carries it as `?md=<hash>`).
5. 📎 Attach the MP4. Post a short community announcement pointing at the lesson.

💸 Lead with the cost curve (**$20 → $100+**) — that's the constraint the audience has already felt — then present the deterministic/generative split as the fix.

---

✍️ *Rifat Erdem Sahin — built with 🧠 Gemini + 🎬 Google Vids.*
