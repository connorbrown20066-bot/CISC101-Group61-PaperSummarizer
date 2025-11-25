This repository contains the Research Paper Summarizer built from the meta-prompt. The project follows the PS2 specification, the Week 10 TDD work, and the modular structure used in the Travel Planner example.

System Prompt

The system_prompt.md file defines rules for the summarizer. It sets greeting rules, tone rules, user inputs, boundaries, and required output parts. It controls the full workflow.

Modules Folder

The modules folder holds the internal architecture.

01_intake_setup.md
Reads inputs, normalizes section names, detects missing or short sections, and applies word limits.

02_section_loop.md
Extracts text by section, keeps section order, and writes summaries using consistent terms and PS2 limits.

03_guardrails.md
Checks for missing or empty sections, flags short sections, lowers hallucination risk, and uses chunking rules for long text.

04_rendering.md
Builds the final output with summaries, tables, glossary, and warnings.

05_key_contributions.md
Lists the main contributions in three to five points.

06_equation_explainer.md
Pulls equations and gives short explanations.

Paper Summaries

This folder stores generated outputs, including the full paper summary, the section summaries, the table, the expert and lay summaries, the glossary, and the warnings.

Documentation

The docs folder holds the verification paragraph, the flowchart, and the written reflections.
