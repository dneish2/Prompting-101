## 1. High‑Level Conceptual Framework
### 1.1 The Neish Prompting Model

> *“If you can’t explain it simply, you don’t understand it well enough.”* - Albert Einstein

**Why Prompting Matters**
Prompting is both an art and a science: a well‑crafted prompt unlocks the full potential of AI assistants, guiding them to deliver precise, context‑aware, and actionable output.
This guide offers clear and professional guidance to empower business users and their technical collaborators to master prompting techniques for chat interactions, email management, document creation, and data analysis in Microsoft 365.

> We distill tasks into four core components:

1. **Context** – System role or background (e.g. “You are a marketing analyst.”)
2. **Instruction** – Clear action verb + object (e.g. “Draft a summary.”)
3. **Constraints** – Format, length, tone (e.g. “in bullet points, ≤100 words.”)
4. **Examples/Variables** – Placeholders `{}` or sample input/output

### 1.2 Prompt Anatomy
| Component | Purpose | Syntax Example |
|--------------|---------------------------------------------------|-----------------------------------------|
| Context | Sets role & scope | `You are a project manager.` |
| Task | Defines the action | `Summarize the Q1 report.` |
| Constraints | Controls format, tone, length | `Use professional tone, 150 words.` |
| Variables | Marks inputs to be filled | `{sender}`, `{start_date}`, `{data}` |
| Output Spec | Describes desired structure | `Present as table with columns X, Y.` |

---

## 2. Chat: Conversational AI Across M365
| Use Case | Prompt Template | Example |
|----------------------------|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **Cross‑App Synthesis** | `Summarize key points from {doc_title}, {email_thread}, and {spreadsheet}.` | `Summarize key points from "Q2 Analysis" doc, IT email thread, and Sales spreadsheet.` |
| **Meeting Prep** | `Prepare an agenda for a meeting on {topic} with goals: {goals}.` | `Prepare an agenda for a project kickoff with goals: align scope, assign owners, set milestones.` |
| **Action Items Extraction** | `List all action items from the email thread titled "{thread_subject}".` | `List all action items from the email thread titled "Q2 Budget Discussion".` |
| **Quick Spreadsheet Query** | `In the attached spreadsheet, calculate {operation} for column "{column_name}".` | `In the attached spreadsheet, calculate the average for column "Revenue".` |

---

## 3. Email Productivity (Outlook)
| Use Case | Prompt Template | Example |
|----------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **Summarize Thread** | `Summarize the email thread from {sender} between {start_date} and {end_date}. Highlight key decisions.` | `Summarize the thread from IT Team between 2025‑04‑01 and 2025‑04‑10. Highlight key decisions.` |
| **Draft Reply** | `Draft a reply to {name}: {your_points}. Tone: {tone}, length ~{words} words.` | `Draft a reply to Sarah: apologize for delay; update on status; propose next steps. Tone: friendly, 120 words.` |
| **Extract Action Items** | `List action items and assignees from the email titled "{subject}".` | `List action items and assignees from the email titled "Q2 Budget Approval".` |
| **Schedule Follow‑up** | `Set a reminder to follow up with {contact} on {topic} by {date}.` | `Set a reminder to follow up with Finance on audit results by 2025‑05‑01.` |
| **Bulk Unsubscribe** | `Unsubscribe from all newsletters older than {days} days in {folder}.` | `Unsubscribe from all newsletters older than 30 days in Promotions.` |

---

## 4. Document Drafting (Word)
| Use Case | Prompt Template | Example |
|----------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Generate Draft** | `Write a {length}-word {doc_type} on {topic}. Include sections: {sections}.` | `Write a 500‑word report on Q1 sales. Include sections: Executive Summary, Analysis, Recommendations.` |
| **Rewrite Text** | `Rewrite the following for {tone}: "{text}".` | `Rewrite the following for a technical audience: "Our solution leverages..."` |
| **Summarize Document** | `Summarize the document titled "{title}" in {format}.` | `Summarize the document titled "Market Research 2024" in bullet points.` |
| **Style Adjustment** | `Convert the selected text to {style} style. Maintain accuracy.` | `Convert the selected text to concise style. Maintain accuracy.` |
| **Q&A** | `Answer questions about the document: {question}.` | `Answer questions about the document: "What are the main cost drivers?"` |

