# Reddit Market Research Agent (n8n Workflow)

## Overview
This repository contains the workflow logic for a market research tool built on **n8n**. The purpose of this tool is to analyze trending topics in technology and gaming communities to help create relevant educational content for YouTube.

**Note:** This application is **Read-Only**. It does not post, comment, or vote on Reddit.

## Architecture
The application uses n8n to orchestrate the following steps:

1. **Trigger:** The workflow runs on a scheduled timer (e.g., once daily).
2. **Data Ingestion (Reddit API):** - Uses the Reddit API to fetch `top` posts from specific subreddits (e.g., r/ArtificialInteligence, r/gaming).
   - Filters for posts with high engagement (comments/upvotes).
3. **Analysis (Google Gemini):**
   - The text content of these posts is sent to Google Gemini (AI).
   - The AI summarizes the discussions and identifies common questions or pain points.
4. **Output (Google Sheets):**
   - The summarized insights and topic ideas are saved to a Google Sheet for content planning.

## Tech Stack
- **n8n:** Workflow automation and API orchestration.
- **Reddit API:** Data source for community trends.
- **Google Gemini API:** Natural Language Processing (NLP) for sentiment analysis.
- **Google Sheets:** Data storage for the content team.

## Usage
This workflow is hosted on a private self-hosted n8n instance and is restricted to authorized developers only.
