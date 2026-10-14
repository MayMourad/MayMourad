<p>
  <a href="#selected-projects">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MayMourad/MayMourad/main/assets/hero-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MayMourad/MayMourad/main/assets/hero-light.svg">
      <img alt="May A. Mourad — Artificial Intelligence · Robotics · Intelligent Systems" src="https://raw.githubusercontent.com/MayMourad/MayMourad/main/assets/hero-light.svg" width="100%">
    </picture>
  </a>
</p>

I'm a Grade 12 student (Advanced Stream, class of 2027) at ADNOC Schools Madinat Zayed, Abu Dhabi, preparing to study AI engineering. I build working software — a family walking app with a unit-tested scoring algorithm, an agentic planning workflow on Gemini, a simulation of ancestry bias in genomic data — and try to keep its logic testable and explainable. I've also built robots and hardware prototypes for UAE competitions, and my research spans cognitive neuroscience and fairness in genomic AI.

[Projects](#selected-projects) · [Evidence](#engineering-evidence) · [Stack](#stack-and-capabilities) · [Research](#research) · [Leadership](#leadership-and-recognition) · [Connect](#connect)

## Selected projects

### Khutwa

*A family walking app for the UAE Year of Family · Third Place, Khalifa University Smart Mobile App Contest (SMAC) 2026*

Families share one Ghaf tree that grows with their combined steps. Walking near one of eight Abu Dhabi heritage sites plays a short narrated story about the place.

**My role —** AI & Data Lead, in a team of two with Shamsa Faris Al Mazrouei (Core App Lead). I designed the Khutwa Score and its weighting, developed the weekly step aggregation, designed the Firestore data model and security rules, contributed to testing and debugging the scoring logic, and prepared the technical documentation and presentations.

**Engineering —** The score is a weighted composite of movement (40%), time together (35%) and heritage (25%), with each metric capped at a target so a surplus in one can't make up for another. Scoring and aggregation are pure TypeScript functions kept apart from Firebase, covered by 18 Jest tests and a documented worked example. Stories were pre-generated with an LLM, reviewed, and played with on-device text-to-speech; no LLM runs inside the app.

`React Native` `Expo` `TypeScript` `Firebase Auth` `Cloud Firestore` `Jest` `GitHub Actions`<br>
[Source](https://github.com/MayMourad/SMAC-ADNOCMZ-Khutwa) · [Web build](https://maymourad.github.io/SMAC-ADNOCMZ-Khutwa/) · [Scoring method](https://github.com/MayMourad/SMAC-ADNOCMZ-Khutwa/blob/main/docs/khutwa-score.md) · [AI usage report](https://github.com/MayMourad/SMAC-ADNOCMZ-Khutwa/blob/main/docs/AI-USAGE-REPORT.md)

### Genomic Variant Prioritization & Bias Simulator

*An interactive simulation of ancestry bias in genetic reference data · independent student project, 2026*

A mock decision-support tool that ranks genetic variants and reports how well reference databases such as gnomAD and ClinVar cover a patient's ancestry. Switching from a European to a Gulf/Emirati reference context drops a share of variants to medium or low confidence and flags them for manual review, making the coverage gap visible in two clicks.

**My role —** Sole developer. The project is framed around a Technology Innovation Institute research centre but is not affiliated with or endorsed by TII.

**Engineering —** Deterministic scoring over synthetic variants, so every run is reproducible, with a staged pipeline view, a Recharts confidence distribution, expandable evidence rows and CSV export. The interface cites the population-genetics studies behind its assumptions. It uses no patient data and makes no clinical claims.

`React` `TypeScript` `Vite` `Recharts` `Three.js` `Tailwind CSS`<br>
[Source](https://github.com/MayMourad/AI-Strategy-TII) · [Live simulation](https://maymourad.github.io/AI-Strategy-TII/)

### GreenReceipt AI

*Receipt analysis with a vision model and deterministic scoring · TKS Prompt to Product Challenge, July 2026*

Upload a shopping receipt and get one report on spending, wellness and sustainability, summarised as a PurchaseIQ score with suggested swaps.

**My role —** Sole developer.

**Engineering —** In live mode, the receipt image goes to Anthropic's vision API with instructions to return a single JSON object in a fixed schema; the API key is entered by the user and held only in memory. The model supplies the item-level analysis and PurchaseIQ sub-scores. A deterministic swap engine in plain JavaScript then proposes up to three swaps and recalculates the totals. Demo mode runs on three sample receipts and needs no key.

`JavaScript` `Anthropic API` `Structured JSON output` `HTML/CSS`<br>
[Source](https://github.com/MayMourad/GreenReceipt-AI) · [Live demo](https://maymourad.github.io/GreenReceipt-AI/)

### MajlisAI

*An agentic workflow for family coordination · Sandooq Al Watan Agentic AI Summer Program, August 2026*

Turns a free-form family message in Arabic or English into a structured bilingual plan with assigned tasks, translated directions, timing alerts and a family-connection prompt.

**My role —** Team Lead and Lead Developer in a team of four. I built the operational pipeline; teammates led prompt design, knowledge curation and testing.

**Engineering —** Google Form → Google Sheets → Apps Script → Gemini → plan logged back to the sheet. Gemini processes each request against one Majlis AI system instruction. The public repository holds the bilingual showcase site and the live intake form; the Apps Script backend is maintained separately and is not published.

`Gemini API` `Google Apps Script` `Google Sheets` `Google Forms` `HTML/CSS/JS`<br>
[Showcase source](https://github.com/MayMourad/MajlisAI) · [Live site](https://maymourad.github.io/MajlisAI/)

### Also featured

**NeuroPace Analytics** — *Python back end for cognitive-readiness analytics*<br>
A FastAPI service that uses NumPy to turn synthetic athlete telemetry into a Cognitive Readiness Index (z-score normalisation, rolling means, a weighted combination and a logistic mapping to 0–100) and a per-session risk score, served over REST endpoints. Sole developer. The back end currently sits inside the dashboard's HTML file and is not yet connected to it.<br>
`Python` `FastAPI` `NumPy` · [Source](https://github.com/MayMourad/NeuroPace-Analytics) · [Dashboard](https://maymourad.github.io/NeuroPace-Analytics/)

**ReEngine AI** — *Explainable rules engine for device reuse · Promising Changemaker Award, Techsplore (Girls Who Code), August 2026*<br>
Scores an underused laptop, tablet or phone against five second-life roles with a transparent six-factor rules engine. There's no machine learning, and every sub-score is shown. One role is fully built: the laptop becomes a working family and study dashboard, and the app issues an Impact Receipt. Sole developer.<br>
`JavaScript` `HTML/CSS` · [Source](https://github.com/MayMourad/ReEngine-AI) · [Demo](https://maymourad.github.io/ReEngine-AI/)

<details>
<summary>Earlier prototypes and physical engineering</summary>
<br>

- **FamilyOS:** Team Leader and Lead Developer. 7th place, Abu Dhabi University 5th Annual College of Engineering Hackathon (2026). A bilingual family-support concept prototype; the submitted version has no AI back end. [Source](https://github.com/MayMourad/FamilyOS-AI)
- **NeuroBridge:** Team Lead and Lead Developer, Abu Dhabi University 4th Annual College of Engineering Hackathon (2025). An accessibility concept with a rule-based assistant; adaptive learning was proposed, not built. [Source](https://github.com/MayMourad/NeuroBridge)
- **EcoCore AI:** Sole developer, International Computing Olympiad 2025, Certificate of Outstanding Participation (GCC region). A sustainability prototype with simulated environmental data and a rule-based chatbot. [Source](https://github.com/MayMourad/EcoCore-AI)
- **Robotics and hardware:** MakeX Mubarmij Al Emarat, 5th nationally and qualified for the 2024 international finals in China (did not attend). Team Leader and Lead Engineer, Yas in Schools 4x4 (2024). A piezoelectric energy-harvesting prototype (First Place, Academy of Excellence STEM Track, 2025). Arduino builds, including obstacle-detecting glasses.

</details>

## Engineering evidence

Problem, approach, implementation and outcome for four of these projects, with a link to something you can check.

**Khutwa**<br>
`PROBLEM ` Reward family connection, not step counts alone<br>
`APPROACH` Weighted composite (40 / 35 / 25), each metric capped at a target<br>
`BUILD   ` Pure TypeScript scoring and aggregation, isolated from Firebase<br>
`OUTCOME ` 18 Jest tests and a documented [worked example](https://github.com/MayMourad/SMAC-ADNOCMZ-Khutwa/blob/main/docs/khutwa-score.md)

**Variant simulator**<br>
`PROBLEM ` Show how reference-panel gaps change confidence in variant rankings<br>
`APPROACH` Score the same variants under European and Gulf ancestry contexts<br>
`BUILD   ` Deterministic logic over synthetic data, in React with Recharts<br>
`OUTCOME ` A reproducible [two-click contrast](https://maymourad.github.io/AI-Strategy-TII/), with the studies it relies on cited

**GreenReceipt AI**<br>
`PROBLEM ` Make a vision model's output usable by application code<br>
`APPROACH` One fixed JSON schema, with the swap logic kept outside the model<br>
`BUILD   ` Vision API call, then deterministic swaps and rescoring in JavaScript<br>
`OUTCOME ` Live and demo modes share one report format ([source](https://github.com/MayMourad/GreenReceipt-AI/blob/main/app.js))

**MajlisAI**<br>
`PROBLEM ` Turn free-form family messages into assignable tasks<br>
`APPROACH` An agentic pipeline driven by one system instruction<br>
`BUILD   ` Forms → Sheets → Apps Script → Gemini → Sheets<br>
`OUTCOME ` A working pipeline behind the [live intake form](https://maymourad.github.io/MajlisAI/)

## Stack and capabilities

- **Languages:** TypeScript, JavaScript, Python, C++, HTML/CSS<br><sub>Khutwa · GreenReceipt · NeuroPace · Arduino projects</sub>
- **Front end and mobile:** React, React Native, Expo, Vite<br><sub>Khutwa · Variant simulator</sub>
- **Back end, data and integrations:** Firebase Auth, Cloud Firestore, FastAPI, NumPy, Google Apps Script<br><sub>Khutwa · NeuroPace · MajlisAI</sub>
- **AI and computation:** Anthropic API, Gemini API, agentic workflows, weighted scoring models, statistical normalisation<br><sub>GreenReceipt · MajlisAI · Khutwa · ReEngine · NeuroPace</sub>
- **Testing and delivery:** Jest, GitHub Actions, GitHub Pages, EAS Build<br><sub>Khutwa</sub>
- **Robotics and embedded:** Arduino, sensor integration, motor control<br><sub>MakeX · Yas in Schools · Arduino builds</sub>

## Research

**`PUBLISHED`** &nbsp;*The Impact of Multitasking on Memory Formation in Teenagers: A Cognitive Neuroscience Perspective*<br>
International Youth Neuroscience Association (IYNA) Journal, Vol. 9, Issue 5, August 2025 · [Journal issue (PDF)](https://drive.google.com/file/d/1eXbgknR1VjSV7UjG-uSs-YziiWU1swl4/view?usp=drive_link)

**`COMPLETED`** &nbsp;*Genetic Dataset Bias in AI Disease Prediction: Investigating How Population Diversity Influences Accuracy and Fairness of Medical AI Models*<br>
ESTEDAD National Ambassadors Program, Scientific Research Track · Khalifa University · July 2026<br>
Team Leader. A literature review and research matrix, with findings presented to Khalifa University; not published. The variant simulator above explores the same question computationally.

**`PROPOSAL`** &nbsp;*Real-Time Brain–Computer Interfaces for Enhancing Attention in Students Through Neurofeedback*<br>
IYNA Summer Program, 2026<br>
An EEG-based neurofeedback concept, written as a research proposal. No system has been built or tested.

## Leadership and recognition

**Leadership**

- **Chair, MBZUAI AI Youth Ambassadors (AYA), Cohort 2** · academic year 2026–27<br><sub>Cohort strategic priorities: practical AI innovation, AI education pathways, interdisciplinary AI fluency, and responsible AI in creative fields.</sub>
- **Chair, AI Youth Council (MIT RAISE), ADNOC Schools Madinat Zayed** · appointed October 2026

**Recognition**

- **Third Place**, Khalifa University Smart Mobile App Contest (SMAC), 2026 · Khutwa
- **Promising Changemaker Award**, Techsplore (Girls Who Code), 2026 · ReEngine AI
- **7th Place**, Abu Dhabi University 5th Annual College of Engineering Hackathon, 2026 · FamilyOS
- **Certificate of Outstanding Participation** (GCC region), International Computing Olympiad, 2025 · EcoCore AI
- **First Place**, Academy of Excellence STEM Track, 2025 · piezoelectric energy-harvesting prototype
- **5th Place nationally**, MakeX Mubarmij Al Emarat, 2024 · qualified for the international finals in China; did not attend

## Connect

[LinkedIn](https://www.linkedin.com/in/may-mourad-47a288374/) · [GitHub](https://github.com/MayMourad) · [maymourad10@gmail.com](mailto:maymourad10@gmail.com)
