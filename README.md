# Hetanshi Shah

### Frontend-focused software engineer — React, TypeScript and Android.

I build interfaces that make hard-to-check things easy to check: React and TypeScript on the web, Kotlin and Jetpack Compose on mobile. I also write the Java and Python backends behind them, and two years of shipping production REST APIs before grad school means I know what the UI is talking to.

📍 New Jersey &nbsp;·&nbsp; 🎓 M.S. Computer Science, Montclair State University — 4.0 GPA, December 2026 &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/hetanshi-shah-96a10b337/) &nbsp;·&nbsp; [Email](mailto:hetanshishahh@gmail.com)

---

## Selected work

### [Source-checked Q&A](https://github.com/hetanshigithub/source-checked-qa) — an AI answer you can verify
`React` `TypeScript` `Vite` `TanStack Query` `Vitest`

AI answers are hard to verify, so this interface puts the evidence next to the answer. Each statement is numbered, and selecting one highlights the exact sentence in its source passage. When the documents don't answer the question, it says so instead of showing a confident-looking guess.

- **Exact citations.** The backend returns the character range of every cited sentence and the interface highlights those ranges as given. A statement it can't locate is labelled "Source passage not located", not guessed at.
- **Honest weak-match state** below a confidence line, plus a retrieval inspector showing every passage, its similarity score and how many statements used it.
- Upload and remove documents, shareable `?q=` links, and Back/Forward stepping between questions.
- **56 tests**, axe accessibility checks on the main screens, and a demo mode that runs with no server. The README lists the limits, including that nothing was tested with a screen reader.

### [Sigcheck](https://github.com/hetanshigithub/sigcheck) — find out why a webhook signature fails
`React` `TypeScript` `Tailwind CSS` `Web Crypto API` `Vitest`

Paste a payload, secret and signature header. Sigcheck says whether the signature is valid and, when it isn't, which common mistake explains it, such as a trailing newline, re-serialized JSON or a base64 secret used as text. Everything runs in the browser, so nothing you paste is sent anywhere.

- Verifies Stripe-style, GitHub-style and plain HMAC signatures, and tries about 400 payload, secret and algorithm variations on a mismatch.
- Generates a Node or Python verifier, and the tests actually run the generated code against known vectors.
- 60+ tests with axe accessibility checks.

### [Hookshot](https://github.com/hetanshigithub/hookshot) — reliable webhook delivery (the backend side of the same problem)
`Java 21` `Spring Boot 3` `PostgreSQL` `Docker`

The machinery behind "we'll POST to your URL when something happens," the way Stripe and GitHub do it. Sending one HTTP request is easy; sending it reliably is the hard part — receivers go down, retries stampede, payloads get forged, and users point webhooks at your internal network.

- **Postgres is the queue.** Jobs are claimed with `FOR UPDATE SKIP LOCKED`, so you can run as many worker instances as you like, and publishing enqueues in the same transaction as the event — no dual-write failure mode and no broker to operate.
- **Lease-based claiming** means a crashed worker needs no cleanup job: its rows simply become due again. At-least-once delivery, equal-jitter exponential backoff, dead-letter state and a manual redeliver endpoint.
- **HMAC-SHA256 signatures** with replay protection, idempotency keys settled by a unique constraint, and SSRF protection re-checked at send time with no redirects followed.
- Tested on a controlled `Clock` so multi-hour backoff schedules run instantly, plus a concurrency test where 8 workers race for 200 deliveries. CI runs the suite twice — on H2 and against real PostgreSQL 16.

### [V-TALKS](https://github.com/hetanshigithub/V-TALKS-Android-Prototype) — visa guidance for international students
`Kotlin` `Jetpack Compose` `MVVM` `local-first`

An Android app for the F-1, CPT, OPT, STEM OPT and EAD decisions where a wrong move costs a student their status. Step-by-step guides with interactive checklists, a deadline tracker with on-device reminders, and a career roadmap that lines visa timing up against internship and job planning.

- Built from **semi-structured interviews with F-1 graduate students** and reflexive thematic analysis. Six user-need themes drove the feature set — not a feature list I wrote first.
- **Rule-based chatbot, deliberately not an LLM.** In a compliance context a hallucinated answer is worse than no answer, so responses stay deterministic and every one routes the student to their DSO to verify.
- **No backend at all.** Privacy surfaced in every interview, so the whole app runs on-device. Ships as an installable APK, API 26+.

