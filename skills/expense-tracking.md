# Expense Tracking Skill

Automates the tedious work of categorizing receipts and logging expenses. Turn photos of receipts into audit-ready expense records.

## What It Does

The Expense Tracking skill:

1. **Accepts receipt photos** (smartphone photos of paper receipts)
2. **Extracts key data** (vendor, date, amount, description, category)
3. **Categorizes expenses** against your chart of accounts
4. **Flags unusual items** (personal vs. business, potential duplicates)
5. **Creates QB entries** (with your approval)
6. **Organizes by project** (if you track expenses by client/project)

## When to Use

- **Weekly:** Batch-process receipts collected during the week
- **As needed:** Log individual expense immediately when incurred
- **Monthly:** Before month-end close, ensure all receipts are recorded

## Setup

### Prerequisites
- QuickBooks Online
- Claude for Small Business enabled
- QB chart of accounts set up (expense categories defined)
- QB project/customer setup (if tracking by project)

### Configuration Steps

1. **In Claude Cowork**, toggle "Claude for Small Business" on
2. **Authorize QB connection**
3. **Select "Expense Tracking"** skill
4. **Configure QB account:**
   - Select checking account for expenses (where paid from)
   - Optional: Create expense report project for personal reimbursements
5. **Set categorization rules:**
   - Default categories for common vendors (e.g., "Starbucks" → Office Supplies)
   - Flags for large expenses (e.g., > $500 requires manual review)
   - Require project coding for all expenses (yes/no)
6. **Expense limit:** Set approval threshold (e.g., > $1,000 requires manager review)

## Usage

### Quick Start
```
Open Claude Cowork
→ Claude for Small Business
→ Track Expenses
→ "Upload Receipt" or "Batch Upload"
```

### Step 1: Submit Receipt
You can:
- **Take a photo** on your phone → upload to Claude
- **Email receipt PDF** → Claude picks it up
- **Upload Excel/CSV** → Claude parses rows
- **Receipt app integration** → Sync from Expensify, Dext, etc.

### Step 2: Claude Extracts Data
Claude reads receipt and extracts:

```
Vendor:        Staples
Date:          2026-02-15
Amount:        $145.67
Items:         Printer ink (x2), Paper (white, 500 sheets), Desk organizer
Category:      Office Supplies
Project:       General Operations (if relevant)
Suspicious?:   No
```

### Step 3: Review & Approve
Claude asks:
- "Does this look right?" Show extracted data
- "Change category?" (if unsure)
- "Assign to project?" (if tracking by client)
- "Personal reimbursement?" (if you paid out of pocket)

**You can:**
- ✅ Approve
- ✏️ Correct category or amount
- 🚫 Reject (duplicate, personal, etc.)
- 📸 Ask for clarification (if receipt is blurry)

### Step 4: Create QB Entry
Claude creates a QB journal entry (for your approval):

```
Debit:   Office Supplies Expense     $145.67
Credit:  Checking Account                      $145.67
Description: Staples - printer ink, paper, organizer
Date: Feb 15, 2026
Reference: Receipt photo on file
```

You approve, and Claude posts to QB.

### Batch Processing

For multiple receipts, you can:
1. Collect receipts in a folder
2. Upload all at once to Claude
3. Claude extracts all data
4. You batch-review and approve
5. Claude creates QB entries for all at once

**Example workflow:**
```
Monday morning
↓
Upload 8 receipts from last week
↓
Claude extracts all 8, shows summary
↓
You review: Approve 7, flag 1 for follow-up
↓
Claude posts 7 entries to QB
↓
Done in 10 minutes
```

## Output

After logging expenses:

1. **Expense Log** — All expenses submitted with categories and status
2. **QB Entries** — Journal entries created and posted
3. **Receipt Archive** — Photos organized by date and category
4. **Expense Report** (optional) — Summary for your records or accountant

## Troubleshooting

### "Receipt Photo is Blurry"
- Claude will ask for better photo
- Retake photo in better light
- Or provide info manually (date, vendor, amount)

### "Amount is Hard to Read"
- Claude will highlight the unclear part
- You can type the amount manually
- Or provide receipt in digital format if available

### "Wrong Category Assigned"
- Claude will ask which category is correct
- You can select from your QB chart of accounts
- Claude learns your preferences over time

### "Expense Marked as Suspicious"
Claude flags items that might be:
- Personal (e.g., meal at Starbucks)
- Duplicate (similar vendor/amount/date)
- Out of policy (e.g., entertainment > limits)
- Wrong account (expense vs. fixed asset)

**What to do:**
- Confirm if business or personal
- For personal: Create reimbursement expense report
- For others: Provide explanation (Claude notes it)

### "QB Connection Lost"
- Reauthorize QB: Settings → Connected Apps → QB → Reauthorize
- Clear browser cache and try again

## Best Practices

1. **Log receipts frequently** — Don't wait until month-end; process weekly
2. **Use same vendors** — Claude learns "Staples = Office Supplies" and auto-categorizes
3. **Keep photos organized** — Take receipt photos in good light, in landscape
4. **Document unusual items** — Add note if expense is non-standard
5. **Review categorization** — Correct Claude's guesses so it learns your preferences
6. **File receipts digitally** — Keep photo with QB entry for audit trail

## Advanced Features

### Project-Based Expense Tracking
If you work with clients or manage projects:
- Tag expenses with project/client code
- Claude tracks project expenses separately
- Easy to bill back expenses to customers
- Generate project expense reports for billing

**Example:**
```
Vendor: AWS (cloud hosting)
Amount: $342.15
Project: Client X - Website Hosting
Billable?: Yes
Bill-back rate: 100% (pass through)
↓
QB: Billing entry created
Invoice to Client X: $342.15 + markup
```

### Personal Reimbursement Workflow
If you pay personal expenses and reimburse yourself:
1. Upload personal receipt
2. Flag as "Personal Reimbursement"
3. Claude creates:
   - Expense entry (appropriate category)
   - AR entry to you (personal receivable)
4. When you reimburse yourself: Mark AR as paid

### Policy Enforcement
Claude can flag expenses that violate policy:
- Meals > $25 per person
- Hotels > $200/night
- Flights > economy class
- Entertainment > pre-approved limits

Configuration:
```
Policy Rules:
- Meals: < $25 per person
- Hotels: < $200/night
- Travel: Economy or coach
- Entertainment: Pre-approve anything > $50
```

## Integration with Other Skills

- **Month-End Close:** Ensures all expenses recorded before close
- **Payroll Planning:** Expense tracking shows cash outflows for forecast
- **Tax Prep:** Organized expenses feed into tax preparation
- **Reimbursement:** Personal expenses tracked for employee reimbursement

## Related Resources

- [QB Chart of Accounts Setup](../docs/integration-guide.md#chart-of-accounts)
- [Expense Report Template](../templates/expense-report.xlsx)
- [Receipt Management Best Practices](../docs/faq.md#receipt-management)

---

**Last Updated:** 2026-09-27  
**Maintained By:** Eric Boulou
