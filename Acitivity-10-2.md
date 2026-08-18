# BOI Sri Lanka — Brand Guideline & Social Media Prompt Pack

This file contains three reusable prompts for a brand-focused AI workflow:

1. Extract brand guidelines from a supplied image or infographic and produce a structured brand guideline.
2. Convert those extracted guidelines into a reusable `SKILL.md` file.
3. Generate social media content that follows the approved brand guidelines, including logo usage, spacing, typography, colours, tone, and visual consistency.

---

# 1. Prompt: Extract Brand Guidelines from an Image / Infographic

## Use when

Use this prompt when a brand poster, infographic, campaign visual, presentation slide, social media creative, logo sheet, or other brand reference image is provided.

## Prompt

```text
You are a professional brand identity analyst and visual communication specialist.

Analyse the provided brand image, infographic, or visual reference and extract the brand guidelines that can be reliably identified from it.

OBJECTIVE
Create a clear, practical, and reusable brand guideline that can be used by designers, content creators, and AI systems to maintain visual and communication consistency.

IMPORTANT RULES
- Analyse only what is visible or clearly inferable from the supplied image.
- Do not invent colours, font names, measurements, logo rules, or brand specifications that cannot be supported by the image.
- Clearly label uncertain observations as "Approximate" or "Requires confirmation".
- Preserve the apparent intent of the original brand identity.
- Prioritise consistency, professionalism, accessibility, and readability.
- Treat logos and official marks as protected brand assets.
- Do not redraw, distort, recolour, crop, or alter logos unless the source explicitly shows that usage.

EXTRACT AND DOCUMENT THE FOLLOWING

1. Brand Identity
- Brand name
- Brand purpose or positioning, if visible
- Overall personality
- Key visual characteristics

2. Logo Usage
- Primary logo
- Secondary logo or variations
- Logo orientation
- Approximate placement
- Clear-space / safe-area guidance visible in the reference
- Minimum-size guidance if visible
- Incorrect usage examples, if shown

3. Colour Palette
For every clearly identifiable colour, provide:
- Colour name
- Approximate HEX value where possible
- RGB value where possible
- Role in the visual system, such as primary, secondary, accent, background, or text

If exact colour values cannot be reliably determined from the image, state that they are approximate and should be verified from the original brand asset.

4. Typography
Identify:
- Font family, if identifiable
- Heading style
- Body-text style
- Weight and emphasis
- Capitalisation conventions
- Alignment and hierarchy

Do not claim an exact font name unless there is sufficient evidence.

5. Layout and Spacing
Document:
- Margins
- Padding
- Alignment
- Grid or column structure
- Visual hierarchy
- White-space usage
- Image-to-text balance
- Safe areas around logos and important content

6. Imagery and Visual Style
Describe:
- Photography style
- Illustration style
- Icon style
- Graphic shapes
- Patterns
- Borders
- Shadows
- Background treatment
- Other recurring visual elements

7. Tone of Voice
Infer the communication style shown in the reference, such as:
- Formal
- Professional
- Institutional
- Approachable
- Innovative
- Premium
- Authoritative

Only state what is reasonably supported by the supplied material.

8. Social Media Application
Provide practical rules for applying the identity to:
- LinkedIn
- Facebook
- Instagram
- Other digital channels where relevant

9. Consistency Rules
Create a concise list of MUST / SHOULD / MUST NOT rules for maintaining brand consistency.

OUTPUT FORMAT

# Brand Guidelines

## 1. Brand Identity
## 2. Logo Guidelines
## 3. Colour Palette
## 4. Typography
## 5. Layout & Spacing
## 6. Imagery & Visual Style
## 7. Tone of Voice
## 8. Social Media Guidelines
## 9. Brand Consistency Rules
## 10. Items Requiring Confirmation

For every specification derived from the image, distinguish between:
- Confirmed / clearly visible
- Approximate
- Requires confirmation
```

---

# 2. Prompt: Generate a `SKILL.md` from the Brand Guidelines

## Use when

Use this prompt after a brand guideline has been extracted and you want to convert it into a reusable AI Skill that consistently follows the brand.

## Prompt