### [Prompt Experimentation Engine](https://github.com/hetanshigithub/Ai-Prompt-Experimentation-Engine) — making prompt iteration measurable
`Python` `OpenAI API`

Prompt tuning is usually guesswork. This runs one task through five prompt strategies, scores every output against a shared rubric, and ranks them.

- Scoring blends model judgment with **deterministic rule checks** — length, repetition, sentence structure, task keyword coverage — into a weighted six-factor total (relevance 22%, overall effectiveness 20%, clarity 18%, specificity 18%, tone 12%, rule-based quality 10%).
- **Mock mode runs the full pipeline with no API key**, so the workflow is demoable for free.
- Optional refinement loop feeds critique back in and re-runs; every experiment exports to JSON so runs can be compared over time.

---

## Other projects

| | What it does | Stack |
| --- | --- | --- |
| [AI Research Assistant](https://github.com/hetanshigithub/ai-research-assistant-rag) | RAG built from scratch — chunking, embeddings and cosine-similarity retrieval over your own documents, returning a summary with key insights, risks and supporting evidence. Runs fully local, no paid API. | Python · sentence-transformers · scikit-learn |
| [Who Wants to Be a Millionaire](https://github.com/hetanshigithub/WhoWantsToBeAMillionaire) | Trivia game with progressive difficulty and score tracking. State survives rotation and configuration changes; JUnit tests cover answer validation, score progression and edge cases. | Kotlin · Compose · StateFlow · JUnit |
| [Study Planner](https://github.com/hetanshigithub/study-planner-app) | Study tasks and daily habits, with local persistence and saved user preferences. | Kotlin · Compose · Room · DataStore |
| [Campus Gallery](https://github.com/hetanshigithub/CampusGallery) | Photo gallery with local storage and async image loading. | Kotlin · Compose · Room · Coil |
| [Student Profile](https://github.com/hetanshigithub/studentprofile) | Profile management app structured on clean architecture. | Kotlin · Compose |

---

## Before grad school

Two years at **Dbmares** as a junior software developer: REST APIs and backend reporting services in Java/Spring Boot, C#/.NET and Python/SQL, consumed by Angular front ends. Wrote the unit and integration tests and the Azure DevOps CI/CD pipelines behind them, and handled production defects through root-cause analysis.

---

## Stack

| | |
| --- | --- |
| **Frontend** | ![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white) ![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?logo=reactquery&logoColor=white) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest&logoColor=white) ![Testing Library](https://img.shields.io/badge/Testing_Library-E33332?logo=testinglibrary&logoColor=white) ![HTML/CSS](https://img.shields.io/badge/HTML_%2F_CSS-E34F26?logo=html5&logoColor=white) |
| **Android** | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) ![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?logo=jetpackcompose&logoColor=white) ![Material 3](https://img.shields.io/badge/Material_3-757575?logo=materialdesign&logoColor=white) ![Room](https://img.shields.io/badge/Room-3DDC84?logo=android&logoColor=white) ![DataStore](https://img.shields.io/badge/DataStore-3DDC84?logo=android&logoColor=white) ![MVVM](https://img.shields.io/badge/MVVM-555555) |
| **Backend** | ![Java](https://img.shields.io/badge/Java_21-ED8B00?logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?logo=springboot&logoColor=white) ![.NET](https://img.shields.io/badge/.NET-512BD4?logo=dotnet&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white) ![Flyway](https://img.shields.io/badge/Flyway-CC0000?logo=flyway&logoColor=white) ![REST](https://img.shields.io/badge/REST_APIs-02569B) |
| **Languages** | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?logo=csharp&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white) |
| **AI / ML** | ![RAG](https://img.shields.io/badge/RAG-412991) ![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?logo=openai&logoColor=white) ![sentence-transformers](https://img.shields.io/badge/sentence--transformers-FFD21E?logo=huggingface&logoColor=black) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white) |
| **Testing & infra** | ![JUnit](https://img.shields.io/badge/JUnit-25A162?logo=junit5&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white) ![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?logo=azuredevops&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white) ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?logo=sonarqube&logoColor=white) |

---

**Graduating December 2026 and looking for frontend and software engineering roles (React, TypeScript, Android).** The fastest way to reach me is [email](mailto:hetanshishahh@gmail.com).
