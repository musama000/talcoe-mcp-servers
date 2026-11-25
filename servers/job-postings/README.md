# Job Postings MCP server

Ask: "Find remote senior platform engineer roles on Ashby paying at least $160k."

One of the rows that comes back:

```json
{
  "title": "Senior Software Engineer - Lead Platform",
  "company": "a-place-for-mom",
  "location": "Remote-US",
  "workplaceType": "Remote",
  "salaryMin": 160000,
  "salaryMax": 190000,
  "salaryCurrency": "USD",
  "jobUrl": "https://jobs.ashbyhq.com/a-place-for-mom/ee4c0ce4-ceb6-4d38-a1d5-0dda8a737d2a"
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/greenhouse-jobs,talcoe/lever-jobs,talcoe/ashby-jobs,talcoe/workday-jobs,talcoe/smartrecruiters-jobs,talcoe/usajobs,talcoe/remote-jobs-aggregator
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--greenhouse-jobs` | Open roles across 600 companies on Greenhouse, or your own company list, by keyword, location, department and posting date | $0.005 per job |
| `talcoe--lever-jobs` | Open roles across companies on Lever by keyword, location, team, workplace type and commitment | $0.005 per job |
| `talcoe--ashby-jobs` | Open roles across about 2,000 companies on Ashby, with pay range, by keyword, location, department, remote and minimum salary | $0.005 per job |
| `talcoe--workday-jobs` | Open roles on Workday careers sites by keyword, location and posting date, with full descriptions | $0.005 per job |
| `talcoe--smartrecruiters-jobs` | Open roles on SmartRecruiters by keyword, country, workplace type and posting date | $0.005 per job |
| `talcoe--usajobs` | Federal jobs on USAJOBS by keyword, occupation series, GS grade, agency and location, with salary and dates | $0.005 per job |
| `talcoe--remote-jobs-aggregator` | Remote jobs from RemoteOK and We Work Remotely with tags, salary and apply links | $0.005 per job |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "Find remote senior platform engineer roles on Ashby paying at least $160k."
- "Which Greenhouse companies posted product designer jobs in New York this week?"
- "List GS-13 cybersecurity jobs on USAJOBS that close this month."

## Source actors

- [Greenhouse Jobs Scraper](https://apify.com/talcoe/greenhouse-jobs)
- [Lever Jobs Scraper](https://apify.com/talcoe/lever-jobs)
- [Ashby Jobs Scraper](https://apify.com/talcoe/ashby-jobs)
- [Workday Jobs Scraper](https://apify.com/talcoe/workday-jobs)
- [SmartRecruiters Jobs Scraper](https://apify.com/talcoe/smartrecruiters-jobs)
- [USAJOBS Federal Jobs Scraper](https://apify.com/talcoe/usajobs)
- [Remote Jobs Aggregator](https://apify.com/talcoe/remote-jobs-aggregator)
