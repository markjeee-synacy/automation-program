# AUTOMATION PROGRAM

This is a platform to manage the Automation Program for RISE.

## About the Automation program

Automation is a Technology-department program at RISE. Mission: build digital intelligence infrastructure (automation + business intelligence + network intelligence) so RISE can operate at scale with precision and agility, while delivering faster, more reliable connectivity to Philippine businesses.

## About RISE

RISE is a business-only fiber internet ISP based in the Philippines, with a mission to accelerate internet access across the country by delivering high-quality, reliable fiber connectivity exclusively to enterprises, government institutions, and educational organizations.

## About this platform

This platform serves as a centralized hub for managing the Automation Program at RISE. It provides tools and resources for:

- Collect research data and insights
- Develop opportunities, initiatives, and objectives
- Track performance and impact of automation efforts

## Sub-Programs

The Automation Program is organized into four Sub-Programs, each with its own goals and execution focus:

- **Artificial Intelligence** — `program-files/programs/artificial-intelligence/`
- **Business Intelligence** — `program-files/programs/business-intelligence/`
- **Enterprise Automation** — `program-files/programs/enterprise-automation/`
- **Network Intelligence** — `program-files/programs/network-intelligence/`

The program-wide mission is recorded in `program-files/Mission.md`.

## Technology Stack of this platform

This is primarily a Markdown-based knowledge base and workflows platform. It includes scripts to manage content and files in this project.

Program-of-record content under `program-files/` (the Mission and per-Sub-Program documents) is published as a standalone website using Astro as the static site generator, self-hosted in our own AWS cloud environment, and is also published to our Confluence company account via the Atlassian MCP tool. The same `program-files/` content is co-edited in Google Docs via the Google Drive MCP tool.

Knowledge base content under `docs/kb/` is internal context only — it is not published.

Key technologies used:
- TypeScript
- Node.js
- Astro
- MCP tool: Atlassian
- MCP tool: Google Drive
