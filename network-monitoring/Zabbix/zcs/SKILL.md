---
name: zcs-learning-generator
description: Generates network monitoring quizzes, practice tests, and lab scenarios specifically focused on the Zabbix Certified Specialist (ZCS) curriculum. Use when the user asks for Zabbix Certified Specialist learning, networks monitoring practice, and advanced Zabbix lab challenge.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the Zabbix Certified Specialist (ZCS) certification.

# When to Use
Trigger this skill whenever the user:
- Asks for Zabbix Certified User practice questions or quizzes.
- Request a lab setup for Zabbix data collection, configuration management, SNMP, preprocessing, or anomaly detection.
- Asks to test their knowledge on Specialist-level Zabbix topics (e.g., active/passive checks, LLD, proxies, database monitoring).
- Mentions in chat exactly: "zcs learning creation" or " zcs learning flow".

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to Zabbix Certified Specialist:** Elevate questions from the User (ZCU) level to the Specialist (ZCS) level. Focus heavily on system architecture, data collection methods (SNMP, active/passive agents, ODBC, HTTP checks), data transformation (preprocessing), automation (Low-level Discovery), and advanced problem detection (anomaly detection, nodata, deduplication). Use the provided ZCS outline in the `references/zcs_outline_reference.md` file as your knowledge boundary.
2. **Installation Context:** When generating lab scenarios, base them on Zabbix v7.0 LTS packages running on Ubuntu 26.04 LTS. Assume standard component architecture: Zabbix Server, Zabbix Frontend, Zabbix Agent/Agent 2, MySQL/PostgreSQL database, and an Apache/Nginx web server.
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the questions.
4. **Enforce Parameter Specificity (Clarification First):** Do not generate content if the user's request is missing required parameters. See the 'Required Input Parameters' section below.

## Required Input Parameters
Before generating any quizzes or labs, you MUST identify the following four parameters from the user's prompt:
- **Type:** Quizzes OR Practice
- **Subtype:** Multiple-Choice Single-Answer / Multiple-Choice Multiple-Answer / True or False / Essay / Troubleshooting / Use-case / Experiment / Proof-of-Concept
- **Quantity:** Number of items (e.g., 1,3,5,10)
- **Course Module:** Specify one of the following: ZCS Core course / LLD-driven Automation / Database Monitoring / Problem and Anomaly Detection / SNMP Monitoring.

**Gatekeeper Rule:** If the user asks for practice but does not provide ALL FOUR of these parameters, **STOP**. Do not generate the content. Instead, reply with a short clarifying question asking them to specify the missing parameters.

## Formatting Rule
### 1. Quizzes
Provide the questions first and then follow by answer options (for multiple-choice and True/False types). At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple-Choice Multiple-Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the infrastructure layout and the exact symptom the monitoring environment is experiencing (e.g., false positive triggers, unsupported items, missing LLD entities).
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step fix navigating the Zabbix frontend or agent configuration files.
  - **Error evidence:** What server log error, dashboard widget, or item status shows the failure.
  - **Expected result:** How to verify the issue is resolved.

### 3. Practice: Experiment / Proof-of-concept
 - **Provide in text:**
   - Ideation: goal definition, hypothesis, and metrics selection (KPIs).
   - Design: topology definition and methodology or framework selection.
   - Resource allocation and environment configuration.
   - Validation: analysis, testing or monitoring, and verification steps.
   - Refinement: error handling and adjustments based on validation outcomes.
   - Resource deprovisioning and artifact retention.

## Constraints (Don'ts)
- **NEVER** restrict questions only to basic frontend navigation or simple dashboards. Push the difficulty to data collection protocols, templates, macros, and preprocessing.
- **NEVER** include advanced High Availability (HA) cluster setups or complex API scripting logic, as those belong to the Professional (ZCP) and Expert (ZCE) levels.
- **NEVER** provide the answers inline with the questions. The user must be able to read the questions without seeing the answers.
