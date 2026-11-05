# Hetanshi Shah

### Software Development Engineer: backend APIs, data pipelines, AI evaluation, and React/TypeScript frontends.

I build reliable backend systems and the interfaces on top of them. Over 3+ years I've shipped REST APIs and microservices in Java/Spring Boot, Python data pipelines, and AI evaluation workflows, and I build React/TypeScript frontends that make hard-to-check things easy to check.

📍 New York, USA &nbsp;·&nbsp; 🎓 M.S. Computer Science, Montclair State University (4.0 GPA, December 2026) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/hetanshi-shah-96a10b337/) &nbsp;·&nbsp; [Email](mailto:shahhetanshi.work@gmail.com)

---

## Experience

**Software Development Engineer · Walmart** · Jan 2026 – Present
Enterprise AI evaluation and data pipeline operations.
- Automated Python data pipelines with unit-tested validation, processing 100,000+ operational records a day and removing 15+ hours of manual aggregation each week.
- SQL and Python analysis of large-scale performance metrics, delivered through Power BI dashboards with 3,000+ monthly user interactions.
- AI evaluation frameworks that test the reliability, consistency and failure modes of enterprise LLM outputs against structured accuracy baselines.
- SonarQube static analysis in the CI/CD pipeline, with findings mapped to CWE/CVE categories to cut false-positive vulnerability flags.

**Software Development Engineer · Accenture** · Aug 2022 – Dec 2024
Cloud-native backend integration and API modernization.
- High-throughput REST APIs and reporting microservices in Java, Spring Boot and SQL, handling 10,000+ daily transactions with sub-second latency.
- Azure DevOps CI/CD with Git-based workflows, taking deployment cycles from weeks to days with zero-downtime releases.
- Production support on systems with 99% uptime SLAs: debugging backend defects and writing runbooks that sped up incident response.
- Secure data synchronization pipelines and optimized legacy database connections between core microservices.

---

## Selected work

### [Circle Recommendations](https://github.com/hetanshigithub/circle-recommendations) — which community should she join, and why
`TypeScript` `Fastify` `SQLite` `zod` `Vitest` `GitHub Actions`

An API that recommends Lean In-style peer Circles to a member and explains each one in plain words: *"Matches your interest in getting promoted. Members posted 8 times in the past month."*

- **Filter, score, remove duplicates, explain.** Full, inactive and invite-only Circles are never recommended; six weighted signals rank the rest; near-identical Circles collapse into one.
- **Honest by design.** "Matches your interest" only when it's the Circle's main topic, life-stage Circles only for members who signalled that topic, and photo or profile completeness never affect ranking.
- **Measured, not assumed.** 27 tests, CI on Node 20 and 22, and an eval that checks all 100 members and reports which Circles never get seen.
- A small demo page shows each member's list the way she'd see it, plus what was left out and why.

### [Hookshot](https://github.com/hetanshigithub/hookshot) — reliable webhook delivery
`Java 21` `Spring Boot 3` `PostgreSQL` `Docker`

The machinery behind "we'll POST to your URL when something happens," the way Stripe and GitHub do it. Sending one HTTP request is easy; sending it reliably is the hard part.

- **Postgres is the queue.** Jobs are claimed with `FOR UPDATE SKIP LOCKED`, so any number of workers can run, and publishing enqueues in the same transaction as the event: no dual-write failure mode and no broker to operate.
- **Lease-based claiming** means a crashed worker needs no cleanup job. At-least-once delivery, equal-jitter exponential backoff, dead-letter state and a manual redeliver endpoint.
- **HMAC-SHA256 signatures** with replay protection, idempotency keys settled by a unique constraint, and SSRF protection re-checked at send time.
- Tested on a controlled `Clock` so multi-hour backoff schedules run instantly, plus a concurrency test where 8 workers race for 200 deliveries. CI runs on H2 and real PostgreSQL 16.

### [Document Q&A Assistant](https://github.com/hetanshigithub/ai-research-assistant-rag) — semantic retrieval with cited answers
`Python` `FastAPI` `FAISS` `sentence-transformers` `Docker` `pytest`

Ask questions about your own PDF and text files and get answers that trace back to their source. Runs fully locally.

- Chunks documents, embeds them with `all-MiniLM-L6-v2`, and retrieves top-k passages from a FAISS index saved to disk, with document fingerprinting so only changed files are rebuilt.
- An extractive answer generator ranks retrieved sentences by similarity and keyword overlap, removes near-duplicates, and returns cited evidence with a confidence score.
- Retrieval measured with **recall@k and MRR** on a 37-question labeled set; CI runs the pytest suite with an offline stub embedder, so no model download is needed.

