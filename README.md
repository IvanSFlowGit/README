# Ivan Skachek [https://linktr.ee/Ivansflow]

I help fintech, ecommerce and SaaS teams deploy **reliable, auditable AI** for payments, compliance, and operations.  
I build LangGraph agents, Python services, and automation pipelines where **deterministic rules decide anything that touches money** and the model only drafts language.

Flagship project: **[PayPilot](https://paypilot.fly.dev)** – an AI dunning agent that recovers failed subscription payments with full auditability and no PII stored.

More work: **[streamflow.solutions](https://streamflow.solutions)**  
Contact: [nonfungibleivan@gmail.com](mailto:nonfungibleivan@gmail.com) | [LinkedIn](https://www.linkedin.com/in/ivansflow/) | [Calendly](https://calendly.com/nonfungibleivan/30min)

---

## Who I help

I work with:

- SaaS and ecommerce teams dealing with failed payments, subscription churn, or revenue leakage.
- Fintech and payments companies that need auditable AI for dunning, collections, or risk workflows.
- Compliance and AML teams that want AI-assisted triage without handing decisions to a model.
- Agencies and consultancies that need a technical partner to deliver AI features for their clients.

My preferred pattern is simple: deterministic rules handle money, risk, and compliance; AI handles language, retrieval, and analyst assistance.

---

## Running projects

### [PayPilot – AI dunning agent for subscription billing](https://paypilot.fly.dev)

A 7‑node LangGraph agent with RAG over a dunning playbook, served through a FastAPI API and deployed on Fly.io with Docker, CI, and health checks.

- Retry strategy and all money‑affecting decisions live in a **deterministic rules table**.  
- The model only drafts email/SMS language; rules decide actions, so behavior is explainable from a row rather than a transcript.  
- The full test suite runs offline with the model and retriever mocked: no API key, no network, including adversarial prompt‑injection and PII‑masking cases in CI.  
- Untrusted input is fenced and outputs fail closed.  
- Closed‑loop recovery proven on Stripe test mode: failed invoice → recovery email → paid, matched by invoice ID, with idempotency, send caps, and a metrics endpoint.  
- GDPR‑ready by architecture and verified in CI: no name or email column stored, PII masked before the model, append‑only audit log, erasure proven by test, EU AI Act Article 50 disclosure built in.

**Live demo:** [paypilot.fly.dev](https://paypilot.fly.dev)  
**Code:** [`github.com/IvanSFlowGit/paypilot`](https://github.com/IvanSFlowGit/paypilot)

---

## Selected contributions

### [LangGraph error handler matrix](https://github.com/IvanSFlowGit/langgraph-error-handler-matrix)

A reproducible test matrix isolating a defect in LangGraph’s error handling, with a negative control for every case so a pass cannot be explained by the test itself.

- 24 handled‑path cases plus 6 over‑suppression controls.  
- Independently reproduced by another engineer on [the issue](https://github.com/langchain-ai/langgraph/issues/8277).

### [AML alert‑triage demo](https://aml-triage-demo.vercel.app)

Live demo on the same deterministic‑core pattern:

- A rules engine scores each alert so the score is auditable and reproducible.  
- The model writes the analyst narrative but **never the decision**.  
- Synthetic data only.

**Demo:** [aml-triage-demo.vercel.app](https://aml-triage-demo.vercel.app)  
**Code:** [`github.com/IvanSFlowGit/aml-triage-demo`](https://github.com/IvanSFlowGit/aml-triage-demo)

### Revend – revenue recovery for ecommerce

A revenue-recovery project for abandoned carts and post-purchase leakage:

- Different message per shopper matched to their cart and hesitation, rather than one blanket discount.
- Same deterministic-core pattern as PayPilot: rules decide offers, model drafts copy.
- Shopify App Store publication is planned; this project is not currently presented as a live public listing.

---

## How I work

- **Deterministic core, AI on top:** rules and scoring handle risk, money, and compliance; the model explains and drafts.  
- **Evaluation with controls:** where a result could be explained by the test rather than the code, there is a negative control published next to the result.  
- **Superseded numbers are retired, not edited:** a figure quoted in an old commit stays readable as the number that was true then.  
- **Client‑facing delivery:** discovery and scoping calls, findings walkthroughs, end‑to‑end ownership from requirements to production.

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat&logo=meta&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Fly.io](https://img.shields.io/badge/Fly.io-24175B?style=flat&logo=flydotio&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-FF6D5A?style=flat&logo=n8n&logoColor=white)
![Make](https://img.shields.io/badge/Make-000000?style=flat&logo=make&logoColor=white)

This is what I would reach for, not everything I have touched.

---

## Contact

- Email: [nonfungibleivan@gmail.com](mailto:nonfungibleivan@gmail.com)
- LinkedIn: [linkedin.com/in/ivansflow](https://www.linkedin.com/in/ivansflow/)
- Website: [streamflow.solutions](https://streamflow.solutions)
- Book a 30-minute call: [calendly.com/nonfungibleivan/30min](https://calendly.com/nonfungibleivan/30min)

I’m open to collaborations involving payments, compliance, ecommerce revenue recovery, and reliable AI automation.
