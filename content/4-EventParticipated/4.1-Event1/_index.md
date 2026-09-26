---
title: "Build-a-thon Kickoff - Code the Future with CMC Global"
date: 2026-09-26
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Event Report: “Build-a-thon Kickoff - Code the Future with CMC Global”

---

### 1. General Event Overview

| Field | Details |
| :--- | :--- |
| **Event Name** | **Build-a-thon Kickoff: Code the Future with CMC Global** |
| **Date** | September 26, 2026 |
| **Participation Mode** | In-Person (Offline at event venue) |
| **Organizer** | **CMC Global** in collaboration with AWS Cloud Community |
| **Role** | Attendee & Prospective Competitor |

---

### 2. Keynote Speakers & Experts

* **Mr. Truong** – *Tech Lead, CMC Global*: Technical lead responsible for the in-depth architectural breakdown of the AI Incident Response Bot addressing cross-timezone operational challenges.
* **Ms. Nhan** – *Marketing & Talent Acquisition Representative, CMC Global*: Provided comprehensive insights into global markets, career pathways, organizational culture, and the **CMC Job Fair**.

---

### 3. Event Objectives & Background

1. **Launch the Build-a-thon Competition:** Provide a collaborative innovation platform for students and aspiring engineers to tackle real-world digital transformation challenges.
2. **Promote Cloud-Native & Generative AI Solutions:** Showcase enterprise case studies on integrating Large Language Models (LLMs) into production-grade operations.
3. **Expand Career Pathways (CMC Job Fair):** Share recruitment pipelines, structured Fresher/Intern programs, and opportunities within global delivery centers.
4. **Disseminate Operational Engineering Insights:** Demonstrate how seasoned engineers overcome cross-timezone operational bottlenecks in multinational service delivery.

---

### 4. In-Depth Technical Breakdown & Enterprise Case Study

#### 4.1. CMC Global Overview & Career Opportunities (CMC Job Fair)
* **Global Footprint & Market Expansion:** CMC Global stands as one of Vietnam's leading technology services providers, delivering digital transformation solutions to strategic markets across **Australia, Japan, South Korea, Singapore, Europe, and the United States**.
* **Talent Development:** The organization maintains a strong commitment to mentoring junior talent, offering structured career pathways and early access to large-scale enterprise engagements.
* **Agile & Multinational Work Culture:** Engineers operate within diverse, multicultural environments requiring both technical rigor and effective cross-timezone coordination.

---

#### 4.2. Enterprise Problem Statement: The Australia Time-Zone Dilemma
During the technical keynote, Mr. Truong (Tech Lead) analyzed a critical operational dilemma faced by managed services teams:

* **Context:** CMC Global manages and maintains mission-critical production workloads for enterprise partners and major clients based in **Australia**.
* **The Core Pain Point:** Australian business hours precede Vietnam by approximately 3 to 4 hours. When Australian clients experience urgent system anomalies or high-severity incidents (P1/P2) early in their morning, it corresponds to late-night or pre-dawn hours in Vietnam.
* **Consequences of Manual On-Call Triage:**
  * Lack of immediately available overnight engineers to acknowledge incoming incident alerts.
  * Increased Mean Time to Acknowledge (MTTA), leading to Service Level Agreement (SLA) breaches.
  * Escalated client anxiety due to the absence of immediate status confirmation and initial diagnostic feedback.

---

#### 4.3. Architectural Solution: Autonomous AI Incident Bot via Claude Kit & Slack Socket Mode
To permanently solve this operational bottleneck without overwhelming engineering staff, CMC Global’s engineering team architected and deployed an **Intelligent Automated Incident Triage & Diagnosis Bot**.

