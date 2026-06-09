
# AI Job Search Agent

An autonomous AI-powered career intelligence system built using n8n, Claude, Google Workspace, and Telegram.

## Problem

Searching hundreds of PM jobs daily is time-consuming and produces many low-quality opportunities.

## Solution

This workflow automatically:

- Discovers new PM jobs from RSS feeds
- Matches jobs against my resume
- Researches company fundamentals
- Calculates weighted opportunity scores
- Prioritizes jobs into P1/P2/P3 buckets
- Stores opportunities in Google Sheets
- Sends Telegram alerts for high-priority jobs

## Architecture
<img width="1440" height="1640" alt="image" src="https://github.com/user-attachments/assets/a27a77ee-398a-4393-a4b7-ad9e65ec919d" />

<img width="1192" height="715" alt="image" src="https://github.com/user-attachments/assets/3d0f45d1-cc06-4765-97a1-e02c33eab1c4" />



## Tech Stack

- n8n
- Claude Sonnet
- Google Sheets API
- Google Docs API
- Telegram Bot API
- RSS Feeds
- JavaScript

## Sample Output


### Telegram Alert
<img width="713" height="820" alt="image" src="https://github.com/user-attachments/assets/c2389c9a-9926-4309-82c7-d3d1859686da" />




### Google Sheet

<img width="1133" height="202" alt="image" src="https://github.com/user-attachments/assets/9f702d36-fd40-4944-9ca7-181af849139d" />

## Product Decisions

### Why Resume Matching First?

Resume matching acts as the first screening layer and eliminates low-fit opportunities before spending additional LLM tokens on company research.

### Why Company Research?

A role may appear attractive based on title alone, but company stage, funding, growth prospects, and product maturity significantly impact long-term career outcomes.

### Why Weighted Scoring?

Job fit is not determined solely by skill match. Career alignment, market opportunity, and compensation potential are also important decision factors.

### Why Telegram Alerts?

High-priority opportunities require immediate visibility and action without manually reviewing spreadsheets.

## Scoring Framework

Final Score =

50% Resume Match Score

* 30% Career Alignment Score
* 15% Market Opportunity Score
* 5% Salary Score

Priority Classification:

P1: 85+
High-priority opportunities that should be reviewed immediately.

P2: 75-84
Strong opportunities worth considering.

P3: Below 75
Lower-priority opportunities stored for future reference.


## Results

- Processes 100+ jobs automatically
- Reduces manual screening effort by 90%
- Surfaces only high-fit opportunities

## Future Roadmap

- LinkedIn integration
- Resume tailoring agent
- Cover letter generation
- Interview preparation agent

