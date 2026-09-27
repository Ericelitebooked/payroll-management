# Payroll Management System

Claude AI-powered payroll management system for small business. Automates payroll planning, invoicing, expense tracking, and financial reporting using Claude's latest models and integration with QuickBooks and PayPal.

## Overview

This system leverages Claude's pre-built small business agents to streamline critical payroll and finance operations:

- **Payroll Planning** — Reconcile cash positions, forecast 30-day cash needs, and prepare payroll
- **Invoice Management** — Automate overdue invoice tracking and payment reminders
- **Expense Tracking** — Categorize expenses and reconcile accounts
- **Month-End Close** — Automate book reconciliation and P&L generation
- **Tax Preparation** — Organize documents and prepare for tax season

## Features

### Finance Automation
- Payroll settlement reconciliation (QuickBooks + PayPal)
- 30-day cash flow forecasting
- Invoice tracking and payment reminders
- Expense categorization from receipts
- Monthly book reconciliation
- P&L summaries for accountants

### HR Operations
- Employee onboarding workflows
- Policy Q&A automation
- Job description and offer letter drafting
- PTO and schedule tracking

### Sales & Operations
- CRM data synchronization (HubSpot)
- Lead qualification and prioritization
- Proposal and quote generation
- Vendor contract tracking
- Calendar and meeting automation

## Integration Partners

- **QuickBooks** — Accounting, payroll planning, monthly close
- **PayPal** — Payment settlement and dispute tracking
- **HubSpot** — CRM, sales pipeline, lead management
- **Google Workspace** — Calendar, email, document management
- **Microsoft 365** — Office integration
- **Canva** — Marketing asset generation
- **Docusign** — Contract management

## Getting Started

### 1. Prerequisites
- Claude Max or Claude Team account
- QuickBooks Online (or Desktop)
- PayPal Business account
- GitHub (for version control)

### 2. Setup

#### Step 1: Clone the Repository
```bash
git clone https://github.com/Ericelitebooked/payroll-management.git
cd payroll-management
```

