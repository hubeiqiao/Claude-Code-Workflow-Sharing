# My Claude Code Workflow: How a Product Person Ships Real Products with Claude Code

<aside>
💡

**TL;DR:** Write what you want first without AI. Use Plan Mode with `ultrathink` to break it down. Keep context window under control by compacting and using subagents. Test manually. When debugging, act like a PM and provide evidence. The bottleneck is not AI's capability, it's your ability to articulate what you want.

</aside>

![Vibe Engineering](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/01-vibe-engineering-hero.png)

- Table of Contents

# Introduction

## What is Claude Code?

[Claude Code](https://code.claude.com/docs/en/overview) is a "general agent" disguised as a developer tool. It can help with almost any computer task you can complete by running code or terminal commands, as long as you know how to use it. You can build almost anything you want in the digital world.

![CleanShot 2026-01-14 at 14.53.01.png](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/CleanShot_2026-01-14_at_14.53.01.png)

Claude Code is my favourite product of 2025 and I'm now subscribing to the [Claude Max plan](https://claude.com/pricing) ($200 per month). These coding agents enabled me to do things I couldn't imagine a year ago.

Last summer, Claude Code was not as powerful as it is now. But with **Opus 4.5**, I can feel the difference (while it still has multiple areas to improve), I feel I am able to do anything I want as long as I can articulate my thoughts with a longer plan. Now, I am building a real product with backend, cloud, payment, credit and promo code system rather than only frontend prototypes. Claude Code with Opus 4.5 is the most powerful tool I've ever accessed.

**This is the golden era to build for yourself.**

*P.S. Claude Code reminds me of grinding in World of Warcraft during college... except now I'm shipping real products instead of raiding dungeons.*

## My Background

[I am a product person without a strong technical background.](http://hubeiqiao.com) Fortunately, I'm already familiar with the software development process, which means I am better positioned than most people for vibe coding.

![CleanShot 2026-01-14 at 14.53.47.png](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/CleanShot_2026-01-14_at_14.53.47.png)

Incredibly, I am building my first real commercialized product ([joespeaking.com](https://joespeaking.com/)) by using Claude Code with Opus 4.5 and plan to start alpha testing by the end of this month.

**I am a living example of how AI empowers skills.**

## Why Do We Have This Session/Page

This month, I am at Ottawa's first [AGI Ventures Canada](https://www.agiventures.ca/) Hacker House alongside some high-agency people. I'm also excited (and grateful) to have been accepted into the first cohort.

![CleanShot 2026-01-14 at 14.54.45.png](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/CleanShot_2026-01-14_at_14.54.45.png)

At the house, we not only build together but also will have several workshops and sharing sessions. Since I absolutely love Claude Code, I came up with an idea to just share my workflow and trigger discussion to learn from each other. For Claude Code, everyone has different usage and workflows. **The core of this session is to explore a better workflow for you and me.**

This is just how I use Claude Code currently (Tuesday, January 14, 2026). It updates rapidly. It's been incredible to witness the rapid development of Claude Code every single day at [Claude Code Changelog (@ClaudeCodeLog)](https://x.com/ClaudeCodeLog)! And the new [Claude Cowork](https://techcrunch.com/2026/01/12/anthropics-new-cowork-tool-offers-claude-code-without-the-code/) was [written 100% by Claude Code itself](https://x.com/bcherny/status/2010809450844831752) (with human guidance).

# What I Do with Claude Code

- **Build**: My product ([joespeaking.com](https://joespeaking.com/))
- **Display**: Website/Slide deck (This material is an example, I focus on the content first and then let Claude Cowork polish the content and Claude Code build the website for me). You can check other beautiful websites I built before:
    - [Joe Hu's 2025 - The Year of Vibe Coding](https://hubeiqiao.com/2025/)
    - [Protect Ontario Graduate Pathways | Comment on OINP Proposal 25-MLITSD019](https://oinp.hubeiqiao.com/)
    - [Theories and Mechanisms for AI-Powered ESL Speaking System Design](https://eslr.hubeiqiao.com/)
- **Write**: Assignment, Report (Honestly speaking, Claude Code is able to complete most of your assignments even over 100+ pages project report in a few hours as long as you provided enough context information.)

**As long as a task can be done on your computer, Claude Code is likely to complete it.**

# Key Principles

I believe these are things that remain unchanged in the short term.

### 1. Your Demands: Detailed Documentation First

Articulate what you want. Most issues arise because you don't know what you want or haven't clarified your requirements. Since I don't know the code, this is the core part to validate if AI understands my demands by reading documents. I also think it's a crucial step for all of these AI tools.

### 2. Context Window Management

**What is the context window?** In short, it's the memory of AI. Opus 4.5 has a 200K context window. It's not enough for bigger tasks. Additionally, the performance will go down as the context window fills up.

**The Context Quality Curve**

```
Quality of Output
     |
100% |--------,
     |        |\\
 80% |        | \\
     |        |  \\ <- "Lost in the Middle" begins
 60% |        |   \\
     |        |    \\____
 40% |        |         \\___
     |        |              \\___
 20% |        |                   \\
     +--------+--------------------> Context Usage %
            20%   40%   60%   80%  100%

```

**Key insight:** Quality degrades non-linearly. The last 20% of context is poison.

*Source: [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172)*

**To manage the issue of context window, we need to:**

- Break the tasks down into smaller pieces
- Implement tasks one at a time
- Document the status
- Use Subagent and compact manually
- ... (we will discuss more later)

### 3. Manual Testing is the Key

Manual testing is the key to delivering the better result with your taste. However, it takes time...

### 4. Mindset: Stay Curious and Keep Your Passion

Ask any questions. If AI's response has any unreasonable areas, ask it to clarify. You can say you don't know how to code, but you can't say you don't know the logic. Even if you don't know some technical terms, you can always ask AI to explain them to you. Your curiosity and consistent passion are the key to continuously work with these extraordinary products.

![Pushback and Investigate](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/02-pushback-investigate-deeper.png)

# My Workflow

## Before Running Claude Code

**Use the native build** (install it with homebrew)! Much nicer syntax highlighting. This is the reply I received from Claude Code creator [Boris Cherny (@bcherny)](https://x.com/bcherny).

You can also run Claude Code on Claude Desktop directly now if something doesn't work on your terminal. (P.S. Anthropic just released [Cowork](https://techcrunch.com/2026/01/12/anthropics-new-cowork-tool-offers-claude-code-without-the-code/) on January 12, 2026 for non-technical people to use Claude Code in a more user-friendly way. The raw text and polishing were handled by Claude Cowork.)

## Decision Tree

**Coding project:**

- Big or main feature -> Claude Code local
- Other unrelated features -> Claude Code web (run multiple in parallel even on your smartphone!)

![Claude Code Web Parallel Sessions](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/04-claude-code-web-parallel-sessions.png)

**Visualization:**

- Document -> Claude Code with Opus 4.5 in Plan mode with Frontend design Skills

Additionally, I always have a markdown editor alongside to draft my thoughts and prompts.

## Draft Plan

This is the most important phase. Spend time here to save time later.

### 1. No AI. Just Write What I Want First

Don't worry about the grammar. Just write. Even for this sharing session, I wrote my raw thoughts first.

![Raw Draft Statistics](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/05-raw-draft-statistics.png)

### 2. Send the Raw Text to Claude Code (CC)

Refer to other context (for example, mention the specific document like `docs/PHASE_9_NEXT_STEPS.md`) to Claude Code, start with **Plan mode** and add `ultrathink`. Generally, CC will ask you some questions to clarify. You answer and will get version 1 of the document.

![Plan Document Phases](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/06-plan-document-phases.png)

![Plan Verification Steps](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/07-plan-verification-steps.png)

### 3. Use the "ask-questions-if-underspecified" Skill

Always add: *"If you have any questions, use 'ask-questions-if-underspecified' to ask me questions."* If I don't know the answers to some questions, I usually type "follow the best practice".

![Ask Questions Skill Example](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/08-ask-questions-skill-example.png)

### 4. Read the Document Carefully

If you have any questions, send the feedback to CC. Back and forth.

### 5. For Big Projects, Clear Context and Review Again

If this is a big project or a crucial feature, I will clear the context window and send the draft document to CC again to allow it to review it and I also send the feedback back-and-forth. I  usually have 3 rounds. I will also let CC break it down into different phases. I will have another specific document for each phase. For each phase, break it down into small tasks that can be verified at each step. This usually takes several hours per phase document. This is absolutely worthwhile. It's better than dealing with future revisions later.

![Document Version History](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/09-document-version-history.png)

### 6. Allow CC to Check the Status Before Coding

You can allow CC to check the status before coding and documenting. This will allow CC to check and verify the code itself (the actual status) to enhance the documentation.

![Pre-Implementation Checklist](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/10-pre-implementation-checklist.png)

### 7. Allow AI to Draft the Plan Visually

Allow AI to draft the plan visually with diagrams and even UI prototype with elements. This shows you more directly what you want and allows you to change it before coding.

![Visual UI Mockup](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/11-visual-ui-mockup.png)

### 8. For Bug/Issue, Investigate First. Don't Code.

If it is a bug/issue, let CC write an issue and investigate/reproduce it first. Don't code.

![Bug Investigation Document](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/12-bug-investigation-document.png)

### Tips for Planning

- **Shift + Tab** switches to Plan Mode. The benefit of the Plan mode is that it will automatically launch subagent to search for the information (save the context window) and write a plan and seek your feedback first.

![Plan Mode Subagents](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/03-plan-mode-subagents.png)

- Add `ultrathink` if it's a huge and complex task

## Execution

I'd suggest learning some basic git, CLI, and **version control** knowledge to help you feel more confident. Return to the fundamentals.

### 1. Start with Plan Mode Again

Once I have a plan, I will clear the context window and start with plan mode again to implement it. In my main product, I always open a new branch to add new features and debug.

![New Branch Plan Mode](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/13-new-branch-plan-mode.png)

### 2. If Something Broken, Escape Escape (Rewind)

If something is broken, press Escape twice (Rewind) to pick the restore point.

### 3. Run /context to Monitor Context Window

Run `/context` or install some plugins to understand the current context window consumption.

![Context Usage Display](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/14-context-usage-display.png)

### 4. Compact Context Window

While people recommend compacting the context window manually, for my convenience, I still use auto-compact. But I will manually compact it when I see this information. I will run `/smart-compact` first to show me the preserved information and then run `/compact` to compact it.

![Auto Compact Notification](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/15-auto-compact-notification.png)

### 5. Update Documents After Execution

After the execution, allow CC to update documents to keep the documentation consistent.

![Document Update Diff](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/16-document-update-diff.png)

### 6. Visualize the Logic

To help you understand the code better, tell CC to write a document to list and visualize the logic. You may not know the code but you should know the logic and control it.

![State Machine Diagram](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/17-state-machine-diagram.png)

### About [CLAUDE.md](http://claude.md/)

`CLAUDE.md` is the document that allows CC to read each time. I didn't write [CLAUDE.md](http://claude.md/) from scratch. I copied from others and talked with AI to keep it simple.

## Test and Deploy

### 1. Manual Test

Manually test to make sure it matches my requirements. Of course you might not cover all the edge cases but at least you can check that the core workflow works.

### 2. Run /pre-flight

Use `/pre-flight` to review the code, add comments, write unit tests, update the document.

![Test Suite Running](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/18-test-suite-running.png)

(Issue: I have over 2000 tests, how can I make the full test suite run faster?)

### 3. Learn GitHub PR, Issue, CI Workflow

Learn how GitHub PR, issue, CI workflow work. (Frankly speaking, I didn't know what a PR was 3 months ago until I used Claude Code Web... and gradually became more confident enough to build a real product). I think these automatic workflows help people like me to maintain the quality. But the issue is that you need to think about updating these tests each time you adjust/add new features.

I still need to learn about how to set different priorities for CI workflows. Otherwise, costs add up quickly.

![GitHub PR Checks Passed](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/19-github-pr-checks-passed.png)

### 4. Code Review

Create a PR and Claude Code/Codex will review the code and send the feedback to Claude Code back and forth. But you need to ask AI to evaluate this code review feedback before implementing it.

### 5. For UI Features, Use Browser Tools

For UI features, you can use Claude Code Web MCP to allow Claude to validate it. [Vercel Agent Browser](https://github.com/vercel-labs/agent-browser) was also released this week (save a lot of context window).

![Dev Browser Skill](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/21-dev-browser-skill.png)

### 6. Deployment Pipeline

For my current real product, I have: **localhost -> Vercel preview -> staging -> main**

For general products: **localhost -> Vercel preview -> main**

![Vercel Deployments](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/22-vercel-deployments.png)

(P.S. I just learned that if it is a commercialized product, you need to subscribe to Vercel Pro otherwise your project might be disabled. The hobby project is just for personal use.)

## Debug

### 1. Be a PM to Help AI Solve Issues

Just like my previous work, be a PM to help R&D solve issues, provide some suggestions as an outsider. It's your responsibility to provide AI with more evidence (log, behaviour), for example, ask AI to add logs and help AI to find the issue. It is your responsibility to provide more context and evidence to help AI. Report a bug professionally.

### 2. Document Issues Each Round

If AI is always breaking one feature, tell AI to document issues each round and write reflections. For example, to allow Gemini and code to capture the band score each time, I have `docs/BAND_SCORE_REGRESSION_LESSONS.md` to fix 15 issues. Additionally, after fixing a regression, ask CC to add tests to prevent it from happening again.

![Incident History Reference](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/20-incident-history-reference.png)

### 3. Compare with a Workable Commit

Once you have a workable node, in the future, if a feature is broken, you can ask AI to check that commit to learn from the pattern.

### 4. Search Online for API Issues

If AI continues to be stuck on the same issue and says it's an API issue, you might search online and find a similar situation. I experienced the Google Gemini Live API transcript issue.

![API Limitation Discovery](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/23-api-limitation-discovery.png)

### 5. Use Other Tools

Use other tools like Codex or Cursor debug. Feed the feedback to each other. (I just used codex-5.2-xhigh to help CC to solve the PWA app icon issue last Sunday)

### 6. Sentry and PostHog for Production

Use Sentry and PostHog for production analysis. Ask AI to monitor the log if it is on the production and have a smooth workflow to have enough evidence to fix the bug if users report. (I'm now building this workflow)

### 7. Use /investigate

Use `/investigate` to investigate an issue. Also, break the task down, or just investigate one issue each time.

![Investigate Command Report](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/24-investigate-command-report.png)

### 8. Ctrl + V for Screenshots

Use **Ctrl + V** to add screenshots for visual bugs.

# Tips Summary

- Using Plan Mode and ultrathink
- Using Claude Code Web simultaneously
- Realizing the context management (or even engineering)
- Slash commands: `/context`, `/compact`, `/clear`
- Custom slash commands: `/investigate`, `/pre-flight`, `/smart-compact` (I shared the full text at the end)
- Use Twitter/X to get the latest info. If you want to learn more about how to use these tools, you'd definitely need to use Twitter/X. Feel free to follow me [Joe Hu (@hubeiqiao) on X](https://x.com/hubeiqiao)!

# Discussion

- What is something I don't realize I don't know but I should know? (Something I don't know how to ask about) Do you have any suggestions about my workflow?
- What's your workflow? Do you have any tips you want to share?
    - How do you manage context window? When do you use compact? When do you start a new conversation?
    - How can we get AI to run tests faster?
    - Do you have any tips about using hooks?
    - "Error: File content (27944 tokens) exceeds maximum allowed tokens (25000). Please use offset and limit parameters to read specific portions of the file, or use the GrepTool to search for specific content." Should I try to keep the per doc tokens within 25K intentionally?

# One More Thing

99% of people don't realize Claude Code's potential. This is the opportunity for all of us.

What does the world look like next year? Or how could my process be improved? On-demand software generation is truly approaching (while it's still a monthly timeline to build a whole application by myself now). My feeling is that the true bottleneck is myself...

# Appendix: My Tool List

![Context Usage Detailed](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/25-context-usage-detailed.png)

![Tools Agents Skills List](My%20Claude%20Code%20Workflow%20How%20a%20Product%20Person%20Ships/26-tools-agents-skills-list.png)

**/preflight**

```
---
description: Review code, add comments, write tests, and run quality checks
allowed-tools: Read, Write, Bash(npm test:*), Bash(npm run lint:*), Bash(npm run format:*), Bash(git:*)
argument-hint: [file-or-directory]
---

Review and test: $ARGUMENTS

## Rules:
- **NO regressions** - run `npm test` after EVERY file change
- **NO logic changes** - only add comments, never modify functional code
- If tests fail after a change -> revert immediately with `git checkout -- <file>`

## Process:

1. **Baseline**: Run `npm test` first. If failing, STOP.

2. **Review code** for bugs, security issues, and missing error handling

3. **Add comments**:
   - Explain WHY, not what
   - Document edge cases and assumptions
   - Reference related code/docs

4. **Write tests** for new functionality (target 80% coverage)

5. **Run quality checks**:
   npm run lint && npm run format && npm test
   Revert any change that breaks tests.

6. **Update** `/tests/README.md` with new test files or testing instructions

7. **Report**: Show test results, linting summary, and files changed

```

**/ask-questions-if-underspecified**

```
---
name: ask-questions-if-underspecified
description: Clarify requirements before implementing.
---

# Ask Questions If Underspecified

## Goal

Ask the minimum set of clarifying questions needed to avoid wrong work; do not start implementing until the must-have questions are answered (or the user explicitly approves proceeding with stated assumptions).

## Workflow

### 1) Decide whether the request is underspecified

Treat a request as underspecified if after exploring how to perform the work, some or all of the following are not clear:
- Define the objective (what should change vs stay the same)
- Define "done" (acceptance criteria, examples, edge cases)
- Define scope (which files/components/users are in/out)
- Define constraints (compatibility, performance, style, deps, time)
- Identify environment (language/runtime versions, OS, build/test runner)
- Clarify safety/reversibility (data migration, rollout/rollback, risk)

If multiple plausible interpretations exist, assume it is underspecified.

### 2) Ask must-have questions first (keep it small)

Ask 1-5 questions in the first pass. Prefer questions that eliminate whole branches of work.

Make questions easy to answer:
- Optimize for scannability (short, numbered questions; avoid paragraphs)
- Offer multiple-choice options when possible
- Suggest reasonable defaults when appropriate (mark them clearly as the default/recommended choice)
- Include a fast-path response (e.g., reply `defaults` to accept all recommended/default choices)
- Include a low-friction "not sure" option when helpful
- Separate "Need to know" from "Nice to know" if that reduces friction

### 3) Pause before acting

Until must-have answers arrive:
- Do not run commands, edit files, or produce a detailed plan that depends on unknowns
- Do perform a clearly labeled, low-risk discovery step only if it does not commit you to a direction

### 4) Confirm interpretation, then proceed

Once you have answers, restate the requirements in 1-3 sentences, then start work.

```

**/smart-compact**

```
---
description: Compact context with explicit preservation rules
---

Perform a smart compaction:

## MUST PRESERVE (never summarize away):
1. Current task/goal
2. All file paths mentioned in last 10 messages
3. Any explicit decisions or constraints I stated
4. Error messages and their solutions
5. The current plan/checklist if one exists

## CAN SUMMARIZE:
1. Exploration that led to dead ends
2. Verbose output from commands (keep just the conclusion)
3. File contents that haven't been modified
4. General discussion that led to decisions (keep just decisions)

## FORMAT:
After compaction, start your next message with:

📦 Context compacted. Preserved:
- [key item 1]
- [key item 2]
- [current goal]

Now perform /compact with these rules in mind.

```

**/investigate**

```
---
description: Deep dive into a bug or behavior
allowed-tools: Read, Grep, Glob, Bash(git log:*), Bash(git blame:*)
argument-hint: [issue-description]
---

Investigate: $ARGUMENTS

Follow this systematic process:

## Phase 1: Understand
- What is the expected behavior?
- What is the actual behavior?
- When did this start? (check git log if relevant)

## Phase 2: Locate
- Search for relevant code with Grep
- Trace the code path from entry point
- Identify all files involved

## Phase 3: Analyze
- Use git blame to understand history
- Look for recent changes that might have caused this
- Check for related issues/patterns elsewhere

## Phase 4: Report
Provide a structured report:
1. **Root Cause**: [one sentence]
2. **Affected Files**: [list]
3. **Recommended Fix**: [approach]
4. **Risk Assessment**: [what could break]
5. **Test Plan**: [how to verify]

Do NOT make any changes. Investigation only.

```

# References

Official Documentation

- [Claude Code Overview](https://code.claude.com/docs/en/overview)
- [Claude Code Documentation](https://code.claude.com/docs)

Research

- [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172)

Community Resources

- [Claude Code Mastery: Advanced Patterns](https://pastebin.com/Hy59QYnC)
- [Vibe Engineering - Simon Willison](https://simonwillison.net/2025/Oct/7/vibe-engineering/)
- [Just Talk To It - Peter Steinberger](https://steipete.me/posts/just-talk-to-it)
- [Vercel Agent Browser](https://github.com/vercel-labs/agent-browser)
- [Vercel Agent Skills (react-best-practices)](https://github.com/vercel-labs/agent-skills)

X Posts

- [Boris Cherny (@bcherny) - Claude Code Creator](https://x.com/bcherny/status/2007179832300581177)
- [Tibo (@thsottiaux) - Codex tips](https://x.com/thsottiaux/status/2006624792531923266)

*Last updated: January 14, 2026*

*This document was drafted by [Joe Hu](http://hubeiqiao.com) and polished with Claude Cowork.*