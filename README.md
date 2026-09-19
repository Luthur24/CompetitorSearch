CompetitorSearch

CompetitorSearch is an AI-powered competitive intelligence application that researches competitor landscapes, structures the findings, and turns web research into organized competitive insights.

Overview

CompetitorSearch is designed to reduce the manual work involved in researching a competitive landscape.

Instead of requiring users to manually construct multiple search queries and organize findings themselves, the application accepts a natural-language competitive research request and uses an AI-assisted research pipeline to refine the intent, search the web, identify relevant companies, structure the results, and enrich incomplete information.

The project demonstrates an approach to combining large language models with web search and structured data processing inside a browser-based application.

How It Works

The research pipeline follows several stages.

Natural-language request
          │
          ▼
   Intent refinement
          │
          ▼
    Web research
          │
          ▼
 Competitor extraction
          │
          ▼
 Structured results
          │
          ▼
   Gap identification
          │
          ▼
   Targeted enrichment
          │
          ▼
 Refined competitive landscape

Core Features

- Natural-language competitor research
- AI-assisted search intent refinement
- Web-based competitor discovery
- Structured competitor extraction
- Competitor positioning analysis
- Company tagging
- Domain identification
- Founded-date enrichment
- Competitive signals
- Confidence information
- Search result enrichment
- Result refinement using additional user instructions
- Retry handling for rate-limited requests
- Structured JSON model responses
- Bounded autonomous research passes

AI Research Pipeline

1. Intent Refinement

A user's natural-language request is converted into a more precise search query.

For example:

"Find competitors to X for small businesses"

can be transformed into a more targeted web-search intent before research begins.

2. Web Search

The refined query is submitted to the web-search layer to collect relevant external information.

3. Structured Competitor Extraction

The collected research is passed through an AI processing stage that identifies real companies and organizes relevant fields such as:

- Company name
- Domain
- Tagline
- Positioning
- Competitive signals
- Tags
- Confidence
- Founded information

4. Refinement

Users can provide additional instructions to filter or reorder the existing competitor set without requiring the system to invent new companies or unsupported facts.

5. Autonomous Enrichment

The application evaluates the structured results for incomplete or weak fields.

It can identify gaps such as:

- Missing company information
- Weak positioning data
- Missing competitive signals
- Uncertain domains
- Missing founding information

It then generates targeted searches to improve the existing dataset.

The enrichment process is intentionally bounded to prevent uncontrolled API usage.

Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Mistral API
- Tavily Search API
- JSON-based AI responses
- Browser Fetch API

Application Architecture

┌───────────────────────────────┐
│          Web Interface        │
│       HTML / CSS / JS         │
└───────────────┬───────────────┘
                │
                ▼
       Intent Processing
                │
                ▼
        Mistral API
                │
                ▼
       Refined Search Query
                │
                ▼
        Tavily Web Search
                │
                ▼
       Search Context Data
                │
                ▼
        Mistral Processing
                │
                ▼
      Structured Companies
                │
                ▼
       Gap Identification
                │
                ▼
        Targeted Research
                │
                ▼
        Enriched Results

Reliability

The application includes retry handling for transient failures and rate limiting.

Requests can be retried with increasing delays, while non-retriable failures are surfaced to the interface.

This provides a more resilient experience when working with external AI and search APIs.

Project Structure

CompetitorSearch/
├── index.html
└── README.md

The current implementation intentionally keeps the application lightweight by combining the interface and client-side application logic in a single HTML file.

Running Locally

Clone the repository and open the application in a modern browser.

git clone <repository-url>
cd CompetitorSearch

Because the application communicates with external APIs from the browser, API configuration and provider security should be handled carefully before production deployment.

Security

Important: API credentials should never be committed directly into a public frontend repository.

For production use, API requests should be routed through a secure backend or server-side proxy where provider credentials can be stored as environment variables.

Any credentials previously exposed in the repository should be revoked and replaced before deployment.

Project Status

Frontend MVP / Experimental AI Application

CompetitorSearch demonstrates an AI-assisted competitive-intelligence workflow combining language-model reasoning, web search, structured extraction, iterative enrichment, and an interactive browser interface.

What This Project Demonstrates

- AI API integration
- Web-search integration
- Prompt engineering
- Structured JSON generation
- Multi-stage AI pipelines
- Iterative data enrichment
- Error and rate-limit handling
- Client-side application architecture
- Product-oriented interface development