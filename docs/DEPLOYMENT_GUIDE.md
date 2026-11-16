# RedCell - Deployment Guide

## Overview
AI red-team platform with autonomous LLM agents for end-to-end penetration testing.

## Architecture
```
FastAPI + React --> LangGraph Engine --> LLM (via LiteLLM) --> Kali Container
                       |                      |                    |
                  Plan/Act Loop          Multi-Provider       Pen Test Tools
                  Task Queue             OpenAI/Claude        nmap, metasploit
                  State Machine          Local Models         burpsuite, etc.
```

## Quick Start
```bash
git clone https://github.com/martian56/redcell.git
cd redcell
docker-compose up -d
```

## Configuration
| Variable | Description |
|----------|-------------|
| LLM_PROVIDER | LLM backend (openai, anthropic, local) |
| MODEL_NAME | Model to use for agents |
| TARGET_SCOPE | Authorized test targets |
| OUTPUT_FORMAT | pdf, json, or sarif |

## Output Formats
| Format | Use Case |
|--------|----------|
| PDF | Executive reports |
| JSON | Integration with tools |
| SARIF | CI/CD pipeline security |

## Disclaimer
For authorized security testing only. Always obtain written permission.