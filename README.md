# Social Media Marketing Intelligence Suite

## Project Overview
This repository contains a powerful, automated suite of tools designed to provide marketing agencies with data-driven insights from social media platforms.  

The system automates the process of scraping public posts and ads from **Facebook, Instagram, and TikTok**, then uses AI to analyze the collected content and comments—transforming raw data into actionable market intelligence.  

This suite is designed for **competitive analysis, audience research, content strategy, and R&D**, enabling agencies to build more effective campaigns. Instead of relying on manual collection and subjective analysis, this system offers a **scalable, repeatable, and objective** method for staying ahead of trends and understanding consumer behavior.

---

## How It Works: The Core Workflow

The system runs on a **modular, scalable architecture** that moves data from social platforms into a structured database enriched with AI.  

### 1. Input Queue
- Marketing analysts submit search requests in **Airtable** (e.g., keyword, competitor handle, hashtag, or region).
- The request is added to a queue and triggers the workflow automatically.

### 2. Workflow Orchestration
- **n8n** handles automation and orchestration.
- It monitors Airtable for new requests and triggers operations, from scraping to storage.
- Supports parallel requests and efficient resource usage.

### 3. Data Scraping
- **Apify actors** are used for each platform:
  - **Facebook & Instagram**: Scrape organic posts, comments, and ads (including engagement, profiles, and ad metadata).
  - **TikTok**: Scrape posts, comments, and ads (including video content, impressions, business names, and dates).

### 4. AI-Powered Analysis
AI models enrich the raw data:
- **Content Analysis**: Identifies key insights, visual hooks, and supporting proof (e.g., testimonials, charts).
- **Comments Analysis**: Summarizes themes, common questions, and sentiment.
- **Virality Scoring**: Assigns numerical scores to help prioritize high-potential content.

### 5. Structured Storage
- All enriched data is stored in **Airtable**, turning it into a “single source of truth”.
- Airtable’s filtering, sorting, and reporting make results easy to explore, share, and use in campaign planning.

---

## Business Benefits for Marketing Agencies

### 1. Unmatched Competitive Intelligence
- Scrapes live ads from Meta & TikTok Ad Libraries.
- Reveals what creative, messaging, and CTAs are working for competitors.
- Cuts R&D from weeks to hours.

### 2. Deep Audience & Market Insights
- Public comments reveal consumer sentiment, frustrations, and desires.
- Helps refine brand voice and messaging.

### 3. Accelerated Content & R&D
- AI surfaces high-virality content automatically.
- Provides creative briefs highlighting why content works.

### 4. Scalable & Automated Efficiency
- Eliminates manual data collection.
- Allows teams to focus on strategy and creative execution.

### 5. Evidence-Based Decision Making
- Provides **Virality Scores, Comment Summaries, and Content Analyses**.
- Enables decisions backed by clear, quantifiable evidence.

---

## Technical Stack
- **Workflow Automation**: n8n  
- **Web Scraping**: Apify Actors  
- **Database & UI**: Airtable  
- **AI Models**: Generative LLMs  

---

## Getting Started

1. **Airtable Setup**  
   - Create a new Airtable base.  
   - Import the provided schema for each scraper.  

2. **Apify Configuration**  
   - Set up your Apify account.  
   - Obtain API tokens for the actors.  

3. **n8n Deployment**  
   - Deploy workflows on a self-hosted or cloud instance.  
   - Connect to Airtable and Apify.  

4. **API Key Integration**  
   - Configure all API keys and webhooks in the workflows.  

5. **Run**  
   - Submit a search request in Airtable to trigger the first scrape.  

📖 For detailed setup instructions, see the **individual manuals** included in the repository.  
