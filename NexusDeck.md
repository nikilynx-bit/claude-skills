# 🧠 SKILL: NexusDeck Slide Architect
**Version:** 2.6.0 | **Category:** Productivity / Presentation Design  
**Triggers:** "create slides", "powerpoint", "presentation", "pitch deck", "slide deck"  
**Core Philosophy:** Slides are not documents; they are visual catalysts for decision-making. Prioritize signal over noise, cognitive ease, and narrative momentum.

---

## 🔄 Phase 1: The Socratic Alignment (MANDATORY)
Before generating *any* content, if the user's request lacks specific details, you MUST ask up to 3 high-leverage questions to calibrate the output. Do not proceed until answered (or until the user explicitly says "use your best judgment").

1. **Audience & Objective:** "Who is the primary audience (e.g., C-suite, technical team, investors), and what is the *single* action or decision you want them to make by the end of this deck?"
2. **Source & Constraints:** "Are we building from scratch, adapting an existing template/brand, or synthesizing a provided document? What is the target slide count (e.g., 5, 10, 15)?"
3. **Tone & Visual Identity:** "What is the desired tone (e.g., authoritative, visionary, educational)? Do you have brand hex codes, or should I apply a default style (e.g., 'Sharp Corporate', 'Soft Minimalist', 'Data-Dense')?"

---

## 🏗️ Phase 2: Cognitive Architecture & Outline
Once aligned, generate a **Slide Blueprint** in Markdown. Every presentation must follow a narrative arc and utilize these 5 canonical slide types:

| Slide Type | Purpose | Cognitive Rule |
| :--- | :--- | :--- |
| **1. Cover** | Hook & Context | Title + Subtitle + Date/Presenter. Zero clutter. |
| **2. Executive Summary / TL;DR** | The "Bottom Line Up Front" | Max 3 bullet points. The entire deck's value proposition. |
| **3. Section Divider** | Narrative Reset | Large typography, single evocative keyword or phrase. |
| **4. Content (Data/Concept)** | Core Argument | **The 5/5/5 Rule:** Max 5 words per line, 5 lines per slide. Suggest 1 visual replacement (chart, icon, diagram) for every 3 bullet points. |
| **5. Summary / Call to Action** | Closure & Next Steps | Clear, numbered next steps or a single, powerful closing quote. |

*Novelty Check:* For every "Content" slide, you must append a `[Visual Suggestion: ...]` tag (e.g., `[Visual Suggestion: Replace bullets 2 & 3 with a 2-column comparison matrix]`).

---

## 🎨 Phase 3: Design System Contract
When generating code (e.g., `python-pptx` or `PptxGenJS`) or detailed markdown, adhere to this strict theme contract:

```json
{
  "theme": {
    "primary": "1A1A2E",       // Deep navy/black for titles & high contrast
    "secondary": "16213E",     // Secondary dark for accents
    "accent": "E94560",        // Vibrant highlight for key data points/CTAs
    "light": "F0F0F0",         // Light backgrounds or secondary text
    "font_heading": "Inter, Arial, or Montserrat",
    "font_body": "Segoe UI, Arial, or Roboto",
    "layout": "16:9 (10in x 5.625in)"
  }
}
