<!-- Showcase repository: the product is real and in use, its source code is private. -->

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg"><img src="assets/banner-light.svg" width="100%" alt="Spead AI Pro for Wijaya Karya. An AI workspace for the tender and contract team: fills the review form, and every quote is checked."></picture>

<p align="center"><a href="https://github.com/nugrahalabib">More of my work</a> · <a href="https://nugrahalabib.com">nugrahalabib.com</a> · <a href="mailto:nugrahalabib@gmail.com">Email</a></p>

<p align="center"><a href="#the-business">The business</a> · <a href="#product-tour">Product tour</a> · <a href="#for-developers">For developers</a></p>

## Overview

Spead AI Pro is the Spead AI deployment for the tender and contract/legal team of the EPCC Division at PT Wijaya Karya. It reads a tender package and fills the tender document review form (Lampiran 2.3). It also answers questions over the same package, with citations.

Filling that form by hand means reading long contract PDFs clause by clause. Here the AI proposes each answer, and every quote it uses is checked against the source document and given a status. People review and approve the result.

Around that core sits a full workspace: a knowledge library with access rights and confidentiality labels, Document Studio with an ONLYOFFICE editor, and connectors where any action that changes data waits for a human to approve.

| | |
| --- | --- |
| **Status** | Pilot |
| **Role** | Built and led by Nugraha Labib Mujaddid as Founder & Lead AI Engineer of Spead AI, deployed for the EPCC Division of PT Wijaya Karya. |
| **Period** | Since Oct 2026 |
| **Source** | Private. This repository presents the product; the code is not published. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/features-dark.svg"><img src="assets/features-light.svg" width="100%" alt="What Spead AI Pro for Wijaya Karya does: Tender review form, Verified quotes, PDF and Office reading, Cited Q&A, Knowledge library, Document Studio, Connectors with approval, SSO, 2FA and quotas."></picture>

## The business

Spead AI Pro is the Spead AI deployment for the tender and contract team of the EPCC Division at PT Wijaya Karya (Persero) Tbk. It reads a tender package, fills the tender document review form (Lampiran 2.3) with quotes that are checked against the contract files, and answers questions about the same package with citations. Around that core sits a full workspace: a knowledge library with access labels and confidentiality, Document Studio with an ONLYOFFICE editor and company templates, connectors where any data change waits for a person, an organisation model and usage quotas. It was built and led by Nugraha Labib Mujaddid as Founder & Lead AI Engineer of Spead AI.

### The problem

Before a bid decision, the tender team reviews the contract package and fills a standard review form: contract type, scope, time for completion, securities, payment terms, penalties, liability, insurance, force majeure, disputes and more. Each answer has to point to the clause it comes from. Done by hand, this means reading long PDFs clause by clause for every tender.

Tender packages are hard to read reliably. General conditions are amended by particular conditions, sometimes in parts A, B and C; some contracts are printed in two language columns; headers and footers repeat on every page; some pages are scanned. A reviewer has to keep track of which version of a clause actually applies.

A general AI tool is risky here. A quote that is not really in the contract, or a number that differs by one digit, is worse than no answer, because the review feeds a commercial decision. The design principle in the code is to reject a correct quote rather than let a wrong one through, and to let a person decide.

Contract documents are confidential. Each employee's assistant must read only what that employee is allowed to read, and any action that sends or changes data outside the workspace has to be approved by a person.

### Who uses it

