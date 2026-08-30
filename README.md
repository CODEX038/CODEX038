<div align="center">

<img src="assets/header.gif" width="100%" alt="Shreepad Salvi — computer vision and agentic AI" />

# Shreepad Salvi

**Applied AI · Computer Vision · Multi-Agent Systems · Geospatial ML**

Computer Engineering @ Bharat College of Engineering, Mumbai · 2023–2027

<a href="https://www.linkedin.com/in/shreepadsalvi/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:shreepadsalvi@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://cfp-04.vercel.app"><img src="https://img.shields.io/badge/Live_Demo-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Live demo" /></a>

</div>

---

## What I optimise for

I build AI systems for messy, low-connectivity, high-variance conditions — specifically Indian ones. Every project here ships with an evaluation log that states where it fails. I'd rather publish an honest mAP number with its caveats than a demo video that only works on the clip I recorded it with.

---

## Measured results

Numbers from held-out evaluation, not training runs. Full per-class tables and caveats are in each repo's evaluation log.

| Project | What was measured | Result |
|---|---|---|
| **BharatDrive-X Twin** | YOLOv8n fine-tuned on IDD + RDD2022 India, 10 hazard classes, 1,648 held-out images, no leakage | **mAP50 0.442** · P 0.672 · R 0.401 · 24.6 ms/image (CPU) |
| **BharatDrive-X Twin** | Fused driver + road perception loop | **25 FPS**, 12 ms loop latency, CPU only — no GPU, no cloud, no API keys |
| **BharatDrive-X Twin** | Alert calibration pass | Max false-critical risk **0.93 → 0.65** |
| **MediBot** | Adversarial suite: poisoned KB, injected docs, fake citations, cross-patient probing | **80 tests + hard eval gates**, passing in CI |
| **FundChain** | Deployed end to end | Live on **Ethereum Sepolia** · [cfp-04.vercel.app](https://cfp-04.vercel.app) |

---

## Projects

<table>
<tr>
<td width="50%" valign="top">

### 🚗 [BharatDrive-X Twin](https://github.com/CODEX038/BharatDrive-x-Twin)
Offline-first AI safety co-pilot. Fuses driver-facing and road-facing perception into one explainable Journey Safety Score — because a drowsy driver on an empty road and an alert driver in dense traffic are not the same risk.

`Python` `PyTorch` `YOLOv8` `OpenCV` `MediaPipe` `SQLite`

</td>
<td width="50%" valign="top">

### 🌾 [Kisan Mitra](https://github.com/CODEX038/kisan-mitra)
Multilingual multi-agent crop advisor. A farmer asks in Hindi or Marathi whether to irrigate; specialist agents check satellite NDVI, soil moisture and weather, and answer in their own language.

`Google ADK` `Gemini` `MCP` `Docker` `Cloud Run`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🩺 [MediBot](https://github.com/CODEX038/MEDIBOT)
Source-grounded healthcare RAG. The model may only cite retrieved, approved sources, must abstain when confidence is low, and is tested against an adversarial suite.

`FastAPI` `PostgreSQL` `RAG` `Next.js` `Docker` `CI`

</td>
<td width="50%" valign="top">

### 🎯 [InternArsenal](https://github.com/CODEX038/INTERNARSENAL)
AI internship platform for Indian students — aggregation, transparent match scoring, ATS-optimised resume generation, and a full application pipeline.

`Next.js 16` `React 19` `TypeScript` `Prisma` `Supabase` `Groq` `Redis`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ⛓️ [FundChain](https://github.com/CODEX038/FUNDCHAIN-V2)
Crowdfunding that replaces trust with proof. Every donation is an on-chain transaction; a contract event listener keeps the database honest to the chain. **[Live →](https://cfp-04.vercel.app)**

`Solidity` `Foundry` `ethers.js` `React` `MongoDB` `Stripe`

</td>
<td width="50%" valign="top">

### 🔭 Everything else
Hackathon builds, experiments, and coursework that outgrew coursework.

**[Browse all repositories →](https://github.com/CODEX038?tab=repositories)**

</td>
</tr>
</table>

---

<details>
<summary><b>Engineering decisions worth reading about</b></summary>

<br>

**Personalised fatigue thresholds.** Most drowsiness detectors use one closed-eye constant for every human. BharatDrive-X learns the threshold as ~65% of the driver's own median EAR, with 3×MAD outlier rejection — so it detects deviation from *you*, not from a textbook.

**Knowing what it doesn't know.** A dedicated reliability engine distinguishes *unknown* from *closed*. An invisible eye is never reported as a shut one; a missing face is investigated, never assumed recovered.

**Fusion that can't be averaged away.** A critical driver state caps the Journey Safety Score, so a calm road can never dilute a drowsy driver into a safe-looking number.

**Abstention as a feature.** MediBot returns a refusal — not a guess — on empty, withdrawn, off-topic or low-confidence queries. Emergency detection runs on deterministic rules, independent of the LLM.

**Guardrails before capability.** Kisan Mitra filters prompt injection on input and attaches safety disclaimers on output, before any agent is allowed to reason.

</details>

<details>
<summary><b>Stack</b></summary>

<br>

**AI / ML** — PyTorch · YOLOv8 · OpenCV · MediaPipe · scikit-learn · RAG · Google ADK · MCP · Gemini · Groq

**Languages** — Python · TypeScript · JavaScript · Solidity · SQL

**Backend** — FastAPI · Node.js · Express · Prisma · PostgreSQL · MongoDB · Redis · Supabase

**Frontend** — Next.js · React · Tailwind CSS

**Infra** — Docker · GitHub Actions · Vercel · GCP Cloud Run · Foundry · pytest

</details>

---

## Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=CODEX038&show_icons=true&theme=github_dark&hide_border=true&bg_color=0D1117&icon_color=5FD3E8&title_color=5FD3E8&cache_seconds=7200" alt="GitHub stats for CODEX038" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=CODEX038&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=5FD3E8&langs_count=8&cache_seconds=7200" alt="Most used languages" />

<img src="https://streak-stats.demolab.com?user=CODEX038&theme=github-dark-blue&hide_border=true&background=0D1117&ring=5FD3E8&fire=5FD3E8&currStreakLabel=5FD3E8&cache_seconds=7200" alt="Contribution streak" />

</div>

---

<div align="center">

**Open to AI/ML, computer vision and data internships** — remote, hybrid, or Mumbai/Pune.

Learning in public, one repo at a time.

</div>
