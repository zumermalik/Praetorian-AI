# 🛡️ Praetorian AI
### The "Moneyball" Macro-Engine for Mental Resilience & Strategic Discipline.

![Project Status](https://img.shields.io/badge/Status-Prototype-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Tech](https://img.shields.io/badge/AI-Gemini%203%20Flash-purple)
![Tech](https://img.shields.io/badge/Data-GRID%20Esports-orange)

> *"You have power over your mind - not outside events. Realize this, and you will find strength."* — Marcus Aurelius

## 📖 Overview

**Praetorian AI** is a Category 1 Assistant Coach application that moves beyond simple K/D ratios and heatmap tracking. Instead of focusing on **micro-mechanics** (aim, reaction time), Praetorian analyzes **macro-psychology** and **decision fatigue**.

Inspired by the "Moneyball" approach to sports analytics, Praetorian ingests live match telemetry from the **GRID Data Platform** and uses **Gemini 3 Flash** to detect when a team is "tilting"—deviating from optimal strategy due to stress, economic pressure, or repeated failure.

It answers the critical question coaches ask: *Did we lose because we missed shots, or because our decision-making loop collapsed?*

## ✨ Key Features

### 1. The Mental Fortitude Score (MFS)
A real-time, dynamic metric (0-100) that tracks a team's adherence to "Logical Play" versus "Emotional Play."
* **Logic:** Detecting re-peeks on lost angles, force-buying when probability is <20%, and irregular rotation timings.
* **Visualization:** Displayed via a high-fidelity **Glassmorphism** dashboard.

### 2. The Stoic AAR (After-Action Report)
Unlike traditional scouting reports that list stats, the Stoic AAR uses Agentic AI to narrate the *psychological story* of the match.
* Separates **"Force Majeure"** (Unavoidable loss due to opponent skill) from **"Internal Error"** (Loss due to lack of discipline).
* Provides actionable coaching insights to reset mental state before the next map.

### 3. Economic Efficiency "Tilt" Detection
Correlates player economy usage with win probability drift. Identifies specific rounds where "Hero Buys" (high risk, low reward) signaled the start of a strategic collapse.

## 🏗️ Architecture & Tech Stack

Praetorian was built using a modern Agentic AI architecture, leveraging the **JetBrains AI Assistant (Junie)** for rapid backend prototyping and data schema generation.

| Component | Technology | Description |
| :--- | :--- | :--- |
| **LLM Engine** | **Gemini 3 Flash** | Used for its massive context window to ingest full-match JSON streams and perform causal analysis. |
| **Data Source** | **GRID Esports API** | Live telemetry for League of Legends / VALORANT. |
| **Backend** | **Python (FastAPI)** | High-performance async API to handle websocket streams. |
| **Frontend** | **Next.js 16** | React framework with Server Actions. |
| **Styling** | **Tailwind CSS** | Implementing a "Visibe-style" Glassmorphism UI (dark mode, frosted glass, neon accents). |
| **IDE** | **JetBrains Fleet** | Developed with integrated AI assistance. |

## 🚀 Getting Started

### Prerequisites
* Node.js 22+
* Python 3.12+
* GRID API Key
* Google Gemini API Key

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/yourusername/praetorian-ai.git](https://github.com/yourusername/praetorian-ai.git)
    cd praetorian-ai
    ```

2.  **Setup Backend (Python)**
    ```bash
    cd backend
    python -m venv venv
    source venv/bin/activate  # or venv\Scripts\activate on Windows
    pip install -r requirements.txt
    
    # Create .env file
    echo "GRID_API_KEY=your_key_here" > .env
    echo "GEMINI_API_KEY=your_key_here" > .env
    
    # Run FastAPI server
    fastapi dev main.py
    ```

3.  **Setup Frontend (Next.js)**
    ```bash
    cd ../frontend
    npm install
    
    # Run Development Server
    npm run dev
    ```

4.  **Access the Dashboard**
    Open `http://localhost:3000` to view the command center.

## 🧠 How It Works (The "Agentic" Flow)

1.  **Ingest:** The `GridIngestor` service connects to the game websocket and normalizes the JSON event stream.
2.  **Filter:** A noise-reduction algorithm (based on Logic Diffusion principles) strips out non-tactical data (emotes, cosmetic sprays).
3.  **Analyze:** The filtered stream is chunked and sent to **Gemini 3 Flash**.
    * *Agent 1 (Observer):* Tracks objective reality (Economy, Health, Position).
    * *Agent 2 (Stoic):* Compares reality against "Optimal Play" patterns.
4.  **Render:** The deviation between Agent 1 and Agent 2 generates the **Mental Fortitude Score**, which updates the UI in real-time.

## 🤝 Contribution & Development

### Using JetBrains Junie
This project relies heavily on **Junie** for type safety and Pydantic model generation. If you are contributing, we recommend using IntelliJ IDEA or Fleet.
* **Prompt Tip:** Use `lines 40-120` of `models.py` as context when asking Junie to generate new event schemas.

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🏆 Acknowledgements

* **GRID** for providing the granular telemetry data.
* **JetBrains** for the IDE and AI tooling that accelerated our development velocity.
* **Google DeepMind** for Gemini 3 Flash.

---
*Built with logic, discipline, and code for 2026.*
