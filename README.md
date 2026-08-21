Challenge 3 – Smart Rann of Kutch Eco-Tourism & Carrying Capacity Planner

Domain: Tourism

The Challenge

The Rann Utsav and Kutch region attract heavy seasonal tourist inflow, straining fragile

desert ecology, local water resources, and infrastructure, while visitors lack guidance on

sustainable and lesser-known eco-tourism alternatives.

Objective

Build Agentic AI solutions that manage tourist load, recommend sustainable travel

itineraries, and protect ecologically sensitive zones in Kutch and surrounding regions.

Suggested AI Agents

• Tourist Load Forecasting Agent

• Sustainable Itinerary Recommendation Agent

• Ecological Carrying Capacity Agent

• Local Artisan & Community Linkage Agent

• Tourism Impact Dashboard Agent

Technology to be used – IBM Bob + IBM Granite LLM + IBM cloud
# RannSmart AI
## Smart Rann of Kutch Eco-Tourism & Carrying Capacity Planner

> **Hackathon Project** | IBM Granite AI × IBM watsonx.ai × IBM Bob

---

## Overview

**RannSmart AI** is an agentic AI web application that intelligently manages tourist loads, protects ecologically sensitive areas, recommends sustainable travel itineraries, and supports local Kutch artisan communities.

Built for the hackathon challenge: *Smart Rann of Kutch Eco-Tourism & Carrying Capacity Planner*.

### Core Problem
The Rann of Kutch receives massive seasonal tourist traffic (especially during Rann Utsav), causing:
- Tourist overcrowding at iconic destinations like Dhordo & Kala Dungar
- Pressure on water and waste infrastructure  
- Environmental damage to fragile ecosystems
- Limited economic benefits reaching local artisan communities

### RannSmart AI's Solution: 5 Agentic AI Modules

| Agent | Role |
|-------|------|
| **Agent 1** — Tourist Load Forecasting | Predict visitor demand by date, season, and Rann Utsav period |
| **Agent 2** — Ecological Carrying Capacity ⭐ | THE critical agent — determines ecological safety limits per destination |
| **Agent 3** — Sustainable Itinerary | Generate personalized, eco-safe itineraries that redistribute tourist load |
| **Agent 4** — Local Artisan & Community | Connect tourists to local craft families and community experiences |
| **Agent 5** — Tourism Impact Dashboard | Admin overview with AI-generated intervention recommendations |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **AI Reasoning** | IBM Granite 13B Instruct v2 via IBM watsonx.ai |
| **Backend** | Node.js + Express.js |
| **Frontend** | Vanilla HTML/CSS/JavaScript (no build step required) |
| **Charts** | Chart.js |
| **Development** | IBM Bob AI |

---

## Quick Start

### Prerequisites
- Node.js 18+ 
- npm

### 1. Install Backend Dependencies
```bash
cd rannsmart-ai/backend
npm install
```

### 2. Configure IBM Granite (Optional — app works without it)
```bash
cp .env.example .env
# Edit .env and add your IBM Cloud API key and watsonx.ai Project ID
```

Get credentials at:
- API Key: https://cloud.ibm.com/iam/apikeys
- Project ID: https://dataplatform.cloud.ibm.com/ → Your project → Manage → Details

### 3. Start Backend Server
```bash
cd rannsmart-ai/backend
npm start
# Server starts at http://localhost:3001
```

### 4. Open Frontend
Open `rannsmart-ai/frontend/public/index.html` in your browser.

Or use the backend to serve it:
```
http://localhost:3001
```

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/health` | Health check + Granite config status |
| GET | `/api/destinations` | List all 10 monitored destinations |
| POST | `/api/agent/forecast` | Agent 1: Tourist load forecast |
| GET | `/api/agent/forecast/all` | Agent 1: Bulk forecast all destinations |
| POST | `/api/agent/capacity` | Agent 2: Ecological capacity assessment |
| POST | `/api/agent/itinerary` | Agent 3: Generate sustainable itinerary |
| GET | `/api/agent/artisans` | Agent 4: All artisan listings |
| POST | `/api/agent/artisans/recommend` | Agent 4: Filtered artisan recommendations |
| GET | `/api/agent/dashboard` | Agent 5: Full tourism impact dashboard |

---

## IBM Granite Integration

All 5 agents use IBM Granite 13B Instruct v2 through structured domain-specific prompts:

- **Agent 1**: Seasonal forecast narrative with crowd advisories  
- **Agent 2**: Ecological risk explanation with specific factor breakdown  
- **Agent 3**: Itinerary introduction emphasizing sustainability and community  
- **Agent 4**: Artisan community introduction with cultural context  
- **Agent 5**: Executive dashboard brief with actionable intervention recommendations

If IBM Granite credentials are not configured, all agents fall back to deterministic rule-based analysis — the app remains fully functional.

---

## Destinations Covered

| Destination | Type | Ecological Sensitivity | Status (Peak Season) |
|-------------|------|------------------------|----------------------|
| Dhordo | White Rann | HIGH | 🔴 Over Capacity |
| Kala Dungar | Viewpoint | HIGH | 🔴 Over Capacity |
| Wild Ass Sanctuary | Wildlife | VERY HIGH | 🟡 Moderate |
| Banni Grasslands | Ecosystem | VERY HIGH | 🟢 Safe |
| Hodka | Village/Community | MEDIUM | 🟢 Safe |
| Bhuj | City/Heritage | LOW | 🟢 Safe |
| Mandvi | Coastal | MEDIUM | 🟢 Safe |
| Nirona | Craft Village | LOW | 🟢 Safe |
| Lakhpat | Heritage Fort | MEDIUM | 🟢 Safe |
| Anjar | Heritage Town | LOW | 🟢 Safe |

---

## Artisan & Community Data

8 artisan families/communities with demo listings representing:
- Ajrakh Block Printing (Ajrakhpur/Bhuj)
- Rogan Art — Castor Oil Painting (Nirona)
- Kutchi Embroidery & Mirror Work (Hodka)
- Vankar Woollen Weaving (Bhujodi/Bhuj)
- Copper Bell Making / Ghungroo (Nirona)
- Maldhari Pastoral Experiences (Banni)
- Mandvi Dhow Shipbuilding Heritage
- Dhordo Folk Music & Dance

---

## Disclaimer

> ⚠️ **DEMO DATA NOTICE**: All tourist load figures, carrying capacity values, ecological stress metrics, and artisan details are estimated demo/mock data created for hackathon purposes. These do NOT represent official government statistics or verified field measurements. The application architecture and AI reasoning demonstrate the approach; real deployment would require official data sources from Gujarat Forest Department, Rann Utsav organizers, and local government bodies.

---

## Built With

- **IBM Bob AI** — Development assistant (code generation, architecture)
- **IBM Granite LLM** — AI reasoning and natural language generation
- **IBM watsonx.ai** — Granite model serving platform

---

*Developed for the Smart Rann of Kutch Eco-Tourism Hackathon Challenge