#### Step 2: Configure Claude for Small Business
1. Go to [Claude for Small Business](https://claude.com/solutions/small-business)
2. Toggle on "Claude for Small Business"
3. Connect your tools:
   - QuickBooks Online
   - PayPal
   - HubSpot (optional)
   - Google Workspace

#### Step 3: Set Up Skills
Follow the guides in the `skills/` directory:
- [Payroll Planning Setup](./skills/payroll-planning.md)
- [Invoice Chasing Setup](./skills/invoice-chasing.md)
- [Month-End Close Setup](./skills/month-end-close.md)
- [Expense Tracking Setup](./skills/expense-tracking.md)

#### Step 4: Use Templates
Copy templates from `templates/` and customize for your business:
- Payroll Schedule
- Invoice Tracker
- Cash Flow Summary
- Expense Report
- Tax Prep Checklist

### 3. Running Your First Payroll

1. **Open Claude Cowork** and toggle "Claude for Small Business" on
2. **Select "Plan Payroll"** skill
3. **Connect your data:**
   - QB cash position
   - PayPal settlements (last 30 days)
   - Employee rates and hours
4. **Approve the forecast** and payment plan Claude generates
5. **Process payroll** through Gusto/ADP using Claude's recommendations

## Skills Reference

### Payroll Planning
Automates the most critical step: ensuring you have cash to make payroll.

**What it does:**
- Pulls your QuickBooks cash position
- Reviews PayPal settlements and customer payments
- Forecasts your position for the next 30 days
- Ranks what's overdue
- Queues payment reminders

**When to use:** Weekly or before payroll date

**Output:** Cash forecast + payroll approval + payment plan

---

### Invoice Chasing
Keeps money flowing by automating follow-ups on overdue invoices.

**What it does:**
- Monitors all invoices in QuickBooks
- Identifies overdue accounts (1st, 2nd, 3rd notices)
- Drafts professional payment reminder emails
- Logs follow-ups in QB
- Flags accounts for review if patterns emerge

**When to use:** Daily or weekly

**Output:** Reminder email drafts (you approve before sending)

---

### Month-End Close
Removes the friction from monthly accounting work.

**What it does:**
- Reconciles QB against PayPal/bank settlements
- Flags discrepancies and out-of-balance accounts
- Generates plain-English P&L summary
- Exports close packet for your accountant

**When to use:** Last business day of month

**Output:** Reconciliation report + P&L summary + close packet

---

### Expense Tracking
Turns receipt photos into categorized, audit-ready records.

**What it does:**
- Parses expense photos or PDFs
- Extracts vendor, date, amount, description
- Categorizes against your chart of accounts
- Flags unusual or potentially personal expenses
- Logs entries to QB

**When to use:** Weekly expense review

**Output:** Categorized expense log (you approve before posting)

---

### Tax Season Prep
Organizes your year's records for your CPA ahead of tax time.

**What it does:**
- Gathers all invoices, receipts, and transaction records
- Organizes by category (income, expenses, deductions)
- Flags items that need explanation or documentation
- Exports summary for CPA
- Creates checklist of missing documents

**When to use:** November–December

**Output:** Organized tax prep folder + missing items checklist

---

## Project Structure

```
payroll-management/
├── README.md                          # This file
├── CLAUDE.md                          # Claude context and instructions
├── .gitignore                         # Git ignore rules
├── skills/
│   ├── payroll-planning.md            # Skill: Payroll planning guide
│   ├── invoice-chasing.md             # Skill: Invoice reminders
│   ├── month-end-close.md             # Skill: Monthly close procedures
│   ├── expense-tracking.md            # Skill: Expense categorization
│   ├── tax-season-prep.md             # Skill: Tax prep organization
│   ├── employee-onboarding.md         # Skill: HR onboarding
│   └── hr-policy-qa.md                # Skill: Policy questions
├── templates/
│   ├── payroll-schedule.xlsx          # Payroll schedule template
│   ├── invoice-tracker.xlsx           # Invoice tracking sheet
│   ├── cash-flow-summary.xlsx         # Cash flow forecast
│   ├── expense-report.xlsx            # Expense log template
│   ├── tax-prep-checklist.md          # Tax season prep checklist
│   └── close-packet-template.xlsx     # Month-end close packet
├── docs/
│   ├── integration-guide.md           # QB/PayPal/HubSpot setup
│   ├── api-reference.md               # Claude API and endpoints
│   ├── troubleshooting.md             # Common issues and fixes
│   └── faq.md                         # Frequently asked questions
└── examples/
    ├── payroll-example.md             # Example: Running first payroll
    ├── invoice-example.md             # Example: Invoice chase workflow
    └── close-example.md               # Example: Month-end close
```

## Common Workflows

### Weekly: Payroll Prep & Invoice Chase
1. Open Claude → "Plan Payroll" skill → Approve forecast
2. Claude → "Chase Invoices" → Review reminder drafts → Send
3. Review cash position dashboard

### Monthly: Close the Books
1. Month-end → "Close the Books" skill
2. Review QB reconciliation
3. Approve P&L summary
4. Export close packet to accountant

### Quarterly: Tax & Compliance Check
1. Review expense categorization
2. Flag any deductions to discuss with CPA
3. Organize records in tax prep folder
4. Schedule CPA review

## Security & Compliance

### Data Protection
- All financial data stays in your QuickBooks and PayPal accounts
- Claude only processes data you explicitly share
- Sensitive data is never stored in Claude's training
- Team/Enterprise plans include enhanced privacy controls

### Approval Workflows
Every financial action (payments, payroll, transfers) requires your approval before execution. Claude drafts or queues actions; you approve or reject.

### Audit Trail
- QB provides full transaction history
- All Claude-generated actions are logged
- Export reports for audit or compliance review

## Support & Resources

### Documentation
- [Integration Setup Guide](./docs/integration-guide.md)
- [Troubleshooting](./docs/troubleshooting.md)
- [FAQ](./docs/faq.md)

### Learning
- [Claude for Small Business Course](https://anthropic.skilljar.com/ai-fluency-for-small-businesses) — Free AI fluency training
- [Anthropic Trust Center](https://trust.anthropic.com/) — Security and compliance details
- [Claude API Docs](https://docs.anthropic.com/) — Developer reference

### Help
- GitHub Issues: File bugs or feature requests
- Email: eric.elitebooked@gmail.com
- Claude Cowork Community: Ask questions and share workflows

## Contributing

Found a better way to run payroll? Want to add a new skill? Contributions welcome!

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit changes
4. Push to your fork
5. Open a Pull Request

## License

MIT License — Use freely for your business.

## Changelog

### v0.1 (Initial Release)
- Payroll Planning skill
- Invoice Chasing automation
- Month-End Close workflow
- Expense Tracking setup
- Tax Season Prep guide
- Template library (5 core templates)
- Integration guides (QB, PayPal, HubSpot)

---

**Last updated:** 2026-09-27  
**Maintainer:** Eric Boulou (Ericelitebooked)

For questions or support, open an issue on GitHub or contact eric.elitebooked@gmail.com