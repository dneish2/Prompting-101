# Domain-Specific Prompt Template Guide & Cheat Sheet

This guide provides a unified, single-page resource for creating effective AI prompt templates across various domains. Designed with a human-centered approach, it uses tables and clear modular sections to ensure ease of use and scalability. Whether you're in coding, customer support, finance, legal, marketing, healthcare, education, or HR, this guide will help you get started quickly and intentionally.

---

## Table of Contents
1. [Coding & Software Engineering](#coding--software-engineering)
2. [Customer Support](#customer-support)
3. [Finance & Investment](#finance--investment)
4. [Legal & Compliance](#legal--compliance)
5. [Marketing & Creative Copy](#marketing--creative-copy)
6. [Healthcare & Medical](#healthcare--medical)
7. [Education & Training](#education--training)
8. [Human Resources & Organizational Communication](#human-resources--organizational-communication)
9. [Quick Reference Cheat Sheet](#quick-reference-cheat-sheet)
10. [Final Thoughts & Next Steps](#final-thoughts--next-steps)

---

## 1. Coding & Software Engineering

**Overview:**  
Craft prompts that generate or troubleshoot code with precision. Clearly specify language details, libraries, and constraints to yield accurate, runnable code.

**Template Structure:**
- **Context:** Programming language, version, libraries, constraints  
  *Example:* "Python 3.9, standard library only."
- **Task Description:** Describe the function or problem  
  *Example:* "Write a recursive function to calculate the factorial."
- **Expected Output:** Include one or more example input/output pairs.

**Example Prompts Table:**

| Example # | Context                             | Task Description                                         | Expected Output                        |
|-----------|-------------------------------------|----------------------------------------------------------|----------------------------------------|
| 1         | Python 3.9, standard library only   | Write a recursive function to compute factorial          | `factorial(5)` returns `120`           |
| 2         | JavaScript ES6                      | Create a function to debounce another function           | Function delays execution until idle   |
| 3         | Rust 1.70                           | Implement a thread-safe counter using Mutex              | Counter that can be shared across threads safely |
| 4         | C# with Entity Framework            | Retrieve top 5 most expensive products from database     | LINQ query with descending order and `Take(5)`     |
| 5         | Python, Pandas                      | Merge two DataFrames on a common column with left join   | DataFrame with merged rows using `merge(..., how='left')` |

**Benefits & Pitfalls:**  
- **Benefits:** Produces clear, syntactically correct code; ideal for debugging.  
- **Pitfalls:** Ambiguity in context or constraints can lead to unexpected outputs.

---

## 2. Customer Support

**Overview:**  
Generate empathetic, professional responses for customer inquiries. Define context and tone to ensure consistency and clarity in communication.

**Template Structure:**
- **Context:** Product/service details and customer background  
  *Example:* "Customer experiencing smartphone connectivity issues."
- **Task Description:** Specify the type of response (e.g., troubleshooting, apology)  
  *Example:* "Draft a supportive email response."
- **Expected Output:** Outline the structure (greeting, acknowledgment, solution, closing).

**Example Prompts Table:**

| Example # | Context                                             | Task Description                                      | Expected Output Description                                  |
|-----------|-----------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------------|
| 1         | Customer has connectivity issues with a smartphone  | Draft an empathetic email with troubleshooting steps  | Greeting, problem acknowledgment, step-by-step instructions, and a friendly close |
| 2         | Refund requested after product arrived damaged      | Write a refund confirmation with apology              | Confirmation message, apology, and refund timeline details  |
| 3         | Customer complains about delayed shipping           | Provide estimated shipping time and reassurance       | Status update with expected delivery date and empathy        |
| 4         | Subscription cancellation request                   | Confirm cancellation and offer alternatives           | Confirmation message with optional retention offer           |
| 5         | FAQ clarification request from elderly customer     | Write a simplified explanation with supportive tone   | Clear bullet point explanation and optional phone support offer |

**Benefits & Pitfalls:**  
- **Benefits:** Ensures a consistent tone and timely response.  
- **Pitfalls:** Overly rigid templates might come off as impersonal; allow some personalization.

---

## 3. Finance & Investment

**Overview:**  
Create prompts for analytical and clear financial insights. Focus on precision, structured analysis, and a formal tone.

**Template Structure:**
- **Context:** Financial scenario, market conditions, and asset specifics  
  *Example:* "Analyze a mid-cap tech company's performance during a downturn."
- **Task Description:** Define the analytical query  
  *Example:* "List key risks including market, operational, and financial factors."
- **Expected Output:** Specify the format (e.g., bullet points, risk ratings).

**Example Prompts Table:**

| Example # | Context                                                   | Task Description                                               | Expected Output Description                                       |
|-----------|-----------------------------------------------------------|----------------------------------------------------------------|-------------------------------------------------------------------|
| 1         | Mid-cap tech company in a volatile market                 | Provide a risk analysis covering market, operational, and financial risks  | Bullet list of risks with brief explanations; include disclaimer |
| 2         | High-yield bond portfolio in rising interest rate climate | Summarize exposure and recommend hedging strategy              | Exposure assessment and strategy suggestions in bullets           |
| 3         | Personal investment for a 35-year-old professional        | Recommend asset allocation with moderate risk tolerance        | Portfolio mix percentages and brief rationale                     |
| 4         | 10-K filing for a biotech startup                         | Highlight financial red flags and cash flow status             | Summary table with flagged items                                 |
| 5         | ESG score evaluation for Fortune 500 firm                 | Provide report on environmental and governance factors         | ESG score interpretation with key initiative breakdown            |

**Benefits & Pitfalls:**  
- **Benefits:** Standardizes complex financial queries.  
- **Pitfalls:** Ensure to include disclaimers to clarify that outputs are informational, not financial advice.

---

## 4. Legal & Compliance

**Overview:**  
Generate precise legal content using clear and formal language. Ensure adherence to legal terminology and include necessary disclaimers.

**Template Structure:**
- **Context:** Jurisdiction, document type, case details  
  *Example:* "Review a confidentiality clause under New York law."
- **Task Description:** Specify the legal task  
  *Example:* "Summarize key obligations and flag ambiguous terms."
- **Expected Output:** Define the format (summary, bullet points, etc.).

**Example Prompts Table:**

| Example # | Context                                               | Task Description                                                | Expected Output Description                                   |
|-----------|-------------------------------------------------------|-----------------------------------------------------------------|---------------------------------------------------------------|
| 1         | Confidentiality clause in a contract (New York law)   | Summarize key obligations and list any ambiguous language       | A concise summary followed by bullet-pointed obligations      |
| 2         | GDPR privacy policy for a SaaS product                | Generate a compliant data retention paragraph                   | Formal policy statement referencing specific articles          |
| 3         | Employee handbook for California office               | Draft anti-harassment section aligned with state law            | Clearly defined policy in paragraph format                    |
| 4         | Non-compete clause review for Texas jurisdiction      | Identify enforceability and potential issues                    | Legal bullet summary with risk annotations                    |
| 5         | NDA template for external consultants                 | Fill in missing definitions and adjust for Australian law        | Completed template with clause-level comments                 |

**Benefits & Pitfalls:**  
- **Benefits:** Enhances clarity and consistency in legal documents.  
- **Pitfalls:** Always include a disclaimer noting that the output is not legal advice.

---

## 5. Marketing & Creative Copy

**Overview:**  
Design prompts to generate creative, engaging content that aligns with brand messaging. Focus on tone, creativity, and market relevance.

**Template Structure:**
- **Context:** Define the product, target audience, and brand tone  
  *Example:* "Campaign for a new eco-friendly water bottle targeting millennials."
- **Task Description:** Specify the creative task  
  *Example:* "Write engaging ad copy that highlights sustainability."
- **Expected Output:** Outline the structure (headline, body, call-to-action).

**Example Prompts Table:**

| Example # | Context                                               | Task Description                                      | Expected Output Description                          |
|-----------|-------------------------------------------------------|-------------------------------------------------------|------------------------------------------------------|
| 1         | New eco-friendly water bottle for millennials         | Create ad copy emphasizing sustainability              | Headline, engaging body text, and a clear call-to-action |
| 2         | Launch of AI writing assistant targeting startups     | Write a product launch email                          | Engaging subject line, intro paragraph, and CTA       |
| 3         | Rebranding for a luxury skincare line                 | Draft tagline options reflecting premium quality       | 3 tagline ideas with brief tone explanation           |
| 4         | Social media promo for national coffee day            | Design a tweet + Instagram caption                     | Short, witty copy with hashtags and emoji use         |
| 5         | Landing page for an online course about UX design     | Write the hero section copy                           | Headline, subheadline, and value props bullets        |

**Benefits & Pitfalls:**  
- **Benefits:** Aligns creative outputs with brand identity and market trends.  
- **Pitfalls:** Avoid generic messaging by ensuring specific brand attributes are included.

---

## 6. Healthcare & Medical

**Overview:**  
Generate educational and clinical summaries safely. Use clear language and include necessary disclaimers to indicate that outputs are for informational purposes only.

**Template Structure:**
- **Context:** Patient demographics, symptoms (using simulated data), and clinical context  
  *Example:* "45-year-old patient with chest pain and shortness of breath."
- **Task Description:** Define the clinical task  
  *Example:* "Summarize the clinical scenario with potential diagnoses and recommendations."
- **Expected Output:** Specify the format (e.g., bullet points, structured summary).

**Example Prompts Table:**

| Example # | Context                                               | Task Description                                          | Expected Output Description                                         |
|-----------|-------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------|
| 1         | 45-year-old with chest pain and shortness of breath   | Summarize clinical scenario and list potential causes      | Bullet points for symptoms, possible diagnoses, and a disclaimer    |
| 2         | Pediatric patient with fever and rash                 | Create differential diagnosis list                         | Structured bullet list with disclaimer                              |
| 3         | Senior with dizziness and blurred vision              | Generate an ER triage summary                             | SOAP-style summary with observations and next steps                 |
| 4         | Diabetic patient follow-up summary                    | Draft a patient-friendly visit summary                     | Plain-language explanation of current status and care plan          |
| 5         | Request for layman-friendly explanation of hypertension | Translate a medical article into 6th-grade reading level  | Simplified summary with analogies and definitions                   |

**Benefits & Pitfalls:**  
- **Benefits:** Provides a structured format for clinical summaries and educational content.  
- **Pitfalls:** Always include a disclaimer to clarify that this is not diagnostic advice.

---

## 7. Education & Training

**Overview:**  
Produce structured educational content that is clear, engaging, and tailored to the target audience. Emphasize step-by-step explanations.

**Template Structure:**
- **Context:** Specify subject area, educational level, and learning objectives  
  *Example:* "High school algebra focusing on quadratic equations."
- **Task Description:** Define the teaching task  
  *Example:* "Explain quadratic equations with definitions, examples, and practice problems."
- **Expected Output:** Outline the lesson structure.

**Example Prompts Table:**

| Example # | Context                                               | Task Description                                             | Expected Output Description                                 |
|-----------|-------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------|
| 1         | High school algebra class on quadratic equations       | Explain quadratic equations with examples and practice problems | An introductory explanation, detailed steps, and sample problems |
| 2         | Corporate onboarding for new engineering hires         | Create a technical intro session plan                        | Agenda, modules, time blocks, and key concepts summary       |
| 3         | College biology intro class                            | Describe photosynthesis using visuals and analogies          | Definition, analogy-based breakdown, and a diagram caption   |
| 4         | Early childhood numeracy lesson                        | Teach counting with rhyme-based activities                   | Story prompt, rhyme activity, and interactive task idea      |
| 5         | Online course for adult learners on time management    | Generate lesson outline with tips and case study             | Modular structure with real-world examples                   |

**Benefits & Pitfalls:**  
- **Benefits:** Enhances learning through structured and interactive content.  
- **Pitfalls:** Adapt language and complexity to suit the audience's level.

---

## 8. Human Resources & Organizational Communication

**Overview:**  
Craft prompts to streamline internal communications with clarity, empathy, and consistency. Useful for policy updates, announcements, and feedback.

**Template Structure:**
- **Context:** Describe the HR scenario or internal communication need  
  *Example:* "Announcing a new remote work policy."
- **Task Description:** Define the communication objective  
  *Example:* "Draft an internal email explaining policy changes."
- **Expected Output:** Specify the format (greeting, policy details, next steps).

**Example Prompts Table:**

| Example # | Context                                               | Task Description                                               | Expected Output Description                                  |
|-----------|-------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------|
| 1         | New remote work policy announcement                    | Draft an internal email with a friendly tone and clear instructions  | Email with greeting, detailed policy changes, and actionable next steps |
| 2         | Quarterly performance review period                    | Write a reminder to managers with evaluation links             | Email with instructions, links, and due date                 |
| 3         | Mental health awareness month                          | Create a Slack message with supportive resources               | Concise message with empathy and helpful links               |
| 4         | Office relocation notice                               | Draft an FAQ for employees about logistics                     | FAQ format with address, timeline, and commuting options     |
| 5         | DEI (Diversity, Equity, Inclusion) training launch     | Write announcement with mission alignment statement            | Email or post with schedule and signup form                  |

**Benefits & Pitfalls:**  
- **Benefits:** Promotes clear and empathetic communication within the organization.  
- **Pitfalls:** Avoid overly standardized language; include opportunities for personalization.
---

## Quick Reference Cheat Sheet

| Domain                          | Key Components            | Primary Focus                    | Critical Tip                                      |
|---------------------------------|---------------------------|----------------------------------|---------------------------------------------------|
| **Coding & Software Engineering**   | Context, Task, Examples    | Clarity, syntax, efficiency       | Specify language version and constraints explicitly. |
| **Customer Support**            | Context, Task, Structure   | Empathy, tone, consistency       | Allow for personalized touches while keeping structure. |
| **Finance & Investment**        | Context, Task, Analysis    | Precision, structured analysis   | Always include a disclaimer for informational outputs. |
| **Legal & Compliance**          | Context, Task, Format      | Clarity, legal precision         | Include a legal disclaimer to clarify non-advisory status. |
| **Marketing & Creative Copy**   | Context, Task, Framework   | Creativity, brand alignment      | Tailor outputs to reflect specific brand attributes. |
| **Healthcare & Medical**        | Context, Task, Summary     | Clarity, safety, disclaimers     | Use simulated data and always add a disclaimer. |
| **Education & Training**        | Context, Task, Lesson Plan | Step-by-step clarity, engagement | Adjust language complexity to match the audience.  |
| **HR & Org. Communication**    | Context, Task, Email Format| Clarity, empathy, consistency    | Balance standardized formats with personalization. |

---

## Final Thoughts & Next Steps

- **Iterate & Expand:**  
  This guide is designed as a living document. As you gain experience, add additional example rows and adjust the template structure to fit emerging needs.
  
- **Collaborate & Share:**  
  Use this guide as a starting point across your teams. Gather feedback, share successful templates, and continuously refine the examples.
  
- **Stay Informed:**  
  Keep abreast of new prompting techniques and domain-specific best practices by following relevant research and industry trends.

Intentional, thoughtful prompting is the key to unlocking AI’s full potential. Happy prompting and continuous learning!

---

## Additional Resources
- [OpenAI Prompting Guide](https://openai.com/blog/openai-prompting-guide)
