# Claude Skills for Vercel

A collection of [Claude Code](https://claude.com/claude-code) skills for working with Vercel deployments.

## Available Skills

### vercel-deploy

Deploy applications and websites to Vercel instantly. No authentication required.

**Use when:**
- "Deploy my app"
- "Deploy this to production"
- "Push this live"
- "Deploy and give me the link"

**Features:**
- No authentication required - works instantly
- Auto-detects 40+ frameworks from `package.json`
- Returns preview URL (live site) and claim URL (transfer ownership)
- Handles static HTML projects automatically
- Excludes `node_modules` and `.git` from uploads

**How it works:**
1. Packages your project into a tarball
2. Detects framework (Next.js, Vite, Astro, etc.)
3. Uploads to deployment service
4. Returns preview URL and claim URL

**Output:**
```
✓ Deployment successful!

Preview URL: https://skill-deploy-abc123.vercel.app
Claim URL:   https://vercel.com/claim-deployment?code=...
```

## Installation

Copy the desired skill folder to your Claude Code skills directory:

```bash
cp -r skills/vercel-deploy ~/.claude/skills/
```

That's it. No CLI installation or authentication needed.

## Usage

Skills are automatically available to Claude Code once installed. Simply ask Claude to deploy:

```
Deploy my app
```

```
Deploy this and give me the link
```

Claude will package your project, deploy it, and return both URLs.

## Skill Structure

Each skill contains:
- `SKILL.md` - Instructions for Claude Code
- `scripts/` - Helper scripts for automation

## License

MIT
