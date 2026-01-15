# My Claude Code Workflow: How a Product Person Ships Real Products

**Live Site:** [cc.hubeiqiao.com](https://cc.hubeiqiao.com)

**Original Blog Post:** [hubeiqiao.com/blog/2e80df12-ec77-803f-9814-c71bff16feee](https://hubeiqiao.com/blog/2e80df12-ec77-803f-9814-c71bff16feee)

---

I'm a product person, not an engineer. Yet I ship real, production-ready products using Claude Code + Opus 4.5. This site shares the workflow and principles I've developed.

**The bottleneck is not AI's capability. It's your ability to articulate what you want.**

## TL;DR

1. Write what you want first without AI
2. Use Plan Mode with subagents to break it down
3. Review before auto-accepting suggestions
4. Keep context clean and well-documented
5. Test, commit, deploy incrementally

## Key Principles

### 1. Your Demands First
Articulate what you want. Most issues arise because you don't know what you want or haven't clarified your requirements. Since I don't know the code, this is the core part to validate if AI understands my demands by reading documents.

### 2. Context Window
Think of it like a desk - as it fills with papers, the quality of work decreases. Claude Code can complete 100+ page project reports in a few hours with enough context.

### 3. Memory Management
Claude doesn't truly "remember" - it reads context each time. Keep important information in documents that persist across sessions.

### 4. Assignment, Report
Claude Code can complete large project reports in a few hours with enough context. The key is giving clear assignments and expecting structured reports back.

## My Workflow

### Before Running Claude Code
- Use the native build (install with homebrew)
- Much nicer syntax highlighting
- Can also run Claude Code on Claude Desktop directly

### The Decision Tree

```
New Task?
    ├── Coding Project → Use Plan Mode → Research first
    │                                  → Create plan document
    │                                  → Verify with user
    │                                  → Execute step by step
    │
    └── Visualization → Direct execution usually works
```

### Draft → Plan → Execute → Test → Deploy

1. **Draft in Plain Language** - Write requirements without AI first
2. **Plan Mode** - Let Claude research and create a structured plan
3. **Review the Plan** - Verify it matches your intent before executing
4. **Execute Incrementally** - One step at a time, commit frequently
5. **Test & Deploy** - Run tests, check the build, deploy to staging

## Tips

| Tip | Why It Matters |
|-----|----------------|
| Use Plan Mode | Prevents Claude from diving into code without understanding the full picture |
| Commit Often | Small, frequent commits make it easier to rollback if something breaks |
| Keep Context Clean | Remove irrelevant conversation history to maintain output quality |
| Document Everything | Claude reads your docs each session - make them comprehensive |
| Test Before Deploy | Always run the test suite and build before pushing to production |
| Ask Questions | Use the ask-questions skill to clarify requirements upfront |

## When AI Struggles

- **The last 20%** - Edge cases, polish, and integration often need more guidance
- **Complex debugging** - Sometimes you need to investigate systematically
- **Context overload** - Quality drops when the context window fills up

## Debug Strategies

1. **Reference History** - Check if similar issues occurred before
2. **Systematic Investigation** - Use `/investigate` to get structured reports
3. **Fresh Context** - Start a new session if context is polluted
4. **Search Online** - Sometimes the answer is in documentation or forums

## Author

**Joe Hu** - Product Person & Vibe Engineer

- [hubeiqiao.com](https://hubeiqiao.com)
- [@hubeiqiao](https://x.com/hubeiqiao)
- [@ClaudeCodeLog](https://x.com/ClaudeCodeLog)

---

Built with Claude Code + Opus 4.5
