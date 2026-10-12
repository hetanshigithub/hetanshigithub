# Hetanshi Shah

### Android engineer who also builds AI systems.

Kotlin and Jetpack Compose on the surface, Python and LLM tooling underneath, and two years shipping production REST APIs before grad school.

📍 New Jersey &nbsp;·&nbsp; 🎓 M.S. Computer Science, Montclair State University — 4.0 GPA, December 2026 &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/hetanshi-shah-96a10b337/) &nbsp;·&nbsp; [Email](mailto:hetanshishahh@gmail.com)

---

## Selected work

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

### [Who Wants to Be a Millionaire](https://github.com/hetanshigithub/WhoWantsToBeAMillionaire) — Android, with tests
`Kotlin` `Jetpack Compose` `StateFlow` `JUnit`

A trivia game built to get state handling right, not just to ship screens.

- MVVM with ViewModel and StateFlow; game state survives rotation and configuration changes.
- JUnit tests cover answer validation, score progression and game-flow edge cases.

---

## Other projects

| | What it does | Stack |
| --- | --- | --- |
| [AI Research Assistant](https://github.com/hetanshigithub/ai-research-assistant-rag) | RAG built from scratch — chunking, embeddings and cosine-similarity retrieval over your own documents, returning a summary with key insights, risks and supporting evidence. Runs fully local, no paid API. | Python · sentence-transformers · scikit-learn |
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
| **Android** | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) ![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?logo=jetpackcompose&logoColor=white) ![Material 3](https://img.shields.io/badge/Material_3-757575?logo=materialdesign&logoColor=white) ![Room](https://img.shields.io/badge/Room-3DDC84?logo=android&logoColor=white) ![DataStore](https://img.shields.io/badge/DataStore-3DDC84?logo=android&logoColor=white) ![MVVM](https://img.shields.io/badge/MVVM-555555) |
| **Languages** | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?logo=csharp&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white) |
| **AI / ML** | ![RAG](https://img.shields.io/badge/RAG-412991) ![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?logo=openai&logoColor=white) ![sentence-transformers](https://img.shields.io/badge/sentence--transformers-FFD21E?logo=huggingface&logoColor=black) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white) |
| **Backend** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white) ![.NET](https://img.shields.io/badge/.NET-512BD4?logo=dotnet&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white) |
| **Testing & tooling** | ![JUnit](https://img.shields.io/badge/JUnit-25A162?logo=junit5&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white) ![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?logo=azuredevops&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?logo=sonarqube&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white) |

---

**Graduating December 2026 and looking for software engineering, Android or AI/ML roles.** The fastest way to reach me is [email](mailto:hetanshishahh@gmail.com).
