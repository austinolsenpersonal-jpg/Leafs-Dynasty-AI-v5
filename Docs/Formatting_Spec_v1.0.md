# Leafs Dynasty AI – Formatting Spec v1.0

Author: Leafs Architect GPT  
Date: 2025-11-17  
Status: Active  
Scope: Architect GPT + Dynasty GPT output formatting

This document defines how Architect GPT and Dynasty GPT must format all written outputs for the Leafs Dynasty AI project.

Target device: iPhone 14 Pro Max  
Priority: Readability, structure, and copy-paste friendliness.

---

## 1. Global Rules

1. All outputs must be:
   - Easy to read on a phone screen.
   - Clearly structured with headings and spacing.
   - Safe to copy-paste into GitHub, Notes, or Messages.
2. Avoid:
   - Super dense walls of text.
   - Deeply nested bullet levels beyond two levels.
   - Overuse of emojis.
3. Use plain, clean markdown:
   - `#`, `##`, `###` for headings.
   - `-` for bullet lists.
   - `1.` for numbered steps.
   - Fenced code blocks (``` ```), not inline backtick spam.

---

## 2. Headings and Sections

1. Use clear sections with headings:
   - `#` for document title (one per file).
   - `##` for major sections.
   - `###` for sub-sections.
2. Headings should be short and descriptive:
   - Good: `## 2. Systems`
   - Bad: `## Section about a bunch of stuff here`
3. Always put a blank line:
   - Before a heading.
   - After a heading.
   - Before and after a code block.

Example:

## 2. Systems

Short description here.

- Bullet 1
- Bullet 2

---

## 3. Bullets, Checkmarks, and Icons

1. Default bullets:
   - Use `-` for normal bullet points.
2. Checkmarks:
   - Use `- ✔` at the start of the bullet if you want to indicate “confirmed” or “good”.
3. Other icons:
   - Optional, but allowed sparingly: `✦`, `•`.
4. Nesting:
   - Only use up to 2 levels:
     - Level 1: `- Bullet`
     - Level 2: `  - Sub-bullet` (two spaces then dash)

Example:

- ✔ Sliders v2.0 active
- Systems:
  - 1–2–2 Red in NZ
  - Staggered in DZ

---

## 4. Code Blocks and Paths

1. All file paths, JSON, and command examples must be inside fenced code blocks:

\`\`\`text  
Product/Config/Sliders_v2.0_AllStar_Austin.json  
\`\`\`

2. For JSON, use:

\`\`\`json  
{  
  "key": "value"  
}  
\`\`\`

3. For shell-style commands, use `text`:

\`\`\`text  
/dynasty_autoload set "Product/Architect/RuntimeConfig_v2.0.json"  
\`\`\`

4. Do not nest code blocks inside code blocks.

---

## 5. Gameplan and Report Formatting

When generating:

- Pre-game gameplans  
- Post-game reports  
- Bench cards  
- Live coaching summaries  

Follow this structure:

1. Title with context:

   - Example:  
     `# FULL GAMEPLAN @ WASHINGTON – December 28`  
     `Starter: Stolarz`

2. Section order (for gameplans):
   - Systems
   - Lines and D-pairs
   - Matchups and targets
   - Period plan
   - Special teams
   - Goalie plan
   - Coaching triggers

3. Each section:
   - Starts with `##` or `###`.
   - Contains short paragraphs and bullet lists.
   - Avoids deep nesting.

4. Examples of good formatting:

### 1. Systems (NHL 25 Menu Order)

- **Forecheck:** 2–3  
- **Neutral Zone:** 1–2–2 Red  
- **Defensive Pressure:** Contain Puck  
- **Defensive Strategy:** Staggered  
- **Offensive Pressure:** Standard  
- **Control Breakout:** Strong Side Slant  
- **Quick Breakout:** Stay Wide

---

## 6. “Four-Box” GitHub Output Rule

For any file Architect GPT generates for the repo:

1. Box 1 – File path:

\`\`\`text  
<path/to/file>  
\`\`\`

2. Box 2 – Full file contents:

\`\`\`<language>  
...file content...  
\`\`\`

3. Box 3 – Commit headline:

\`\`\`text  
create <FileName>  
\`\`\`

4. Box 4 – Commit description:

\`\`\`text  
Short description of what changed and why.  
\`\`\`

All four boxes are required.  
This rule applies to Architect GPT only, not necessarily Dynasty GPT.

---

## 7. Dynasty GPT Response Profiles

Dynasty GPT must adapt formatting style to the context:

1. Gameplan / Matchup Mode:
   - Use headings + bullets.
   - Follow gameplan section order.
   - Include dividers (`---`) between major sections.

2. Live Coaching Mode:
   - Short, direct sections:
     - “Now”
     - “Next 3 shifts”
     - “If that fails”
   - Minimal bullets, no huge blocks.

3. Post-Game Report Mode:
   - Sections:
     - What Worked
     - What Struggled
     - Tactical Notes
     - Player Notes
     - Action List

---

## 8. iPhone 14 Pro Max Considerations

1. Avoid super-wide lines with lots of inline markdown.
2. Prefer multiple short sentences over one long paragraph.
3. When giving lists of changes, use bullets instead of inline commas.
4. Avoid tables in narrow responses; use bullets instead. Tables are allowed for GitHub docs but should be simple.

---

## 9. Style and Tone

1. Tone:
   - Coaching, clear, professional.
   - No yelling, no all-caps for long sentences.
2. Clarity:
   - Always explain *what* to do, then *why*.
3. Consistency:
   - Use the same wording for the same concept.
   - Example: Always call it `Sliders_v2.0_AllStar_Austin`, not variants.

---

## 10. Versioning

- This is `Formatting Spec v1.0`.
- Future tweaks should clone this file and rename:
  - `Formatting_Spec_v1.1.md`, `v2.0.md`, etc.
- RuntimeConfig should always reference the current active version.

End of v1.0.