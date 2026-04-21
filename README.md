# ReachOut — LinkedIn Outreach Agent

An AI-powered tool that generates personalized LinkedIn connection messages. Fill in a prospect's details, pick a tone, and get three ready-to-send messages in seconds.

## What it does

Most cold LinkedIn messages get ignored because they're generic. ReachOut uses Claude to write messages that reference something real about the prospect — a recent post, a funding round, a pain point — and keeps them under LinkedIn's 300-character connection request limit.

Each generation gives you three angles to choose from:

- **Empathy** — acknowledges their situation
- **Curiosity** — leads with a question they want to answer
- **Value-led** — opens with what you bring to the table

## Getting started

This is a single HTML file. No build step, no dependencies, no server.

1. Download `outreach-agent.html`
2. Open it in any browser
3. Grab a free API key at [console.anthropic.com](https://console.anthropic.com)
4. Fill in the prospect details and generate

That's it.

## Deploying online

If you want a shareable URL:

**Netlify** — drag and drop the HTML file at [app.netlify.com/drop](https://app.netlify.com/drop). Done in 30 seconds.

**Vercel** — put the file in a folder, run `vercel` from that directory, or connect the repo and it deploys on push.

**GitHub Pages** — rename the file to `index.html`, push to a repo, enable Pages under Settings > Pages.

## Stack

- Vanilla HTML, CSS, JavaScript
- [Claude Sonnet](https://anthropic.com) via the Anthropic Messages API
- No frameworks, no build tools, no tracking

## API key

Your key is entered in the browser and goes directly to Anthropic. It is never logged, stored, or sent anywhere else. If you're deploying this for a team and don't want everyone using their own key, the cleanest approach is to put a small proxy in front of it — a single Vercel edge function works fine.

## Customizing the prompt

The prompt lives at the bottom of the HTML file inside the `run()` function. It's straightforward to edit — change the angles, adjust the character limit, add industry-specific instructions, or swap in a different model.

```js
const prompt = `You are a LinkedIn outreach copywriter...`
```

## Project structure

```
outreach-agent.html   the whole app
README.md             this file
```

## License

MIT
