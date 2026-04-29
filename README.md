# 🤖 AI Application Manual QA Portfolio
### ChatGPT — End-to-End Manual Testing

[![Test Cases](https://img.shields.io/badge/Test%20Cases-32-blue)]()
[![Bugs Found](https://img.shields.io/badge/Bugs%20Found-11-red)]()
[![Pass Rate](https://img.shields.io/badge/Pass%20Rate-59.4%25-orange)]()
[![Platform](https://img.shields.io/badge/Platform-Web%20%2B%20iOS%20%2B%20Android-green)]()

## 📌 Project Summary
Executed comprehensive manual QA on the ChatGPT web application and mobile experiences across authentication, chat interface behaviour, conversation management, model switching, custom instructions, file uploads, and mobile-specific interactions. The project includes AI-specific testing strategy, usability evaluation, and security-minded input validation observations.

## 🎯 What Was Tested
| Module | Test Cases | Bugs Found |
|--------|-----------:|-----------:|
| Authentication | 7 | 1 |
| Chat Interface | 11 | 4 |
| Conversation Management | 7 | 2 |
| Model Switching | 3 | 0 |
| Custom Instructions | 3 | 1 |
| File Upload | 4 | 2 |
| Mobile | 3 | 1 |

## 🔴 Critical Defects Identified
| ID | Title | Severity |
|----|-------|----------|
| BUG-002 | File upload silently drops files over the supported limit | Critical |
| BUG-005 | Chat input hidden by keyboard on iOS Safari | Critical |
| BUG-009 | Whitespace-only prompt submitted without validation | Critical |

## 🧪 Testing Types Applied
- Functional Testing
- Boundary Value Analysis
- Negative Testing
- Session and State Testing
- Usability Testing using Nielsen's heuristics
- Exploratory Testing using SBTM charters
- Cross-browser and mobile testing

## 🔒 Security Observations
| Input Tested | Result |
|--------------|--------|
| `<script>alert('xss')</script>` in prompt | Sanitised as plain text |
| SQL injection pattern in search field | No error exposure observed |
| Session state after logout | Session cleared |
| Whitespace-only prompt submission | Defect logged as BUG-009 |

## 📁 Repository Structure
- `/docs` — Test plan, AI testing approach, usability heuristics notes, and checklist
- `/test-cases` — Manual test cases grouped by module
- `/bug-reports` — Individual defect reports plus master bug log
- `/exploratory-testing` — SBTM-style exploratory charters
- `/usability-evaluation` — Nielsen heuristics scoring report
- `/rtm` — Requirements Traceability Matrix
- `/test-reports` — Final execution summary

## 🛠 Tools Used
| Tool | Purpose |
|------|---------|
| Chrome / Firefox DevTools | Network monitoring, session inspection, console checks |
| BrowserStack | Real-device iOS and Android validation |
| Loom | Screen recording for interaction defects |
| Postman | Manual API response structure verification |
| Notion | Exploratory session notes |

## 👤 Author
**Mrunal** | Manual QA Engineer | [GitHub](https://github.com/Mruunalll)