| Role | What they do with it |
| --- | --- |
| **Tender staff** | Creates the tender project, uploads the agreement and appendices, starts the review, checks flagged items and edits answers. |
| **Tender and contract manager** | Approves items and the whole review, or returns it with notes; can also hold the company admin role. |
| **Legal staff** | Asks questions about clauses across the package and drafts letters and minutes in Document Studio. |
| **Division head and directors** | Read project reviews, ask the assistant for summaries and approve or sign documents routed to them. |
| **Company admin** | Maintains units, positions, labels, connectors, templates and quotas for the division. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/before-after-dark.svg"><img src="assets/before-after-light.svg" width="100%" alt="Before and after: Read the whole package to fill each review item becomes Spead drafts every item with a quote and a clause reference; Trust or re-check every quote by hand becomes Each quote gets a status; only verified quotes are shown as verified; Track general versus particular conditions mentally becomes The reader splits files into clauses and labels the agreement and appendix letters; Ask a colleague where a clause is becomes Ask the package and open the cited page; Shared folders with unclear access becomes Labels and confidentiality decide what each person's assistant can read; Letters retyped on old letterheads becomes Company templates with locked letterhead, numbering and signing route."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/journey-dark.svg"><img src="assets/journey-light.svg" width="100%" alt="How work flows: Create the tender project, Upload the package, Let Spead read, Start the review, Fill and check, Review flagged items, Approve or return, Export and ask."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/value-dark.svg"><img src="assets/value-light.svg" width="100%" alt="What it changes: 6 quote statuses, from verified to not found, checked before a person sees an answer; 0.933 Recall@5 with hybrid search and reranking, up from 0.867 with keyword search (synthetic test set); 0.909 MRR@10 with hybrid search and reranking, up from 0.824 with keyword search (synthetic test set); 0.2 to 0.6 Recall@5 on cross-language queries (Indonesian question, English clause or the reverse), keyword versus hybrid with reranking; 99 API test files run on an in-memory database with two companies."></picture>

### Model and status

Spead AI Pro is a deployment of Spead AI for one organisation: the workspace, assistants and data belong to the Wijaya Karya EPCC Division, while Spead AI builds and operates the product. The tender review module is switched on per company as a package, so the same product can run for organisations that do not need it.

Status: pilot since October 2026. The workspace was demonstrated to the tender and contract team with fictional demo cases, and the review form, quote checking and package Q&A are the core of the pilot. Every name, project and number in this showcase is synthetic.

## Product tour

### 1. Sign-in and account security

People sign in with a work email and password or single sign-on, and can turn on two-step verification. The account page shows signed-in devices so a person can sign out the ones they do not recognise.

- Work email and password, Google sign-in, and company single sign-on
- Two-step verification with an authenticator app and backup codes
- Signed-in devices with remote sign-out
- Password and email changes notify the account owner

<img src="assets/screens/01-sign-in.jpg" width="100%" alt="Sign-in page with password sign-in and single sign-on buttons, in English or Indonesian.">

<sub>Sign-in page with password sign-in and single sign-on buttons, in English or Indonesian.</sub>

<p><img src="assets/screens/24-account-security.jpg" width="100%" alt="Account settings: password, email, two-step verification and signed-in devices (email and addresses blurred)."></p>

<sub>Account settings: password, email, two-step verification and signed-in devices (email and addresses blurred).</sub>

### 2. AI Partner

Every employee has a personal assistant that knows their unit and position and reads only the documents they may open. Suggested questions come from the person's own documents, and the assistant's tone and form of address can be set by the employee within limits set by the company.

- One assistant per employee, prepared automatically for new accounts
- Suggested questions based on recent documents, such as comparing a clause with a template
- Personal settings: name, form of address, personality, with a sample answer
- Company and position rules shown as locked parts

<img src="assets/screens/02-ai-partner-home.jpg" width="100%" alt="AI Partner home on the local stack, where the assistant service was not connected, so it shows that the assistant is getting ready.">

<sub>AI Partner home on the local stack, where the assistant service was not connected, so it shows that the assistant is getting ready.</sub>

<p><img src="assets/screens/23-my-assistant.jpg" width="100%" alt="My assistant: how it addresses the user and its personality, with a sample answer."></p>

<sub>My assistant: how it addresses the user and its personality, with a sample answer.</sub>

### 3. Knowledge library

The library holds both reference documents and tender packages. Every document has a confidentiality level and labels that link it to positions, units or levels. One access filter decides what each person's assistant may read.