### [Source-checked Q&A](https://github.com/hetanshigithub/source-checked-qa) — an AI answer you can verify
`React` `TypeScript` `Vite` `TanStack Query` `Vitest` · [Live demo](https://source-checked-qa.vercel.app/)

AI answers are hard to verify, so this interface puts the evidence next to the answer. Each statement is numbered, and selecting one highlights the exact sentence in its source passage. When the documents don't answer the question, it says so instead of showing a confident-looking guess.

- **Exact citations.** The backend returns the character range of every cited sentence and the interface highlights those ranges as given. A statement it can't locate is labelled "Source passage not located", not guessed at.
- **Honest weak-match state** below a confidence line, plus a retrieval inspector showing every passage, its similarity score and how many statements used it.
- Fully typed API layer with live and demo modes, 56 tests, and axe accessibility checks on the main screens.

### [Sigcheck](https://github.com/hetanshigithub/sigcheck) — find out why a webhook signature fails
`React` `TypeScript` `Tailwind CSS` `Web Crypto API` `Vitest` · [Live demo](https://sigcheck-navy.vercel.app/)

Paste a payload, secret and signature header. Sigcheck says whether the signature is valid and, when it isn't, which common mistake explains it, such as a trailing newline, re-serialized JSON or a base64 secret used as text. Everything runs in the browser, so nothing you paste is sent anywhere.

- Verifies Stripe-style, GitHub-style and plain HMAC signatures, and tries about 400 payload, secret and algorithm variations on a mismatch.
- Generates a Node or Python verifier, and the tests actually run the generated code against known vectors.

---

## Other projects

| | What it does | Stack |
| --- | --- | --- |
| [V-TALKS](https://github.com/hetanshigithub/V-TALKS-Android-Prototype) | Visa guidance for F-1 students, built from user interviews. Local-first, with a deliberately rule-based (not LLM) chatbot because a wrong answer costs a student their status. | Kotlin · Jetpack Compose · MVVM |
| [Prompt Experimentation Engine](https://github.com/hetanshigithub/Ai-Prompt-Experimentation-Engine) | Runs one task through five prompt strategies and ranks them with model judgment plus deterministic rule checks. Mock mode needs no API key. | Python · OpenAI API |
| [Who Wants to Be a Millionaire](https://github.com/hetanshigithub/WhoWantsToBeAMillionaire) | Trivia game with progressive difficulty; JUnit tests cover answer validation, score progression and edge cases. | Kotlin · Compose · StateFlow · JUnit |
| [Study Planner](https://github.com/hetanshigithub/study-planner-app) | Study tasks and daily habits, with local persistence and saved preferences. | Kotlin · Compose · Room · DataStore |
| [Campus Gallery](https://github.com/hetanshigithub/CampusGallery) | Photo gallery with local storage and async image loading. | Kotlin · Compose · Room · Coil |

---

## Stack

| | |
| --- | --- |
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?logo=csharp&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white) ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) |
| **Backend** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white) ![.NET](https://img.shields.io/badge/.NET-512BD4?logo=dotnet&logoColor=white) ![REST](https://img.shields.io/badge/REST_APIs-02569B) ![Microservices](https://img.shields.io/badge/Microservices-555555) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white) ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?logo=powerbi&logoColor=black) |
| **AI** | ![RAG](https://img.shields.io/badge/RAG-412991) ![FAISS](https://img.shields.io/badge/FAISS-0467DF) ![sentence-transformers](https://img.shields.io/badge/sentence--transformers-FFD21E?logo=huggingface&logoColor=black) ![LLM evaluation](https://img.shields.io/badge/LLM_evaluation-412991) ![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?logo=openai&logoColor=white) ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?logo=langchain&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB) ![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white) ![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?logo=reactquery&logoColor=white) ![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?logo=jetpackcompose&logoColor=white) |
| **Cloud, DevOps & testing** | ![Azure](https://img.shields.io/badge/Azure-0078D4?logo=microsoftazure&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white) ![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?logo=azuredevops&logoColor=white) ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?logo=sonarqube&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?logo=pytest&logoColor=white) ![JUnit](https://img.shields.io/badge/JUnit-25A162?logo=junit5&logoColor=white) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest&logoColor=white) |

---

**Graduating December 2026 and looking for software engineering roles.** The fastest way to reach me is [email](mailto:shahhetanshi.work@gmail.com).
