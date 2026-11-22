# autonomous-personal-os
Autonomous Multi-Agent Personal Operating System built with OpenBot, Notion API, and local LLMs.
# 🚀 Autonomous Multi-Agent Personal Operating System

An autonomous, localized, multi-agent personal operating system designed to automate academic tracking, multi-wallet personal finance, hardware diagnostics, and daily logistics for engineering students and developers.

Built by **[Akhmad Muwaffaq](https://github.com/affaxx-dev)** (Computer Engineering student, D4 TRK Polines).

---

## 🏗️ System Architecture

The ecosystem adopts an **Agentic Chief-of-Staff Pattern** running on the OpenBot engine. Rather than relying on a single monolithic prompt, specialized AI teammates communicate via **asynchronous message passing** (`send_message`, `expectsReply`), execute deterministic Python CLI bridges, and trigger event-driven morning routines.

```mermaid
flowchart TD
    User(["👤 User (Akhmad Muwaffaq)"])
    WA["📱 WhatsApp Orchestrator (Mobile Access Bridge)"]

    subgraph Core ["Autonomous Agentic Ecosystem"]
        Jaen["⭐ Jaen (Chief of Staff & Daily Logistics)"]
        Anton["🎓 Anton (Academic & TRK Coursework)"]
        Fiskal["💰 Fiskal (Financial Manager & Notion Sync)"]
        Eko["💻 Eko (SysAdmin, Docker & Hardware Monitor)"]
        Coach["🏃‍♂️ Coach (Trainer & Recovery Specialist)"]
        Asep["🛵 Asep (Vehicle & Odometer Maintenance)"]
        Pixel["🎨 Pixel (UI/UX & KosMuter OS Design)"]
    end

    subgraph Tools ["Real-World Integration & APIs"]
        NotionAPI[("Notion REST API (Finances & Courses)")]
        LocalCLI["Local System CLI (Python / Shell / Docker)"]
        EDF["EDF Kitchen Inventory (kulkas.md)"]
        Cron["Cron Routine Engine (06.00 AM Daily Briefing)"]
    end

    User <--> WA
    WA <--> Jaen
    User <--> Jaen

    Jaen <== "Asynchronous Message Passing" ==> Anton
    Jaen <== "Asynchronous Message Passing" ==> Fiskal
    Jaen <== "Asynchronous Message Passing" ==> Eko
    Jaen <== "Asynchronous Message Passing" ==> Coach
    Jaen <== "Asynchronous Message Passing" ==> Asep
    Jaen <== "Asynchronous Message Passing" ==> Pixel

    Jaen --> Cron
    Jaen --> EDF
    Fiskal --> NotionAPI
    Anton --> NotionAPI
    Eko --> LocalCLI
