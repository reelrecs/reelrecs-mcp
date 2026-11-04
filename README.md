# ReelRecs

Find your next movie or show with current trends, audience viewing and rating patterns, rich title context, and streaming options.

Start with a short question:

- What should I watch tonight?
- What's popular on streaming?
- Help me figure out what I'm in the mood for.

ReelRecs helps your assistant build a useful shortlist, then refine it as you react. Try “lighter,” “a movie instead,” “on Netflix,” or “I've seen those.”

## Connect

**Remote MCP URL:** `https://mcp.reelrecs.com/mcp`

The service uses Streamable HTTP. Public discovery works without a ReelRecs account or API key. If your client supports remote MCP servers, add the URL in its connector settings. Cursor can also load this plugin package.

```json
{
  "mcpServers": {
    "reelrecs": {
      "url": "https://mcp.reelrecs.com/mcp"
    }
  }
}
```

[Get started](https://reelrecs.com/assistants/) · [Claude directory](https://claude.ai/directory/reelrecs)

## What your assistant can do

| Capability | Tools |
| --- | --- |
| Resolve a movie or show, including versions and misspellings | `search_titles` |
| Discover similar titles using what you liked, disliked, or want to feel | `recommend_titles` |
| Compare a title with relevant content peers | `get_title_peers` |
| Explore current popular titles by genre, format, or streaming service | `get_charts` |
| Check where a title is available, with offer types and dates | `get_watch_options` |
| Use your connected account's taste and saved streaming services | `get_my_profile`, `recommend_for_me` |
| Browse, search, and look up your saved ratings | `get_my_ratings` |
| Browse your bookmarks and choose from your saved list | `get_my_bookmarks` |
| Find something to watch together using accepted Watch+ group members' tastes | `get_my_watchplus_groups`, `get_watchplus_context`, `recommend_for_group` |
| Record a brief reaction or concrete problem, subject to the viewer's and host's permissions | `report_recommendation_feedback` |

Candidates carry descriptions, genres, subgenres, useful tags, ReelRecs links and scores when available. **ReelRecs Score** is an overall audience rating. A connected viewer's **Rec Score** is a personal prediction. Streaming offers include their country and observation date; subscription access, free offers, rentals and purchases are distinct.

## Your account and data

Connecting a ReelRecs account is optional. Clients that support ReelRecs' OAuth flow can request read-only access to saved taste, ratings, bookmarks and accepted Watch+ groups. Permission depends on the tool and the scopes you approve. Pending group invitees' tastes are not shared.

Account tools cannot change ratings, bookmarks or groups. The feedback tool writes a short quality report and does not alter saved taste. The service records tool requests, responses and errors for reliability and quality review as described in the [privacy policy](https://reelrecs.com/legal/privacy/). It does not receive the host's full conversation unless the host sends content in a tool call.

Tool definitions come from the live service. Some hosts cache them or require a listing update or reconnect before new tools appear. This repository contains public connection metadata and listing assets. The hosted service, models, customer data and credentials are not distributed here.

## Support

[Contact ReelRecs](https://reelrecs.com/contact/) · [Privacy](https://reelrecs.com/legal/privacy/) · [Terms](https://reelrecs.com/legal/terms/)

The configuration and documentation in this repository are MIT licensed. See [assets/NOTICE](assets/NOTICE) for the logo's permitted use. ReelRecs names and logos remain REELRECS INC trademarks. Use of the hosted service is governed by the ReelRecs terms.
