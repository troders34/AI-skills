---
name: mtcine-learning-generator
description: Generates computer networking quizzes, practice labs, and lab scenarios specifically focused on the MikroTik Certified Inter-Networking Engineer (MTCINE) curriculum. Use when the user asks for multi autonomous system exercise, service-provider core technologies, BGP/MPLS, and MTCINE practice.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the MikroTik Certified Inter-Networking Engineer (MTCINE) certification.

# When to Use
Trigger this skill whenever the user:
- Asks for MTCINE practice questions or quizzes.
- Requests a lab topology, troubleshooting scenario, use-case, experiment, or proof-of-concept setup for service-provider or inter-domain routing protocols.
- Asks to test their knowledge on advanced networking topics (e.g., Autonomous Systems, BGP best path selection, MPLS LDP, VPLS, Traffic Engineering, RSVP).
- Mentions on chat exactly: "mtcine learning creation" or "mtcine learning flow".

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to MTCINE:** Keep questions focused on multi-autonomous system (AS) routing and service-provider core technologies. Focus on RouterOS CLI/WinBox navigation for BGP (iBGP/eBGP, Path Vector, Route Reflectors, Confederations), MPLS (LDP, VPLS, VRF, L3VPN), and Traffic Engineering (RSVP, CSPF). se the provided MTCINE outline in the `references/mtcine_outline_reference.md` file as the knowledge boundary.
2. **Use RouterOS v7 syntax:** Unless v6 is specifically requested, use current RouterOS v7 terminology and command structures (e.g., using the modern instead of the legacy v6 /routing bgp peer menus, and v7 MPLS syntax).
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the question.
4. **Enforce Parameter Specificity (Clarification First):** Do not generate content if the user's request is missing required parameters. See the 'Required Input Parameters' section below.

## Required Input Parameters
Before generating any quizzes or labs, you MUST identify the following four parameters from the user's prompt:
- **Type:** Quizzes OR Practice
- **Subtype:** Multiple-Choice Single-Answer / Multiple-Answer / True or False / Essay / Troubleshooting / Use-case / Experiment / Proof-of-Concept
- **Quantity:** Number of items (e.g., 1,3,5,10)
- **Module:** Specific MTCRE module(s) to cover (Module 1 through 4)

**Gatekeeper Rule:** If the user asks for practice but does not provide ALL FOUR of these parameters, **STOP**. Do not generate the content. Instead, reply with a short clarifying question asking them to specify the missing parameters.

## Formatting Rule
### 1. Quizzes
Provide the questions first and then follow by answer options (for multiple-choice and true-and-false). At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple-Choice Multiple-Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the network layout and the exact symptom the "client" is experiencing.
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step CLI or WinBox fix.
  - **Error evidence:** What command shows the failure (e.g., `/routing bgp session print`, `/mpls ldp neighbor print`).
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
- **NEVER** include basic routing protocols (like static routing or basic OSPF areas) unless they are used strictly as an IGP to support MPLS/BGP infrastructure. Basic routing belongs to the MTCNA and MTCRE levels.
- **NEVER** invent proprietary protocol commands that do not exist in RouterOS.
- **NEVER** provide the answers inline with the questions. The user must be able to read the questions without seeing the answers.
