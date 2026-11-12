---
name: zcp-learning-generator
description: Generates network monitoring quizzes, practice tests, and lab scenarios specifically focused on the Zabbix Certified Professional (ZCP) curriculum. Use when the user asks for Zabbix Certified Professional learning, advanced network monitoring practice, and ZCP lab challenges.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the Zabbix Certified Professional (ZCP) certification.

# When to Use
Trigger this skill whenever the user:
- Asks for Zabbix Certified Professional (ZCP) practice questions or quizzes.
- Request a lab setup for Zabbix High Availability (HA), proxies, API automation, advanced security, or application monitoring.
- Asks to test their knowledge on Professional-level Zabbix topics (e.g., Zabbix API, external vaults, proxy load balancing, VMware/Java monitoring, OpenTelemetry).
- Mentions in chat exactly: "zcp learning creation" or " zcp learning flow".

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to Zabbix Certified Professional (ZCP):** Elevate questions from the Specialist (ZCS) level to the Professional (ZCP) level. Focus heavily on distributed monitoring architecture (proxies, proxy groups), High Availability (HA) deployments, API automation, advanced security (external vaults, HTTPS, PSK encryption), and advanced application monitoring (Java, VMware, OpenTelemetry). Use the provided ZCP outline in the `references/zcp_outline_reference.md` file as your knowledge boundary.
2. **Installation Context:** When generating lab scenarios, base them on Zabbix v7.0 LTS packages running on Ubuntu 26.04 LTS. Assume a distributed component architecture: Zabbix Server in HA mode, multiple Zabbix proxies, Zabbix Frontend, Zabbix Agent/Agent 2, MySQL/PostgreSQL database, and an Apache/Nginx web server.
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the questions.
4. **Enforce Parameter Specificity (Clarification First):** Do not generate content if the user's request is missing required parameters. See the 'Required Input Parameters' section below.

## Required Input Parameters
Before generating any quizzes or labs, you MUST identify the following four parameters from the user's prompt:
- **Type:** Quizzes OR Practice
- **Subtype:** Multiple-Choice Single-Answer / Multiple-Choice Multiple-Answer / True or False / Essay / Troubleshooting / Use-case / Experiment / Proof-of-Concept
- **Quantity:** Number of items (e.g., 1,3,5,10)
- **Course Module:** Specify one of the following: ZCS Core course / Automation and Integration with Zabbix API / Advanced Zabbix Security Administration.

**Gatekeeper Rule:** If the user asks for practice but does not provide ALL FOUR of these parameters, **STOP**. Do not generate the content. Instead, reply with a short clarifying question asking them to specify the missing parameters.

## Formatting Rule
### 1. Quizzes
Provide the questions first and then follow by answer options (for multiple-choice and True/False types). At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple-Choice Multiple-Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the distributed infrastructure layout and the exact symptom the monitoring environment is experiencing (e.g., proxy disconnects, HA failover issues, API authentication failures, TLS handshake errors).
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step fix navigating the Zabbix frontend, API calls, or server/proxy configuration files.
  - **Error evidence:** What server log error (zabbix_server.log, zabbix_proxy.log), API response code, or GUI screen shows the failure.
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
- **NEVER** restrict questions to basic data collection (ZCS level) or basic frontend navigation (ZCU level). Push the difficulty to distributed architecture, API integration, and security.
- **NEVER** provide the answers inline with the questions. The user must be able to read the questions without seeing the answers.
