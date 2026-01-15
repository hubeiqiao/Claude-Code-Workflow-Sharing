# My Claude Code Workflow: How a Product Person Ships Real Products

A showcase site demonstrating how to effectively use Claude Code + Opus 4.5 to ship real products as a non-engineer.

**Live Site:** [Coming soon on Cloudflare Pages]

## About

This project shares my personal workflow for using Claude Code to build production-ready software. As a product person (not a traditional developer), I've developed strategies and principles that help me ship real products with AI assistance.

### Key Topics Covered

- **Vibe Engineering** - Writing clear requirements before touching code
- **Context Window Management** - Maintaining quality output throughout long sessions
- **Plan Mode** - Breaking complex tasks into manageable steps
- **The 80/20 Rule** - When AI accelerates vs. when it struggles
- **Debugging Strategies** - Systematic approaches when things go wrong
- **Testing & Deployment** - Shipping with confidence

## Tech Stack

- **HTML/CSS/JS** - Single-page static site (no build process)
- **Tailwind CSS** - Utility-first styling via CDN
- **Google Fonts** - Space Grotesk, DM Sans, JetBrains Mono, Syne

## Performance Optimizations

- WebP images with PNG fallbacks (84% size reduction on largest images)
- Font preloading for critical fonts
- Throttled scroll events with `requestAnimationFrame`
- Lazy loading for below-fold images
- Proper image dimensions to prevent layout shift

## Local Development

Simply open `index.html` in your browser - no build step required.

```bash
# Clone the repo
git clone https://github.com/hubeiqiao/Claude-Code-Workflow-Sharing.git

# Open in browser
open index.html
```

## Deployment

This site is designed to be hosted on any static hosting platform:

- **Cloudflare Pages** - Connect repo, no build command needed
- **GitHub Pages** - Enable in repo settings
- **Netlify/Vercel** - Drag and drop or connect repo

## Author

**Joe Hu** - Product Person & Vibe Engineer

- Website: [hubeiqiao.com](https://hubeiqiao.com)
- Twitter: [@hubeiqiao](https://x.com/hubeiqiao)
- Claude Code Log: [@ClaudeCodeLog](https://x.com/ClaudeCodeLog)

## License

MIT License - Feel free to use this as inspiration for your own projects.

---

Built with Claude Code + Opus 4.5
