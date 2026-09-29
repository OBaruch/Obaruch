# README Overview

The root [`README.md`](../README.md) is the only "implementation" artifact in this repository. It is written in GitHub-Flavored Markdown with inline HTML (`<h1 align="center">`, `<p align="center">`, `<img>`), which GitHub renders on the profile page.

This page describes what the file contains. It does not change or reproduce it.

## Section-by-section breakdown

| # | Section | Format | Content |
|---|---------|--------|---------|
| 1 | Header | HTML (`<h1>`, `<p align="center">`) | Name, current role (*Advanced AI Engineer @ Bosch*), focus areas, degree / MBA status / location. |
| 2 | Contact badges | HTML links wrapping shields.io badges | Website (`baruchlopez.com`), LinkedIn, GitHub. |
| 3 | 💫 About me | Markdown | Professional summary: 4+ years in end-to-end AI and data solutions, focus areas, education, move toward Enterprise Architecture (TOGAF). |
| 4 | 🛠️ Tech stack | Markdown images (shields.io) | Badges in four groups: *Languages & core*, *AI / ML / LLMs*, *Data / BI / automation*, *Cloud / DevOps / web*. |
| 5 | 🚀 Selected work | Markdown list | Five anonymized professional projects (GenAI customs platform, hackathon win, computer-vision team lead, plant analytics, optimization & ML). |
| 6 | 🎓 Education & learning | Markdown list | Degree, MBA, selected certifications, speaking engagements. |
| 7 | 📁 Featured public projects | Markdown list | Six links to public repositories under `github.com/OBaruch/...`. |
| 8 | 📊 GitHub stats | HTML `<img>` | Dynamic stats card, top-languages card, and trophies. |
| 9 | Footer | HTML | Closing tagline. |

## Tech stack as listed in the README

Taken from the badges as written. This is the author's self-reported stack. It is not a list of technologies used in *this* repository, which contains no code.

- **Languages & core:** Python, SQL, TypeScript, MATLAB, C, C#
- **AI / ML / LLMs:** PyTorch, TensorFlow, Keras, scikit-learn, OpenCV, Hugging Face, Claude, Azure OpenAI
- **Data / BI / automation:** Power BI, Alteryx, KNIME, Airflow, pandas
- **Cloud / DevOps / web:** Azure, AWS, Docker, FastAPI, Flask, Astro, Git

## Featured public projects referenced

| Repository | Description (from the README) |
|------------|-------------------------------|
| `OBaruch/Planetary-Biological-Computing` | *Gaia-1*: planetary-scale closed-loop concept with biological neurons and Earth signals. |
| `OBaruch/Project-Center` | Markdown-first, GitHub-based personal operating repository. |
| `OBaruch/High_Performance_Stocks` | Analysis of US stocks for high annual returns. |
| `OBaruch/ai-voice-agent` | AI voice call agent (Twilio + LLM + TTS). |
| `OBaruch/relationship-exploration-map` | Interactive board-game metaphor for relational growth. |
| `OBaruch/Differential-Evolution-AI` | Evolutionary / bio-inspired optimization (MATLAB). |

The links were not checked from within this repository. Whether each one resolves is **Unknown** here.

## External dependencies

The README has no build step, but it depends on these third-party services at render time:

| Service | Used for | Effect if unavailable |
|---------|----------|-----------------------|
| `img.shields.io` | All static badges (contact and tech stack) | Badges show as broken images or alt text. |
| `github-readme-stats.vercel.app` | Stats card and top-languages card | Cards show as broken images. Public instances of this service are known to hit rate limits. |
| `github-profile-trophy.vercel.app` | Trophies row | Row shows as a broken image. |

## How it works

No code runs. GitHub renders `README.md` on <https://github.com/OBaruch>. The Markdown and HTML are rendered statically, and the images are fetched from the services above whenever someone views the profile.

## Running the project

Nothing needs to be run. To preview changes, open the file in any Markdown viewer that supports GitHub-Flavored Markdown, or view it on GitHub.