- Confidentiality levels: normal, restricted, confidential and highly confidential
- Labels for all employees, a unit and its sub-units, a position or a level
- Per-document switch for whether Spead uses it when answering
- Pages read, approval and file role shown in the detail view
- Deleted documents stay in a 30-day trash

<img src="assets/screens/03-knowledge-library.jpg" width="100%" alt="Knowledge with synthetic documents: status, who can use each one, confidentiality chips and usage in the last 30 days.">

<sub>Knowledge with synthetic documents: status, who can use each one, confidentiality chips and usage in the last 30 days.</sub>

<p><img src="assets/screens/04-knowledge-labels.jpg" width="49%" alt="Labels created for this demo: all employees, the tender and contract team, and managers and above."> <img src="assets/screens/05-knowledge-document.jpg" width="49%" alt="Detail of a synthetic contract appendix: pages read, approval, file role with appendix letter, and who can use it."></p>

<sub>Left: Labels created for this demo: all employees, the tender and contract team, and managers and above. · Right: Detail of a synthetic contract appendix: pages read, approval, file role with appendix letter, and who can use it.</sub>

### 4. Tender package and review

A tender package is a project in Knowledge with its agreement and appendices. From Doc Assistant the team starts Review a tender package, sees a plan with files, pages and time, and runs the review as a background job that can be left and resumed.

- Project details: employer, tender number, location, owning unit and members
- File roles: agreement, appendix A, B and so on, or other
- Plan before running: number of files, pages and estimated minutes
- Job stages: queued, reading files, reading tables, filling items, checking quotes
- Review versions with submit, approve and return, and export to Word, PDF and Excel

<img src="assets/screens/06-tender-package.jpg" width="100%" alt="A synthetic tender package in Knowledge: agreement plus appendices A and B, ready to review.">

<sub>A synthetic tender package in Knowledge: agreement plus appendices A and B, ready to review.</sub>

<p><img src="assets/screens/07-doc-assistant-tasks.jpg" width="49%" alt="Doc Assistant with the ready-made tasks, including Review a tender package."> <img src="assets/screens/08-tender-review-plan.jpg" width="49%" alt="Review setup: the chosen package and the plan Spead will follow before filling the form."></p>

<sub>Left: Doc Assistant with the ready-made tasks, including Review a tender package. · Right: Review setup: the chosen package and the plan Spead will follow before filling the form.</sub>

### 5. Contract reader and quote checking

Two pieces of deterministic code sit around the AI. The reader turns PDFs into a clause map so every answer can cite a clause. The checker tests every quote against the files and gives it one of six statuses before a reviewer sees it.

- Clause segmentation such as 6., 6.7.1 and (A), including layered A, B and C conditions
- Two-column English and Indonesian pages split, repeated headers and footers removed
- OCR for scanned pages; Word, Excel and PowerPoint are read too
- Word-bounded matching, so 14 days never matches inside 114 days
- Only whole or proven quotes count as verified; the rest are flagged

<img src="assets/screens/09-clause-map.png" width="100%" alt="Clause map produced by the product's reader from the synthetic package, run locally.">

<sub>Clause map produced by the product's reader from the synthetic package, run locally.</sub>

<p><img src="assets/screens/10-quote-checker.png" width="100%" alt="The product's quote checker on six hand-typed test quotes against the synthetic package: all six statuses."></p>

<sub>The product's quote checker on six hand-typed test quotes against the synthetic package: all six statuses.</sub>

### 6. Document Studio

Document Studio produces letters, minutes, reports and presentations in the company's format. Built-in templates cover common Indonesian official documents, and companies add their own. Documents open in an ONLYOFFICE editor and move through initials, approval and signature.

- Official letters, internal memos, decrees, circulars, assignment letters, official reports, minutes and agreements
- Built-in templates plus company templates with locked parts
- Editing in ONLYOFFICE through a bridge plugin
- Sharing, comments, versions and a 30-day trash

<img src="assets/screens/11-studio-home.jpg" width="100%" alt="Document Studio home: describe a document, or start from official documents, a presentation, a report or an infographic.">