```mermaid
flowchart TD
    subgraph Australia["Australian Clients & Partners"]
        User[Client / Automated Alert System] -->|Dispatches Incident Alert| SlackChannel[Slack Incident Channel]
    end

    subgraph SecurityBoundary["CMC Global Secure Infrastructure"]
        SlackChannel <-->|Bidirectional WebSockets (Slack Socket Mode)| BotCore[AI Incident Bot Engine]
        BotCore -->|Queries Context & Prompt| ClaudeKit[Custom Claude Kit Framework]
        ClaudeKit <-->|LLM Inference & Log Analysis| ClaudeAPI[Anthropic Claude Core Engine]
        ClaudeKit -->|System Persona / Soul Instructions| SoulConfig[Soul Persona Controller]
    end

    subgraph Operations["Vietnam Engineering Operations"]
        BotCore -->|Instant Automated Mitigation & Acknowledgment| SlackChannel
        BotCore -->|Dispatches Root-Cause Diagnostic Summary| Engineer[Vietnam On-Call Engineers]
    end
```

Key technical pillars implemented:

1. **Custom Claude Kit Framework:**
   - CMC Global engineers designed a modular wrapper framework around **Anthropic's Claude API**.
   - The framework orchestrates session history, dynamic context compression, prompt templates, and token cost optimization when interfacing with Claude models.

2. **Secure Communication via Slack Socket Mode:**
   - Rather than relying on traditional public HTTP webhooks (which necessitate exposing public IPs, opening inbound firewall ports, and configuring NAT gateways), the bot utilizes **Slack Socket Mode**.
   - This mechanism establishes a persistent, secure bidirectional WebSocket connection from inside the corporate private infrastructure out to Slack's backend, guaranteeing that proprietary incident logs and system metrics never transit unprotected public endpoints.

3. **Bot Persona & "Soul" Orchestration:**
   - Specialized system instructions ("Soul" prompt) guide the bot to act as a seasoned Level-2 Support Engineer: maintaining a calm, empathetic, and highly analytical tone.
   - The bot autonomously ingests raw stack traces, extracts error codes, correlates findings against internal runbooks, and proposes immediate workaround steps while notifying local on-call engineers for subsequent handover.

---

### 5. Outcomes & Key Takeaways

| Dimension | Acquired Competency |
| :--- | :--- |
| **Technical Proficiency** | Mastered the mechanics of enterprise AI bots, **Slack Socket Mode** security architecture, and LLM abstraction via custom SDK wrappers. |
| **Architectural Mindset** | Learned how to design scalable, cost-effective automation systems to resolve global operational bottlenecks and safeguard SLAs. |
| **Career Readiness** | Gained firsthand clarity on CMC Global's hiring criteria and the core skill sets needed for Cloud and AI engineering roles. |
| **Professional Soft Skills** | Observed how experienced leaders articulate technical solutions clearly by tying architectural choices directly to business outcomes. |

---

### 6. Actionable Learnings & Application to Internship Project

1. **Business-Centric Engineering:** Technical elegance is meaningless unless it addresses a tangible operational bottleneck.
2. **Integration into Final Workshop Project (Part 5):**
   - Inspired by CMC Global's case study, I plan to incorporate an automated monitoring and notification workflow on **AWS** combining **Serverless services (AWS Lambda, Amazon EventBridge, DynamoDB)** with **Generative AI (Amazon Bedrock / Claude)** into my final project.
3. **Security-First Architecture:** Emphasize zero-trust network boundaries, avoiding exposed public endpoints in alignment with the **AWS Well-Architected Framework (Security Pillar)**.

---

### 7. Event Participation Gallery

{{% notice tip %}}
*Clear-face check-in evidence and visual documentation from the Build-a-thon Kickoff event:*
{{% /notice %}}

![Event Backdrop Check-in](/images/4-event/checkin-backdrop.png)
*Figure 1: Check-in in front of the event backdrop "Build-a-thon: Code the Future with CMC Global - AWS First Cloud Journey"*

![Technical Presentation Slide](/images/4-event/presentation-slide.png)
*Figure 2: Keynote speaker presenting technical architecture: Slack Socket Mode, Claude Code, and AWS*

![Event Venue Atmosphere](/images/4-event/event-venue.png)
*Figure 3: Overview of the event hall packed with participating students and developers*
