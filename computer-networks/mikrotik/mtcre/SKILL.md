---
name: mtcre-learning-generator
description: Generates computer networking quizzes, practice labs, and lab scenarios specifically focused on the MikroTik Certified Routing Engineer (MTCRE) curriculum. Use when the user asks for OSPF or VPN questions, or MTCRE practice.
---

# Summary
This skill is designed to generate structured quizzes and practical lab scenarios to build a comprehensive learning flow for the MikroTik Certified Routing Engineer (MTCRE) certification.

# Instructions
When generating content, follow these strict behavioral rules:
1. **Scope strictly to MTCRE:** Keep questions at routing protocols. Focus on RouterOS CLI/WinBox navigation, static routing, VPN, OSPF, and Point-to-Point addressing. Use the provided MTCRE outline in the references folder as the knowledge boundary.
2. **Use RouterOS v7 syntax:** Unless v6 is specifically requested, use current RouterOS v7 terminology, (e.g., Interface Templates for OSPF, blablabla).
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the question.

## When to Use