<sub>Document Studio home: describe a document, or start from official documents, a presentation, a report or an infographic.</sub>

<p><img src="assets/screens/12-studio-document-types.jpg" width="49%" alt="Types of letters and official documents available to start from."> <img src="assets/screens/13-template-studio.jpg" width="49%" alt="Template Studio with the built-in templates ready to use."></p>

<sub>Left: Types of letters and official documents available to start from. · Right: Template Studio with the built-in templates ready to use.</sub>

### 7. Letterheads, numbering and signatures

The company identity is set once and reused: letterhead, logo, colours and fonts, signature, and letter number formats per document type. Numbers are assigned when a document is signed, in sequence per type and unit.

- Company details and letterhead library
- Brand colours and fonts for presentations, reports and infographics
- Number formats with sequence, unit code, Roman month and year
- Yearly reset and a numbering officer per format
- Personal signature uploaded or drawn, used only when that person signs

<img src="assets/screens/14-letterhead-brand.jpg" width="100%" alt="Letterhead and logo: company details, letterhead library, colours and fonts.">

<sub>Letterhead and logo: company details, letterhead library, colours and fonts.</sub>

<p><img src="assets/screens/15-letter-numbering.jpg" width="100%" alt="Letter number formats per document type, assigned automatically at signing."></p>

<sub>Letter number formats per document type, assigned automatically at signing.</sub>

### 8. Connectors with approval

Connectors let assistants reach office systems such as Microsoft 365, Google, Odoo, databases, REST services and MCP servers. Admins choose which positions may use each one and whether data may change; a change always becomes an approval request for its owner.

- Catalog grouped by category, with read-only database connectors
- Per connector: on for the company, all or specific positions
- May change data: read only, or yes with approval every time
- Credentials kept in an encrypted vault; outbound calls pass a network guard
- Employees request access and admins decide

<img src="assets/screens/16-connectors-catalog.jpg" width="100%" alt="Connector catalog by category, nothing turned on yet in the local stack.">

<sub>Connector catalog by category, nothing turned on yet in the local stack.</sub>

<p><img src="assets/screens/17-connector-setup.jpg" width="100%" alt="Setting up Odoo: positions that may use it, and whether the assistant may change data, with approval every time."></p>

<sub>Setting up Odoo: positions that may use it, and whether the assistant may change data, with approval every time.</sub>

### 9. Organisation and assistants

The organisation model drives everything else: units, positions and people decide what each assistant may read and how it behaves. Admins can start from structure templates, then refine roles, limits and document access per position.

- Tree of units, positions and people, with assistant sync status
- Position role: how to work, main tasks and things never to do
- Document access per position through knowledge labels
- Structure templates for private companies, state-owned enterprises, government agencies and more
- Role templates to fill a position in one click

<img src="assets/screens/18-organisation-tree.jpg" width="100%" alt="Organisation tree of the demo company with generic demo accounts.">

<sub>Organisation tree of the demo company with generic demo accounts.</sub>

<p><img src="assets/screens/19-position-role.jpg" width="49%" alt="A position's role: how to work, main tasks and rules the assistant never breaks, with role templates."> <img src="assets/screens/20-position-document-access.jpg" width="49%" alt="Document access for the Legal staff position, set through knowledge labels."></p>

<sub>Left: A position's role: how to work, main tasks and rules the assistant never breaks, with role templates. · Right: Document access for the Legal staff position, set through knowledge labels.</sub>

<p><img src="assets/screens/21-structure-templates.jpg" width="100%" alt="Structure templates, previewed before they are applied."></p>

<sub>Structure templates, previewed before they are applied.</sub>

### 10. Usage and quotas

AI work is counted as questions against a monthly company quota and a daily personal limit. The usage page forecasts whether the quota will last, lists people who asked for more, and shows adoption.

- Monthly forecast with a chart and a table view
- Requests for more quota approved by the admin
- Adoption: often, regularly, rarely, never
- Breakdown by unit, position, person and feature, with export

<img src="assets/screens/22-usage-quota.jpg" width="100%" alt="Usage page on the fresh demo workspace: quota forecast, requests and adoption.">

