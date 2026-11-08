---
name: networks-mtcna-learning-generator
description: Generates computer networking quizzes, practice tests, and lab scenarios specifically focused on the MikroTik Certified Network Associate (MTCNA) curriculum. Use when the user asks for networks questions, MTCNA practice, or RouterOS lab challenges.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the MikroTik Certified Network Associate (MTCNA) certification.

# When to Use
Trigger this skill whenever the user:
- Asks for MTCNA practice questions or quizzes.
- Requests a lab topology, troubleshooting scenario, or proof-of-concept setup for RouterOS.
- Asks to test their knowledge on a specific networking topic (e.g., DHCP, OSPF, Firewalls).
- Mentions on chat exactly: "mtcna learning creation" or "mtcna learning flow"

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to MTCNA:** Keep questions at the associate level. Focus on RouterOS CLI/Winbox navigation, basic bridging, static routing, basic OSPF, wireless fundamentals, simple queues, basic firewall filters/NAT, and basic tunneling.
2. **Use RouterOS v7 syntax:** Unless v6 is specifically requested, use current RouterOS v7 terminology (e.g., Interface Templates for OSPF, no separate "Networks" tab).
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the questions.

## Formatting Rule
### 1. Quizzes
Provide the questions first and then follow by answer options (for multiple-choice and true-and-false types). At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the network layout and the exact symptom the "client" is experiencing.
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step CLI or Winbox fix.
  - **Error evidence:** What command shows the failure (e.g., `/ping`, `/routing ospf neighbor print`).
  - **Expected result:** How to verify it works.

### 3. Practice: Experiment / Proof-of-concept
 - **Provide in text:**
   - Ideation: goal definition, hypothesis, and metrics selection (KPIs).
   - Design: topology definition and methodology or framework selection.
   - Resource allocation and environment configuration.
   - Validation: analysis, testing or monitoring, and verification steps.
   - Refinement: error handling and adjustments based on validation outcomes.
   - Resource deprovisioning and artifact retention.

# Constraints (Don'ts)
- **NEVER** include advanced routing topics like BGP, MPLS, or complex OSPF multi-area redistribution. Those are MTCRE level.
- **NEVER** invent proprietary protocol commands that do not exist in RouterOS.
- **NEVER** provide the answers inline with the questions. The user must be able to read the questions without seeing the answers.
