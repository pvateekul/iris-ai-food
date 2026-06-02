# OpenClaw Demo Prompts

This document contains all prompts used in the OpenClaw presentation and demonstrations.

> **Note:** Replace all placeholders in the format `<...>` with values appropriate for your use case before running the prompts.

---

## 1. Hatch the Agent — Identity Setup Prompt

Use this prompt to initialize the agent's identity, personality, timezone, and behavioral boundaries.

```md
Hi, I'm <your-name>. You are OpenClaw, my AI assistant. You can call me <your-name>. I want you to have a calm vibe.

Please set our timezone to Thailand/Bangkok. You can pick up any emoji of your choice.
For my boundaries:
- Private things stay private.
- When in doubt, ask before acting externally.
- Never sand half-baked replies to messaging surfaces.
- You are not user's voice - be carreful in group chats.
```

---

## 2. Code Generation Prompt

Use this prompt to generate a modern landing page showcasing OpenClaw capabilities.

```md
@<OpenClaw> Create a modern single-page HTML website that summarizes the capabilities of OpenClaw.

The page should include:
* A clean responsive design
* Hero section with title and short description
* Features section explaining capabilities such as:
    * AI conversations
    * Discord integration
    * Automation tools
    * Plugin system
    * Web interface
    * Docker deployment
* Simple architecture/workflow diagram using HTML/CSS
* Demo/test server section
* Footer with GitHub-style theme

Requirements:
* Generate a complete standalone `index.html`
* Use only HTML, CSS, and minimal JavaScript
* Modern dark theme UI
* Mobile-friendly layout
* Add subtle animations and hover effects
* No external frameworks required
```

---

## 3. Food Price Analysis Automation

Use this prompt to create a scheduled analytics workflow that analyzes food price volatility on a daily basis.

```md
@<OpenClaw> Please analyze the dataset food_prices.csv. Your task is to identify the top 5 foods with the highest price volatility and provide a visualization, set this task to automation everyday at 12.00 PM.
```

> Don't forget to insert `food_prices.csv` in Discord channel.

---

## 4. Testing News Searching Agent

Use this prompt to test the news search and retrieval capability.

```md
@<OpenClaw> ช่วยหาข่าวเกี่ยวกับ <หัวข้อ>
```

---

## 5. Testing News Content Agent

You can copy selected news content and source references from the **News Searching Agent** output and paste them directly into the content channel.

```md
@<OpenClaw> ช่วยเขียนข่าวเกี่ยวกับ <เนื้อหาข่าว>
```

---

## 6. AI Agent Custom Skill with OpenClaw

Use this prompt to demonstrate custom skill execution using the `vo-to-slides` skill.

```md
@<OpenClaw> Can you help make a simple slide based on the topic; <AI for food processing>. 
Please use this skill https://github.com/Samin12/vo-to-slides, download this skill and make some slides so that I can look through it and present it.
```

---

**End of Document**