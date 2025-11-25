For each section:

Extract text.

Summarize with PS2 word limits (100–150 words).

Use consistent terms: self-attention, encoder-decoder, Transformer.

Keep the original order.


 
Change Log: Nov 25, 2025
- Added the summary_level variable.  
- Added conditional behavior for short and detailed summaries.  
- Added instructions for paragraph and bullet list outputs.

Purpose  
Process each section in the order provided by the user. Extract text, check quality, then produce a summary that follows PS2 limits and the chosen summary level.

Inputs  
- section_list  
- section_text  
- summary_level  
- PS2 limits  
- normalized section names  

Logic  
For each section in section_list:  
1. Extract the matching text from the paper.  
2. Check for missing or short sections.  
3. Keep the section order from the user.  
4. Use the terms self attention, encoder decoder, and Transformer.  

Summary Level Rules  
Set a variable:  
summary_level = "short" or "detailed"

If summary_level = "short":  
- Write a compact summary with one to two sentences.  
- Stay factual and use only text from the paper.  
- Follow PS2 limits when possible.  

If summary_level = "detailed":  
- Write a short paragraph.  
- Add a bullet list with three to five key points.  
- Use points that appear in the section text.  
- Keep the output clean and direct.  

Output  
- One summary per section.  
- The output structure must stay consistent across all sections.  
