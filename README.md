<div align="center">

# Daniel Silva

**Software &amp; systems engineer — industrial IoT, real-time telemetry and offline-first systems**

Caracas, Venezuela · Remote, hours overlapping the Americas

[![Portfolio](https://img.shields.io/badge/Portfolio-my--resume--landing-0B7A4B?style=flat-square&logo=vercel&logoColor=white)](https://my-resume-landing.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-daniel--alejandro--silva--rojas-0B7A4B?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-alejandro-silva-rojas/)
[![Email](https://img.shields.io/badge/Email-dsrglrm%40gmail.com-0B7A4B?style=flat-square&logo=maildotru&logoColor=white)](mailto:dsrglrm@gmail.com)

</div>

---

I build the software industrial operations depend on: real-time telemetry, networked hardware
control, and systems that keep working when the network does not. Five years, four production
systems, ~3,000 commits — shipped alongside my Computer Science degree, not after it.

## Results in production

| Result | What it means | Where |
| :-- | :-- | :-- |
| `200–500 ms` → `1–10 ms` | Replaced HTTP polling with a full-duplex WebSocket architecture; the server pushes state changes instead of the client re-asking for data that has not changed. Bandwidth down up to `95%`. | Industrial Digital Twin |
| `524 of 681` commits | Principal author and architect over five years, 398 files, version `12` in real field use. | IoT hardware control |
| `100%` offline | Plant floor runs with no internet and reconciles bidirectionally when connectivity returns. Zero field work lost. | Offline-first ecosystem |
| `20/20` + mention | Undergraduate thesis graded maximum with a Publication Mention, University of Zulia. | Video stabilization |

## Systems

> [!NOTE]
> The four industrial systems are private client repositories under NDA. I describe architecture,
> decisions and trade-offs — never business data. Happy to walk through any of them on a call.

<details>
<summary><strong>Industrial IoT hardware control</strong> — operates inspection cameras from two networked machines, unattended in the field · <em>2022–2026</em></summary>

<br>

Desktop application that coordinates industrial inspection cameras across two machines with no
technical support present on site.

- **Dual-PC architecture** — the same executable relaunches itself and assumes its role, server or
  client, with zero manual setup by the operator.
- **Resilient transfer** — chunked image transfer with reassembly and connection-drop handling.
- **No dead UI** — explicit timeouts at every network boundary, so a powered-off camera never
  freezes the interface.
- **Refactored under delivery** — monolith to modular library without stopping shipping, with a
  pytest/pytest-qt suite and a versioned Windows installer.

`Python` · `PyQt5` · `OpenCV` · `Socket.IO` · `matplotlib` · `pytest` · `PyInstaller`

</details>

<details>
<summary><strong>Offline-first ecosystem</strong> — 100% offline on plant floors, bidirectional cloud sync · <em>2023–2026</em></summary>

<br>

Desktop client that operates with no connectivity and reconciles with the cloud once the network
returns.

- **Sync that survives the field** — per-endpoint sync state, connectivity detection and retries.
- **Self-contained delivery** — a Python orchestrator brings up a portable database, Node/TypeScript
  services and the API, packaged in an installer that resolves its own dependencies.
- **Applied AI in-product** — custom audio transcription and synthesis pipeline (FastAPI/Uvicorn).
- **CI/CD** — GitHub Actions, tests with configuration isolation and connection pooling.

`Python` · `FastAPI` · `Node/TS` · `MariaDB` · `S3` · `GitHub Actions`

</details>

<details>
<summary><strong>Industrial time-series analysis</strong> — detects thermal cycles, replaced manual spreadsheet work · <em>2024–2026</em></summary>

<br>

Finds thermal cycles and gradient key points in sensor series.

- **Detection that does not break** — peak and valley detection with SciPy over a smoothed signal,
  plus interpolation of faulty readings.
- **Format-change resilient** — Polars pipeline adapted to two source-format changes without a
  rewrite.
- **Engineering-ready outputs** — structured JSON per cycle, an Excel table and an annotated plot.

`Python` · `Polars` · `NumPy` · `SciPy` · `matplotlib`

</details>

<details>
<summary><strong>DropAudio CCS</strong> — my own e-commerce product, in production · <em>founder &amp; architect</em></summary>

<br>

Built end to end and operating today at **[dropaudioccs.com](https://dropaudioccs.com)** with 102+
verified reviews.

- **Full stack ownership** — Nuxt 3 SSR storefront on Vercel, Supabase/PostgreSQL with row-level
  security.
- **Custom multi-currency checkout** — USDT, Zinli and Pago Móvil with live rates.
- **Admin panel** — inventory, sales, deliveries, real-time orders and a PDF catalog.
- **Resilient by design** — backup catalog, automated web push via `pg_cron`, technical SEO.

`Nuxt 3` · `Vue 3` · `Supabase` · `PostgreSQL` · `Vercel`

</details>

## Public work

| Repository | What it is |
| :-- | :-- |
| **[System_Stabilization_Interpolation](https://github.com/Dan178A/System_Stabilization_Interpolation)** | Video stabilization for mobile devices using motion meshes and interpolation, with algorithm weights predicted by a neural network. Undergraduate thesis — graded 20/20 with a Publication Mention. |
| **[FlowNet_Video_Stabilization](https://github.com/Dan178A/FlowNet_Video_Stabilization)** | Global camera-motion estimation distilled from a PWC-Net, QP-smoothed camera path, multi-scale photometric refinement. |
| **[RealtimeVoiceAssistant](https://github.com/Dan178A/RealtimeVoiceAssistant)** | Conversational voice assistant with streaming transcription and synthesis; the latency-critical audio path is written in Rust. |
| **[extract_rif](https://github.com/Dan178A/extract_rif)** | HTTP microservice turning Venezuelan RIF tax documents into structured JSON, with a dual-engine OCR pipeline and a fail-safe response contract. |

## Stack

**Languages**

![Python](https://img.shields.io/badge/Python-555?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-555?style=flat-square&logo=typescript&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-555?style=flat-square&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-555?style=flat-square&logo=cplusplus&logoColor=white)

**Real-time &amp; desktop**

![Qt](https://img.shields.io/badge/PyQt5-555?style=flat-square&logo=qt&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-555?style=flat-square&logo=socketdotio&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-555?style=flat-square&logo=grpc&logoColor=white)

**Data &amp; vision**

![Polars](https://img.shields.io/badge/Polars-555?style=flat-square&logo=polars&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-555?style=flat-square&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-555?style=flat-square&logo=scipy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-555?style=flat-square&logo=opencv&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-555?style=flat-square&logo=pytorch&logoColor=white)

**Web &amp; data layer**

![Vue 3](https://img.shields.io/badge/Vue%203-555?style=flat-square&logo=vuedotjs&logoColor=white)
![Nuxt 3](https://img.shields.io/badge/Nuxt%203-555?style=flat-square&logo=nuxtdotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-555?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-555?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-555?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-555?style=flat-square&logo=supabase&logoColor=white)

**Infrastructure**

![AWS](https://img.shields.io/badge/AWS-555?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-555?style=flat-square&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-555?style=flat-square&logo=vercel&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-555?style=flat-square&logo=githubactions&logoColor=white)

---

<div align="center">

**Open to freelance engagements and senior remote roles.**

[Portfolio](https://my-resume-landing.vercel.app/) ·
[LinkedIn](https://www.linkedin.com/in/daniel-alejandro-silva-rojas/) ·
[dsrglrm@gmail.com](mailto:dsrglrm@gmail.com)

</div>
