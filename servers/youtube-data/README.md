# YouTube Data MCP server

Ask: "Pull the transcript of https://www.youtube.com/watch?v=jNQXAC9IVRw and summarize it."

The row that comes back, with the transcript cut short here:

```json
{
  "title": "Me at the zoo",
  "channel": "jawed",
  "publishDate": "2005-04-23",
  "durationSeconds": 19,
  "views": 449293287,
  "language": "en",
  "transcript": "All right, so here we are, in front of the elephants the cool thing about these guys is that they have really... really really long trunks and that's cool",
  "url": "https://www.youtube.com/watch?v=jNQXAC9IVRw"
}
```

## URL

```
https://mcp.apify.com/?tools=talcoe/youtube-transcripts,talcoe/youtube-comments,talcoe/youtube-channel-videos
```

Send your Apify API token as `Authorization: Bearer <token>`. Setup for Claude Code, Cursor and VS Code is in the [main README](../../README.md#connect).

## Tools

| Tool | Returns | Price |
|---|---|---|
| `talcoe--youtube-transcripts` | The full transcript as text and timestamped segments, with title, channel, publish date, duration and views, by caption language with optional translation | $0.005 per video |
| `talcoe--youtube-comments` | One record per comment with text, likes, reply count and pinned or hearted flags, sorted top or newest, with optional replies | $0.003 per comment |
| `talcoe--youtube-channel-videos` | Every public video on a channel with title, views, upload age, duration and thumbnail, filtered by sort order and minimum views | $0.003 per video |

Apify's MCP server adds four helper tools that read run status and results. Each run also carries a small start charge.

## Prompts to try

- "Pull the transcript of this video and give me the timestamps for each topic."
- "What do the top 100 comments on this video say about battery life?"
- "List every video on this channel with more than 100,000 views, newest first."

## Source actors

- [YouTube Transcript Scraper with Timestamps and Languages](https://apify.com/talcoe/youtube-transcripts)
- [YouTube Comments Scraper: Comments, Replies and Likes](https://apify.com/talcoe/youtube-comments)
- [YouTube Channel Scraper: All Videos, Views and Duration](https://apify.com/talcoe/youtube-channel-videos)
