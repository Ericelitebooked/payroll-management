# Claude Context for Payroll Management System

This document provides context for Claude when working within this payroll management repository.

## Project Overview

**Name:** Payroll Management System  
**Purpose:** Automate critical payroll and finance operations for small businesses  
**Owner:** Eric Boulou (eric.elitebooked@gmail.com)  
**Repository:** https://github.com/Ericelitebooked/payroll-management

## What This Project Does

This is a practical implementation guide for using Claude AI and Anthropic's "Claude for Small Business" suite to automate:

- Payroll planning and approval (reconcile cash, forecast 30 days, approve payments)
- Invoice chasing (overdue follow-ups with automated email reminders)
- Month-end close (QB reconciliation, P&L generation, accountant prep packet)
- Expense tracking (receipt photos → categorized QB entries)
- Tax season prep (organize year-end records for CPA filing)

The system integrates with QuickBooks Online, PayPal, HubSpot, Google Workspace, and Docusign.

## Core Skills (What Claude Does for the User)

The repository documents 5 primary skills users enable via Claude for Small Business:

1. **Payroll Planning** — Ensures you have cash to make payroll, forecasts 30 days, queues collection emails
2. **Invoice Chasing** — Monitors overdue invoices, generates reminder emails (1st, 2nd, 3rd notices)
3. **Month-End Close** — Reconciles QB/PayPal, flags discrepancies, generates P&L, exports close packet
4. **Expense Tracking** — Parses receipt photos, categorizes, creates QB entries (with approval)
5. **Tax Season Prep** — Organizes year's records, identifies deductions, exports to CPA folder

Additional HR and operational skills documented:
- Employee onboarding
- HR policy Q&A
- Lead qualification and CRM updates
- Vendor/contract tracking

## Repository Structure

```
payroll-management/
├── README.md                    # Main entry point; overview of system
├── CLAUDE.md                    # This file; context for Claude
├── skills/                      # Documentation for each skill
│   ├── payroll-planning.md
│   ├── invoice-chasing.md
│   ├── month-end-close.md
│   ├── expense-tracking.md
│   ├── tax-season-prep.md
│   ├── employee-onboarding.md
│   └── hr-policy-qa.md
├── templates/                   # Excel/Markdown templates for users
│   ├── payroll-schedule.xlsx
│   ├── invoice-tracker.xlsx
│   ├── cash-flow-summary.xlsx
│   ├── expense-report.xlsx
│   └── tax-prep-checklist.md
├── docs/                        # Integration & setup guides
│   ├── integration-guide.md
│   ├── api-reference.md
│   ├── troubleshooting.md
│   └── faq.md
└── examples/                    # Real-world workflow examples
    ├── payroll-example.md
    ├── invoice-example.md
    └── close-example.md
```

## How Claude Helps (User Perspective)

Users interact with Claude through:

1. **Claude for Small Business** (native plugin)
   - Integrated directly into Claude Cowork
   - Connects to QB, PayPal, HubSpot, Google Workspace, Canva, Docusign
   - Users toggle on "Claude for Small Business" → select skill → start

2. **Claude.ai Projects** (document-based)
   - Users create Project with payroll templates and instructions
   - Upload receipts, ask Claude to categorize
   - Paste QB data; ask Claude to reconcile

3. **Claude Code** (for technical setups)
   - Setup scripts for API integrations
   - Custom workflow automation
   - MCP (Model Context Protocol) integrations

## Key Principles for This Project

1. **Approval-first workflows:** Every financial action requires user approval before execution
   - Claude drafts; user approves; Claude posts/sends
   - No autonomous financial transactions

2. **QB is source of truth:** All financial data lives in QB
   - Claude reads from QB, doesn't replace it
   - All Claude-created entries logged to QB audit trail

3. **Plain-English outputs:** P&L summaries, cash forecasts, and reports use clear language, not jargon

4. **Practical, not perfect:** System is designed to save 80% of manual work, not automate 100%
   - Some review and judgment still required
   - CPA involvement maintained for compliance

5. **Small business focused:** Solutions assume limited accounting staff
   - One person may be managing payroll, invoicing, and closings
   - Automation frees up time for strategic work

## When to Use This Repository

Claude should use this repository when:

- User asks about payroll automation for small business
- User wants to set up Claude for Small Business
- User needs help with QB integration or workflows
- User is building custom payroll systems using Claude API
- User wants templates or best practices for finance operations

Claude should reference specific files when:

- User is setting up a skill → link to skills/ documentation
- User needs integration help → point to docs/integration-guide.md
- User wants a template → link to templates/ folder
- User needs real-world example → point to examples/ folder

## Common Questions Claude May Answer

**"How do I set up payroll planning?"**
→ Point to `skills/payroll-planning.md` for step-by-step setup

**"What's the best way to track expenses?"**
→ Reference `skills/expense-tracking.md` + `templates/expense-report.xlsx`

**"How do I integrate QB with Claude?"**
→ Guide to `docs/integration-guide.md`

**"Can Claude automatically send invoice reminders?"**
→ Yes! See `skills/invoice-chasing.md`

**"What data should I prepare for tax season?"**
→ Reference `skills/tax-season-prep.md` + `templates/tax-prep-checklist.md`

## Technical Details

### Claude Models Used
- Claude Opus or Sonnet (for complex financial analysis)
- Claude Haiku (for receipt parsing and categorization)
- Claude for Small Business (for integrated workflows)

### API Integrations
- QuickBooks Online API (read/write to QB)
- PayPal Settlement API (reconciliation)
- HubSpot API (CRM updates)
- Google Workspace API (calendar, email, docs)
- Docusign API (contract workflows)

### MCP (Model Context Protocol)
- QuickBooks MCP for QB data access
- Email MCP for invoice reminders
- Cloud storage MCP for tax prep folder organization

## Important Notes

1. **Data Security:** User financial data stays in their QB/PayPal accounts. Claude never stores or trains on sensitive data.

2. **Compliance:** This system helps with compliance but doesn't replace CPA. Always have professional tax/accounting review.

3. **Approval Workflows:** Every financial action requires user approval. Claude never autonomously posts entries or sends payments.

4. **Audit Trail:** All Claude-created entries are logged with date, time, and Claude's reasoning.

## Contributing Guidelines

If adding new content to this repository:

1. **Skill documentation:** Follow format in `skills/payroll-planning.md`
   - What it does
   - When to use
   - Setup steps
   - Usage walkthrough
   - Troubleshooting
   - Best practices

2. **Templates:** Create Excel (.xlsx) or Markdown (.md)
   - Include instructions
   - Sample data
   - Formulas/logic explained

3. **Integration guides:** Document setup for each tool
   - Prerequisites
   - Step-by-step authorization
   - Testing & verification

4. **Examples:** Real workflows showing start-to-finish process
   - Sample data
   - Screenshots (if helpful)
   - Expected outputs

## Related Resources

- [Anthropic Claude for Small Business](https://claude.com/solutions/small-business)
- [Claude Documentation](https://docs.anthropic.com/)
- [QuickBooks Online Developer API](https://developer.intuit.com/)
- [Anthropic Trust Center](https://trust.anthropic.com/)

## Contact

- **Owner:** Eric Boulou (eric.elitebooked@gmail.com)
- **GitHub:** https://github.com/Ericelitebooked/payroll-management
- **Issues:** File on GitHub for bug reports or feature requests

---

**Last Updated:** 2026-09-27  
**Version:** 1.0
