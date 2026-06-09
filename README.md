# rmanzoku.net

Official site for Ryo Manzoku.

This is a dependency-free static site. It is designed to be publishable from GitHub Pages, Cloudflare Pages, Vercel, or any static host.

## Repository Boundary

Keep this repository limited to static, publishable site files.

- Do not add build scripts, operational scripts, runner wrappers, agent skills, package managers, or generated workflow tooling here.
- Put operational scripts, skills, research workflows, and automation helpers in `/Users/rmanzoku/ghq/github.com/rmanzoku/workspace`.
- If content needs to be generated, generate it outside this repository and commit only the final static files needed for publication.

## Structure

- `index.html` - top page
- `about/` - canonical profile
- `topics/ai-harness/` - AI harness and answer-space framing
- `topics/ai-bpo/` - AI-BPO / FDE framing
- `topics/ai-agents/` - AI agent operations
- `articles/` - writing index
- `speaking/` - speaking and public materials
- `llms.txt` - canonical AI-readable site guide
- `robots.txt` / `sitemap.xml` - crawler entrypoints

## Local Preview

Open `index.html` directly in a browser, or run a static server:

```sh
python3 -m http.server 8080
```
