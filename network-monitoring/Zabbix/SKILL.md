---
name: zabbix-certified-user-learning-generator
description: Generates network monitoring quizzes, practice tests, and lab scenarios specifically focused on the Zabbix certifications curriculum. Use when the user asks for Zabbix Certified User (ZCU) learning, networks monitoring, or Zabbix lab challenge.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the Zabbix Certified User (ZCU) certification.

# When to Use
Trigger this skill whenever the user:
- Asks for Zabbix Certified User practice questions or quizzes.
- Request a Zabbix GUI navigation, access and filter data, troubleshooting scenario, or proof-of-concept setup for Zabbix dashboards.
- Asks to test their knowledge on a User-level and Zabbix GUI topics (e.g., user interface, filtering, graphs).
- Mentions on chat exactly: "zabbix certified user learning creation" or " zcu learning flow".

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to Zabbix Certified User:** Keep questions at the level 1. Focus on service monitoring, user interface, filtering, alert overview.
2. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the questions.
3. **Installation:**

## Required Input Parameters
Before generating any quizzes or labs, you MUST identify the following four parameters from the user's prompt:
- **Type:** Quizzes or Practice
- **Subtype:** Multiple-Choice Single-Answer / Multiple-Answer / True or False / Essay / Troubleshooting / Use-case / Experiment / Proof-of-Concept
- **Quantity:** Number of items (e.g., 1,3,5,10)

## Formatting Rule
### 1. Quizzes
Provide the questions first and then follow by answer options (if request subtype is multiple-choice or true-and-false types). At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple-Choice Multiple-Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the network layout and the exact symptom the "client" is experiencing.
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step fix.
  - **Error evidence:** Blablabla
  - **Expected result:** How to verify it works.

### 3. Practice: Experiment / Proof-of-concept
 - **Provide in text:**
   - Ideation: goal definition, hypothesis, and metrics selection (KPIs).
   - Design: topology definition and methodology or framework selection.
   - Resource allocation and environment configuration.
   - Validation: analysis, testing or monitoring, and verification steps.
   - Refinement: error handling and adjustments based on validation outcomes.
   - Resource deprovisioning and artifact retention.

## Constraints (Don'ts)
- **NEVER** include complexity of higher-levels. There are Zabbix Certified Specialist, Professional, and Expert levels.
- **NEVER** provide the answers inline with the questions. The user must be able to read the questions without seeing the answers.