```text
You are an expert AI Skill designer and brand-governance specialist.

Using the approved brand guidelines provided below, create a complete and reusable `SKILL.md` file that teaches an AI system how to create brand-consistent communications and visual content.

OBJECTIVE
Turn the supplied brand guidelines into precise operational instructions that another AI system can follow consistently.

IMPORTANT RULES
- Do not invent missing brand requirements.
- Preserve all confirmed brand rules exactly where practical.
- Mark uncertain or approximate specifications clearly.
- Do not override official brand requirements with generic design preferences.
- Treat logos, colours, typography, layouts, and official wording as controlled brand elements.
- Use imperative instructions such as "Use", "Do not use", "Maintain", and "Avoid".
- Keep the Skill concise enough to be practical, but detailed enough to prevent inconsistent outputs.

THE `SKILL.md` MUST CONTAIN

1. YAML Frontmatter
- name: lowercase, descriptive skill name
- description: explain what the skill does and when it should be triggered

2. Purpose
Explain the role of the Skill and the brand outcomes it must protect.

3. Brand Identity Rules
Translate the approved brand identity and personality into operational instructions.

4. Logo Rules
Specify:
- Approved logo versions
- Placement
- Clear space
- Sizing
- Background rules
- Prohibited modifications

5. Colour Rules
Specify:
- Primary colours
- Secondary colours
- Accent colours
- Background colours
- Text colours
- Approximate values where applicable
- Restrictions on colour combinations

6. Typography Rules
Specify:
- Heading hierarchy
- Body copy
- Font weights
- Capitalisation
- Alignment
- Readability requirements

7. Layout and Spacing Rules
Specify:
- Margins
- Padding
- White space
- Alignment
- Visual hierarchy
- Safe areas

8. Imagery and Visual Style
Specify the appropriate photography, illustrations, icons, shapes, patterns, and supporting visual language.

9. Tone and Language
Specify:
- Tone
- Formality
- Preferred wording style
- Language conventions
- Phrases or styles to avoid

10. Social Media Rules
Provide practical instructions for creating brand-consistent social media posts.

11. Quality-Control Checklist
Create a final checklist covering:
- Logo correctness
- Colour correctness
- Typography
- Spacing
- Alignment
- Tone
- Consistency
- Accessibility/readability

12. Handling Missing Information
Tell the AI what to do when an input does not provide enough information to confidently apply a brand rule. It should ask for confirmation or use a clearly marked assumption rather than inventing a rule.

OUTPUT REQUIREMENT
Return only the complete `SKILL.md` content in Markdown.

BRAND GUIDELINES TO CONVERT:
[PASTE APPROVED BRAND GUIDELINES HERE]
```

---

# 3. Prompt: Generate a Brand-Consistent Social Media Post

## Use when

Use this prompt when creating a social media post or creative using the approved brand guidelines and, where applicable, official logo/assets.

## Prompt

```text
You are a professional government communications and brand-content specialist.

Create a social media post using the approved brand guidelines provided below.

OBJECTIVE
Produce a professional, clear, credible, and brand-consistent social media communication suitable for an official government or institutional organisation.

INPUTS
- Platform: [LinkedIn / Facebook / Instagram / X / Other]
- Campaign or topic: [INSERT]
- Key message: [INSERT]
- Target audience: [INSERT]
- Call to action: [INSERT]
- Supporting information: [INSERT]
- Approved brand guidelines: [INSERT]
- Approved logo/assets: [INSERT, if available]

BRAND COMPLIANCE RULES

1. Logo
- Use only the approved logo/assets supplied by the user or referenced in the brand guidelines.
- Never redraw, recreate, distort, stretch, rotate, recolour, or otherwise modify the logo.
- Maintain the approved clear space around the logo.
- Keep the logo visually secondary to the core message unless the brand guidelines specify otherwise.

2. Colour
- Use only approved brand colours or colours explicitly permitted by the brand guidelines.
- Maintain sufficient contrast for readability.
- Do not introduce decorative colours merely for visual appeal.

3. Typography
- Follow the approved font hierarchy, weights, and alignment.
- Do not substitute fonts when an approved font is available.
- Maintain a clear hierarchy between headline, supporting text, and call to action.

4. Layout and Spacing
- Maintain generous and consistent white space.
- Respect logo safe areas and content safe areas.
- Do not overcrowd the design.
- Keep visual hierarchy clear.
- Maintain consistent margins, padding, and alignment.

5. Visual Consistency
- Follow the approved imagery, illustration, icon, shape, pattern, and background styles.
- Ensure all visual elements look like part of the same brand system.
- Avoid unnecessary decorative elements.

6. Tone of Voice
- Use a professional, respectful, factual, and audience-appropriate tone.
- For government communications, avoid exaggerated claims, aggressive sales language, slang, or unsupported statements.
- Use concise and accessible language.

7. Content Accuracy
- Do not invent statistics, achievements, programme details, policy statements, dates, or claims.
- Use only information supplied by the user or contained in approved source material.
- Flag any information that requires verification.

OUTPUT
Provide:

A. Social Media Copy
- Headline
- Main post text
- Call to action
- Optional hashtags, limited to relevant and professional terms

B. Creative Direction
Describe the recommended visual composition, including:
- Canvas/layout
- Logo position
- Headline position
- Supporting text position
- Image placement
- Colour usage
- White space
- Call-to-action placement
- Any required visual assets

C. Brand Compliance Check
Confirm whether the proposed post complies with:
- Logo rules
- Colour rules
- Typography rules
- Spacing rules
- Visual style
- Tone of voice
- Content accuracy

When a brand specification is not available, do not guess. Mark it as "Requires confirmation".

APPROVED BRAND GUIDELINES:
[PASTE BRAND GUIDELINES HERE]
```

---

# Recommended Workflow

Use the three prompts as a simple sequential workflow:

**Brand Image / Infographic**
→ **Extract Brand Guidelines**
→ **Review & Confirm**
→ **Generate `SKILL.md`**
→ **Create Social Media Content**
→ **Run Brand Compliance Check**

For official BOI or government communications, the final human review should confirm official logos, colours, programme names, statistics, claims, dates, URLs, and any policy or investment-related statements before publication.
