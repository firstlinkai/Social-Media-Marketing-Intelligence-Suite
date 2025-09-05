# Social Media Marketing Intelligence Suite

## Project Overview
This repository contains a powerful, automated suite of tools designed to provide marketing agencies with deep, data-driven insights from social media platforms. The system automates the tedious and time-consuming process of scraping public posts and ads from Facebook, Instagram, and TikTok. It then uses advanced AI to analyze the collected content and comments, transforming raw data into actionable market intelligence.

This suite is a strategic asset for competitive analysis, audience research, content strategy, and R&D, enabling agencies to build more effective and resonant marketing campaigns. Instead of relying on manual data collection and subjective analysis, this system provides a scalable, repeatable, and objective method for staying ahead of trends and understanding consumer behavior. It acts as the backbone for any modern digital marketing operation seeking to leverage real-time public data to inform and optimize campaigns.

## How It Works: The Core Workflow
The system is built on a modular and scalable architecture that orchestrates a seamless data flow from social media platforms to a structured database with AI enrichment. This process is designed to be both powerful and easy to use, abstracting away the technical complexity for the end user.

### Input Queue
The process begins when a marketing analyst submits a search request directly within the intuitive Airtable user interface. The user simply defines the parameters of their research—for example, a specific keyword, a competitor's handle, a hashtag, or a geographic region. This request is instantly added to a queue, triggering the automation without any manual intervention from the technical team.

### Workflow Orchestration
An n8n workflow acts as the central automation engine. n8n's visual, node-based interface allows for the rapid creation and modification of complex data pipelines. It constantly monitors the Airtable base for new search requests. When a request is detected, n8n triggers a sequence of operations, managing the entire lifecycle of the data from scraping to final storage. This on-demand system ensures efficient use of resources and provides a robust framework for handling multiple parallel requests.

### Data Scraping
n8n invokes specialized Apify actors tailored for each social media platform. These actors are robust, headless browsers that mimic user behavior to navigate social media sites and collect data. This approach is highly effective at bypassing anti-scraping measures. The actors perform the heavy lifting of scraping:

- **Facebook & Instagram**: Scrape organic posts and comments, as well as ads from the Meta Ad Library. Data includes rich post content (text, image/video URLs), engagement metrics (likes, shares, comments), author profiles (name, follower count), and critical ad metadata (e.g., region, impressions, ad text, creative variants).
- **TikTok**: Scrape organic posts and comments, and ads from the TikTok Ad Library. Data includes video content, business names, estimated impressions, and publish dates for ads, providing a complete picture of a brand's paid strategy.

### AI-Powered Analysis
Once the raw data is collected, it is sent to Large Language Models (LLMs) for deep analysis and enrichment. This is the "intelligence" layer of the system that transforms raw data into actionable insight. The AI modules are specifically designed to:

- **Content Analysis**: The LLM analyzes the post's visuals and text to identify Key Insights, such as the core value proposition or a summary of the post's purpose. It also determines the Visual Hook, or what makes the content a "scroll stopper" (e.g., a rapid-fire scene change, a vibrant color palette). Finally, it pinpoints Undeniable Proof, which are the credible elements that support claims within the content (e.g., customer testimonials, data charts, expert quotes).
- **Comments Analysis**: The AI modules process the comment sections to summarize key themes, common questions, and overall sentiment. This provides a direct window into how the audience is reacting to the content, which is invaluable for identifying a brand's strengths and weaknesses from the consumer perspective.
- **Virality Scoring**: The AI assigns a numerical score to posts based on a set of criteria to help prioritize content with the highest potential for replication or further study. This score is a powerful shortcut for analysts, allowing them to focus their attention on the most promising content without having to manually review thousands of records.

### Structured Storage
The final, enriched data—including all scraped content, metadata, and AI insights—is seamlessly stored back into a well-structured Airtable database. This turns Airtable from a simple queue into a "single source of truth" for the marketing team. Its powerful filtering, sorting, and reporting capabilities provide a user-friendly and searchable interface for analysts to review findings, generate reports, and share with internal and external stakeholders. The structured format ensures that the data is not only accessible but also easily understandable and ready for immediate use in campaign planning.

## Business Benefits for a Marketing Agency
This system is not just a collection of scripts; it is a strategic tool that provides a significant competitive advantage.

### 1. Unmatched Competitive Intelligence
By scraping competitor ads from the Meta and TikTok Ad Libraries, agencies can gain a clear, real-time understanding of what ad creative, messaging, and calls-to-action are working for others in the market. This insight is not based on guesswork; it is derived from live campaigns and their performance signals. For example, an agency can identify that a competitor is successfully using user-generated content (UGC) with a specific type of background music. This insight allows for the rapid development of effective, data-backed ad campaigns, giving the agency and its clients a decisive edge. It shortens the R&D cycle from weeks to hours and ensures every ad dollar is spent more effectively.

### 2. Deep Audience & Market Insights
Analyzing public posts and comments provides a direct line to consumer sentiment and perception. Agencies can go beyond basic demographics to identify trending topics, understand consumer pain points, and discover the exact language their target audience uses. This information is invaluable for refining a brand's voice and creating content that truly resonates. For instance, if a brand is considering a new product feature, analyzing public comments on similar products can reveal common user frustrations and desires, allowing the agency to craft a marketing message that directly addresses those needs.

### 3. Accelerated Content & R&D
The AI-driven analysis accelerates the R&D process, making it proactive rather than reactive. Instead of manually sifting through thousands of posts, the system automatically surfaces content with high virality scores and identifies the key elements that make it successful (Visual Hooks, Undeniable Proof). This enables agencies to quickly identify creative trends and build a powerful content pipeline. The AI-generated insights act as a creative brief, helping copywriters and designers understand precisely why a piece of content is successful, allowing them to replicate its key elements for new campaigns.

### 4. Scalable & Automated Efficiency
This automation suite eliminates the need for manual, time-intensive data collection. Marketing teams can focus on what they do best—strategy and creative execution—while the system handles the continuous, real-time collection and analysis of vast amounts of social media data. This dramatically reduces the cost and time associated with market research, freeing up human resources for more high-value tasks. The on-demand nature of the system means resources are only used when needed, making it an incredibly efficient solution.

### 5. Evidence-Based Decision Making
The output of the system is not just raw data, but a curated set of insights. By providing a Virality Score, a Comments Summary, and a detailed Content Analysis, the tools empower marketing teams to make decisions based on clear, quantifiable evidence rather than guesswork. This provides confidence and justification for strategic choices, making it easier to sell ideas to clients and stakeholders. The documented data trail allows for easy post-campaign analysis and optimization, creating a continuous loop of learning and improvement.

## Technical Stack
The system is built on a robust and flexible stack of tools chosen for their powerful automation capabilities and ease of integration.

- **Workflow Automation**: n8n  
- **Web Scraping**: Apify Actors  
- **Database & User Interface**: Airtable  
- **AI Models**: Various Generative AI models (LLMs)  

## Getting Started
To set up and run this system:

1. **Airtable Setup**: Create a new Airtable base and import the provided schema for each scraper.  
2. **Apify Configuration**: Configure your Apify account and obtain the necessary API tokens for the actors.  
3. **n8n Deployment**: Deploy the n8n workflows on your self-hosted or cloud-based instance and connect them to your Airtable and Apify accounts.  
4. **API Key Integration**: Ensure all API keys and webhooks are correctly configured within the n8n workflows.  
5. **Run**: Submit a search request in your Airtable base to trigger the first scrape.  

Please refer to the individual manuals for a detailed, step-by-step walkthrough of each system's setup and usage.
