---
name: zcs-learning-generator
description: Generates network monitoring quizzes, practice tests, and lab scenarios specifically focused on the Zabbix Certified Specialist (ZCS) curriculum. Use when the user asks for Zabbix Certified Specialist learning, networks monitoring practice, or Zabbix GUI lab challenge.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the Zabbix Certified Specialist (ZCS) certification.

# When to Use
Trigger this skill whenever the user:
- Asks for Zabbix Certified User practice questions or quizzes.
- Request a GUI navigation exercise, data filtering task, troubleshooting scenario, or proof-of-concept setup for Zabbix dashboards.
- Asks to test their knowledge on a User-level Zabbix frontend topics (e.g., user interface, filtering, graphs, and viewing alerts).
- Mentions in chat exactly: "zcs learning creation" or " zcs learning flow".

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to Zabbix Certified User:** Keep questions at the intermediate and specialist level. Focus on service monitoring concepts, navigating the Zabbix web interface, filtering data, and viewing alerts. Use the provided ZCU outline in the `references/zcu_outline_reference.md` file as your knowledge boundary.
2. **Installation Context:** When generating lab scenarios, base them on Zabbix v7.0 LTS packages running on Ubuntu 26.04 LTS. Assume standard component architecture: Zabbix Server, Zabbix Frontend, Zabbix Agent, MySQL/PostgreSQL database, and an Apache/Nginx web server. Unless other versions are specified, use this version.
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the questions.
4. **Enforce Parameter Specificity (Clarification First):** Do not generate content if the user's request is missing required parameters. See the 'Required Input Parameters' section below.

## Required Input Parameters
Before generating any quizzes or labs, you MUST identify the following four parameters from the user's prompt:
- **Type:** Quizzes OR Practice
- **Subtype:** Multiple-Choice Single-Answer / Multiple-Choice Multiple-Answer / True or False / Essay / Troubleshooting / Use-case / Experiment / Proof-of-Concept
- **Quantity:** Number of items (e.g., 1,3,5,10)
- **Course Module:** Specify one of the following: Core course / Fundamentals of Problem Detection / Mastering Zabbix Graphs and Dashboards / Transforming and Extracting Data with Zabbix Pre-processing.

## Formatting Rule
### 1. Quizzes
Provide the questions first and then follow by answer options (for multiple-choice and True/False types). At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple-Choice Multiple-Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the network layout and the exact symptom the "client" is experiencing.
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step fix navigation the Zabbix frontend.
  - **Error evidence:** What dashboard widget, event log, or GUI screen shows the failure or trigger.
  - **Expected result:** How to verify the issue is resolved in the UI.

### 3. Practice: Experiment / Proof-of-concept
 - **Provide in text:**
   - Ideation: goal definition, hypothesis, and metrics selection (KPIs).
   - Design: topology definition and methodology or framework selection.
   - Resource allocation and environment configuration.
   - Validation: analysis, testing or monitoring, and verification steps.
   - Refinement: error handling and adjustments based on validation outcomes.
   - Resource deprovisioning and artifact retention.

## Constraints (Don'ts)
- **NEVER** include higher-level administrative complexity (e.g., installing Zabbix Proxies, high availability setups, or writing complex custom scripts). Those belong to the Specialist, Professional, and Expert levels.
- **NEVER** provide the answers inline with the questions. The user must be able to read the questions without seeing the answers.
