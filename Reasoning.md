## Design Choices Rationale

### Why I Worded It This Way

- **"Guide them to understand error messages and analyze code independently"** – Emphasizes the learning objective over problem-solving. The word *independently* signals that the goal is skill-building, not immediate fixes.
- **"Response Process" structure** – Numbered steps because debugging is inherently sequential. The AI needs a clear workflow: acknowledge → identify → guide. Ensures consistent, focused responses.
- **Observable code signals (Simple/Structured/Complex)**   – Uses concrete code characteristics the AI can observe, making adaptation decisions objective rather than subjective.

### How It Avoids Giving Solutions

**Multiple prevention layers:**
- **Direct prohibition:** "Never give corrected code" with specific redirect language.  
- **Progressive escalation:** The concept → strategy → location → specifics structure ensures AI starts broadly, and only gets specific after students attempt solutions.  
- **Pseudocode boundary:** Illustrates concepts without providing drop-in fixes.  
- **Trigger-based specificity:** "Only if they try your suggestions and remain stuck" creates a clear threshold.

**Redirect strategy:** "Let's figure out why this isn't working" reframes fix-requests as learning opportunities maintaining the collaborative teaching dynamic.

### How It Encourages Student-Friendly Feedback

- **Tone adaptation:** Complexity levels get matching communication styles – encouraging for simple code, professional for complex code.  
- **End with specific next step:** Every interaction moves learning forward rather than leaving students hanging.  
- **Error-type specific approaches:** Syntax errors handled differently from logic errors; targeted strategies for each.  
- **Multiple error handling:** Prioritize the most blocking issue first to prevent overwhelming students, while acknowledging other issues.

---

## Reasoning (Required Responses)

### What tone and style should the AI use when responding?

The AI should adapt its tone based on code complexity signals:

- **Simple code:** Encouraging, patient, and explanatory. Use analogies and step-by-step guidance.
  *Example:* "That's a common mistake! Think of variables like labeled boxes..."  
- **Structured code:** Professional but supportive. Use standard terminology while maintaining helpfulness, focus on systematic approaches and best practices.  
- **Complex code:** Concise and peer-like. Focus on architecture, optimization, and advanced debugging tools.

**Consistent across all levels:** Respect student's effort, avoid condescension, and always end with actionable guidance.

### How should the AI balance between identifying bugs and guiding the student?

- **70/30 rule:** 70% guidance, 30% identification.  
- **Identification approach:** Point to *type* of error and *general area*, without pinpointing exact lines.  
  *Example:* "This looks like a scope issue in your loop logic" rather than "Line 15 has the wrong variable."
- **Guidance emphasis:** Focus on *how* to find and understand the bug:  
  - "Try adding print statements to see what's happening..."  
  - "What do you think this error message is telling you?"  
  - "Test your assumptions by..."  
- **Progressive disclosure:** Start with concepts; escalate to specifics only when students show they’ve tried suggested approaches. This ensures they learn the debugging process, not just the fix.

### How would you adapt this prompt for beginner vs. advanced learners?

**The prompt already handles this through observable code signals:**

- **Beginners (simple code signals):**  
  - More encouragement and reassurance  
  - Explicit explanations of fundamentals  
  - Emphasis on print-statement debugging  
  - Step-by-step guidance  
  - Normalize common mistakes  

- **Advanced learners (complex code signals):**  
  - Assume familiarity with core concepts  
  - Focus on architecture and performance considerations  
  - Suggest sophisticated debugging tools (debuggers, logging, profiling)  
  - Engage in peer-to-peer discussion style  
  - Address design trade-offs and best practices  

**Key insight:** Rather than asking the AI to guess experience levels, the prompt uses objective code characteristics. Simple code gets beginner-appropriate help; complex code gets advanced guidance. This prevents mismatched communication styles and ensures the response fits the actual debugging context.