---

## 5. Data Wizardry (Excel)
| Use Case | Prompt Template | Example |
|--------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| **Formula Suggestion** | `Suggest a formula to calculate {metric} from columns {A} and {B}.` | `Suggest a formula to calculate profit margin from columns Revenue and Cost.` |
| **Data Analysis** | `Analyze the selected data for {insight}. Present findings in {format}.` | `Analyze the selected data for sales trends. Present findings in bullet points.` |
| **Chart Generation** | `Create a {chart_type} chart for {metric} over {period}.` | `Create a line chart for monthly revenue over the last 12 months.` |
| **Pivot Table** | `Build a pivot table showing {rows} by {columns}, values summed on {value_field}.` | `Build a pivot table showing Region by Product, values summed on Sales.` |
| **Data Cleaning** | `Identify and fix anomalies in the selected range (duplicates, missing). Report changes.` | `Identify and fix anomalies in the selected range. Report changes.` |

---

## 6. Advanced & Technical Prompting
### 6.1 Technical Prompt Examples
| Role | Use Case | Prompt Template | Example |
|------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Solution Architect** | Pattern Recommendation | `As a solution architect, analyze this system: {description}. Recommend an architectural pattern with rationale.` | `As a solution architect, analyze this e‑commerce system (inventory DB, auth, payments). Recommend a pattern and why.` |
| **Solution Architect** | Security Threat Modeling | `You are a security‑focused architect. Identify vulnerabilities in: {architecture_details}. Suggest mitigations.` | `You are a security‑focused architect. Identify vulnerabilities in this microservices setup and suggest fixes.` |
| **Developer** | Debugging Assistance | `Here is {language} code: {code}. Find bugs and suggest fixes.` | `Here is Python code: `\`def calc(x): return x / y\``. Find bugs and suggest fixes.` |
| **Developer** | Unit Test Generation | `Generate unit tests in {framework} for: {function_signature} – {function_body}. Include edge cases.` | `Generate pytest tests for: `\`def add(a, b): return a + b\``. Include edge cases.` |

### 6.2 Custom Agents & Integration Samples
```yaml
# Sample Agent manifest
name: BudgetAnalyzer
trigger: "Analyze budget for {project}"
actions:
- type: ai
prompt: "Analyze budget for {project}, highlight overruns."
```
```python
# Sample API integration
from msgraph import GraphClient
from openai import OpenAI

graph = GraphClient(...)
data = graph.get('/me/drive/root:/Budgets')
client = OpenAI()
resp = client.chat.completions.create(
model="gpt-4",
messages=[
{"role":"system","content":"You are a financial analyst."},
{"role":"user","content":f"Analyze these budgets: {data}"}
]
)
```

---

## 7. Prompting Best Practices
> Effective prompts follow these core best practices, think of them like a well‑written recipe: precise ingredients, clear steps, and exact measurements.

1. **Define the Persona**
- **Why:** The assistant adopts a “voice” when you set a role.
- **How:** Begin with “You are a …” (e.g. “You are a marketing analyst.”)

2. **Frame the Task Clearly**
- **Why:** A precise instruction focuses the assistant’s reasoning.
- **How:** Use an action verb + object (e.g. “Summarize the report.”)

3. **Provide Examples**
- **Why:** Concrete samples guide style and structure.
- **How:** Include input/output pairs or fill in `{}` placeholders.

4. **Constrain the Scope**
- **Why:** Limits ambiguity and unexpected digressions.
- **How:** Specify format, tone, and length (e.g. “In 5 bullet points, ≤80 words, professional tone.”)

5. **Iterate & Refine**
- **Why:** Each refinement sharpens clarity and outcome.
- **How:** Review the output, remove ambiguity, adjust variables, and repeat.

---

*Crafted by David Neish*