<sub>Usage page on the fresh demo workspace: quota forecast, requests and adoption.</sub>

## For developers

### Architecture

Spead AI Pro is a TypeScript monorepo with npm workspaces. The API (apps/wika-api) runs on Node 22 with Fastify 5 and PostgreSQL through pg, with PGlite for tests and local runs. The web app (apps/wika-app) is the approved Spead AI interface, assembled from vanilla JavaScript modules into one bundle that runs under a strict content security policy, with History API routing and a three.js mascot. A first React 19 and Vite release of the review screen lives in apps/wika-web, and apps/wika-onlyoffice-plugin bridges the ONLYOFFICE editor.

Shared packages keep the core logic testable: pembaca reads PDF (pdf.js), Word, Excel and PowerPoint and builds the clause map; tinjauan defines the review form schema and grades filled forms against answer keys; kontrak holds zod schemas shared by API and web; ekspor writes DOCX and PDF; email renders bilingual templates.

The API is multi-tenant: every business table carries the company id and queries go through a tenant-scoped database helper. Long work runs as jobs: PDF parsing in worker threads, the review job in a queue with visible stages, and email through an outbox that can run in a separate process.

Knowledge search is hybrid: BM25 keyword search plus vector search with e5-small embeddings stored as encrypted int8 vectors, then a multilingual reranker, all running locally through onnxruntime-node, with OCR for scanned pages.

Each employee has their own assistant. Assistant tools (search knowledge, get a document, compare documents, list and run connectors, create schedules, save memory) call back into the API with an HMAC-SHA256 signature and a one-time nonce, and run with the rights of the employee who owns the assistant.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg"><img src="assets/architecture-light.svg" width="100%" alt="How Spead AI Pro for Wijaya Karya is built."></picture>

### Data model

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/data-model-dark.svg"><img src="assets/data-model-light.svg" width="100%" alt="Data model: perusahaan, unit / posisi / pengguna, label / label_sasaran, berkas, proyek / anggota_proyek, tinjauan / butir_tinjauan, pekerjaan, analisa, studio_dokumen / studio_template / studio_kop, konektor_sambungan / konektor_aksi_tertunda, kuota_periode / buku_pemakaian, riwayat."></picture>

### Key flows

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-1-dark.svg"><img src="assets/flow-1-light.svg" width="100%" alt="Reading a tender package: The file is checked by content, not by name; tender packages accept PDF only. Then A worker thread parses pages with pdf.js, removes repeated headers and footers and splits two-language columns. Then Clauses and sub-items are segmented, including layered A, B and C conditions, and labelled with the file role. Then Scanned pages go through OCR. Then The text is indexed for keyword and vector search, encrypted at rest."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-2-dark.svg"><img src="assets/flow-2-light.svg" width="100%" alt="Filling the review form: The user picks a package in Doc Assistant and sees the plan. Then The job moves through queued, reading files, reading tables, filling items and checking quotes. Then The AI drafts each item as quote and summary segments with clause references. Then The checker tests every quote and assigns one of six statuses. Then Reviewers approve per item, submit, and a manager approves or returns; the review exports to Word, PDF or Excel."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-3-dark.svg"><img src="assets/flow-3-light.svg" width="100%" alt="Answering from Knowledge: The employee asks their assistant. Then The assistant calls the knowledge search tool with a signed request. Then The API verifies the signature and nonce and applies the employee's access filter. Then Hybrid search and reranking return passages, and the answer carries numbered sources."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-4-dark.svg"><img src="assets/flow-4-light.svg" width="100%" alt="Connector action with approval: The assistant proposes a change in an external system. Then The API stores it as a pending action and shows an approval card to its owner. Then On approval, the call runs with vault credentials through the outbound network guard. Then The result and the decision are written to the audit history."></picture>

### Security

