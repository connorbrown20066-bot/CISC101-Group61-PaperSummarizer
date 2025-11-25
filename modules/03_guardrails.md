Detect missing and empty sections.

Flag sections with fewer than 50 words.

Check for hallucination risks.

Add chunking rules for long papers.

  
Change Log: Nov 25, 2025
- Added strict evidence mode.  
- Added clear rules for missing, empty, and short section warnings.  
- Added exposed messages that prevent unsupported claims.

Purpose  
Reduce unsupported content, enforce evidence rules, and guide the system when the user provides weak or missing sections.

Inputs  
- section_text  
- PS2 limits  
- summary_level  
- evidence_mode  
- section length checks  

Evidence Mode  
Add a variable:  
evidence_mode = "strict" or "standard"

If evidence_mode = "strict":  
- Use only claims, equations, and results found in the provided text.  
- Do not infer or add ideas that do not appear in the section.  
- If text is not enough, output:  
  "The source text does not provide enough detail to summarize this section in strict evidence mode."

If evidence_mode = "standard":  
- Follow normal rules from the PS2 spec.  
- Keep summaries grounded in the text.  

Section Warnings  
Add warnings for quality issues:

Missing Section  
If the section is not found:  
"Section skipped: no usable text was provided."

Empty Section  
If the section text is blank:  
"Section skipped: no usable text was provided."

Short Section (< 50 words)  
"Section short: summary may be incomplete."

Hallucination Checks  
- Compare each claim to the source text.  
- Do not output content that does not appear in the text.  
- Flag weak matches for the system to handle.  

Long Text Chunking  
If the section exceeds the context window:  
- Split text into chunks.  
- Summarize each chunk.  
- Combine chunk summaries into the final section output.  