- Passwords are hashed with argon2id; sessions use HttpOnly cookies with the __Host- prefix over HTTPS and a CSRF header on every change.
- Two-step verification with TOTP and backup codes; Google sign-in and per-company single sign-on through OpenID Connect.
- Sign-in attempts are rate limited per IP, with a lockout per email and IP after repeated failures.
- Files, search indexes and vectors are encrypted at rest, with separate keys for files, data and backups.
- Connector credentials sit in an AES-GCM vault with keys derived by HKDF, and outbound requests pass a guard against server-side request forgery.
- Assistant tool calls are signed with HMAC-SHA256 and a one-time nonce and run with the owner's rights; data-changing actions need a person's approval.
- One access filter decides what any assistant may read, and audit and usage tables are append-only at the database level.
- Error messages shown to users come from error codes in two languages; raw server messages are never displayed.

### Quality

- 99 API test files run with node --test on an in-memory PGlite database that holds two companies, so tenant leaks show up as failures.
- Playwright suites run the real web app against a real local API stack, without mocks.
- A parity test compares the assembled web app with the approved prototype, including screenshots.
- A search evaluation on a synthetic set of 16 documents, 104 passages and 45 queries measured Recall@5 of 0.867 for keyword search, 0.911 for hybrid search and 0.933 with reranking, and MRR@10 of 0.824, 0.859 and 0.909.
- An automatic grader in the tinjauan package scores filled review forms against answer keys.

### Deployment and operations

Runs on a Linux server under systemd with nginx, behind a CDN; the previous address redirects permanently.

The ONLYOFFICE document server runs in a rootless container on its own subdomain.

The assistant runtime listens on the loopback interface only.

Local search and OCR models are installed read-only on the server.

Daily encrypted backups; database migrations are tested on a copy before each release.

### Decisions

| Decision | Why |
| --- | --- |
| Reject rather than pass | The checker would rather flag a correct quote for a person than show a quote with a different number as verified. |
| Deterministic code around the AI | Reading clauses and checking quotes are plain code with tests, so the AI only drafts and every claim can be traced to a clause. |
| One access filter | A single function decides what an assistant may read, so search, Q&A and tools cannot drift apart on permissions. |
| Local search models | Embeddings, reranking and OCR run on the server, which keeps document text inside the deployment and made the search measurable with an evaluation set. |
| Signed tool calls with the owner's rights | An assistant cannot do more than its employee could, and a replayed request is rejected. |
| Approval for every data change | Connectors default to read only; a change becomes an approval request so a person stays accountable. |
| Approved prototype as the frontend | The interface is assembled from the approved Spead AI prototype and checked for parity, so what the client saw is what ships. |
| PGlite in tests | The same SQL runs in memory with two companies per test, which makes tenant isolation testable on every run. |

### Built with

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg"><img src="assets/stack-light.svg" width="100%" alt="Spead AI Pro for Wijaya Karya stack."></picture>

### Engineering highlights

- Every quote the AI cites is checked against the source text and gets one of six statuses before a person sees it.
- A single access filter decides what each person's assistant can read, so the AI sees only what that person may see.
- Agent tool calls are signed with HMAC-SHA256 and a one-time nonce, and run with the rights of the employee who owns the agent.
- Connector credentials sit in an AES-GCM vault, outbound traffic goes through an SSRF guard, and data-changing actions need human approval.
- On a synthetic test set of 16 documents and 45 queries, Recall@5 rose from 0.867 with keyword search to 0.933 with hybrid search and reranking.

## Related

- [Spead AI](https://github.com/nugrahalabib/spead-ai-showcase)
- [HC Platform for Wijaya Karya](https://github.com/nugrahalabib/wika-hc-platform-showcase)
- [Q-NEXUS for Wijaya Karya](https://github.com/nugrahalabib/wika-q-nexus-showcase)
- [All my work on GitHub](https://github.com/nugrahalabib)

---

<sub>Built by [Nugraha Labib Mujaddid](https://github.com/nugrahalabib). This page describes a private codebase; questions about the product or a demo are welcome at [nugrahalabib@gmail.com](mailto:nugrahalabib@gmail.com).</sub>
