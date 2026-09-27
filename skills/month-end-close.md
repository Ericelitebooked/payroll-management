# Month-End Close Skill

Automates the tedious work of closing your books. Reconciles QB against bank/PayPal statements, flags discrepancies, and exports a close packet for your accountant.

## What It Does

The Month-End Close skill:

1. **Reconciles QB balance** against PayPal settlement and bank statements
2. **Identifies discrepancies** (transactions in one place but not the other)
3. **Flags out-of-balance accounts** that need investigation
4. **Generates plain-English P&L summary** for quick business review
5. **Exports close packet** with all supporting documents for accountant
6. **Creates month-end checklist** of items to review before final close

## When to Use

- **Last business day of month:** Official monthly close
- **Before tax reviews:** Quarterly or when CPA wants clean books
- **After large transactions:** To ensure one-time items are accounted for

## Setup

### Prerequisites
- QuickBooks Online (Desktop partially supported)
- PayPal Business account (if you accept payments via PayPal)
- Bank account(s) connected to QB (for reconciliation)
- Claude for Small Business enabled

### Configuration Steps

1. **In Claude Cowork**, toggle "Claude for Small Business" on
2. **Authorize QB and PayPal** connections
3. **Select "Month-End Close"** skill
4. **Configure accounts:**
   - QB Operating Account (main checking)
   - PayPal Settlement Account (if applicable)
   - Credit card accounts (if tracked in QB)
5. **Set expected close date:** End of month (QB will set default)
6. **Choose reporting level:**
   - Summary Close (top-level only)
   - Detailed Close (all accounts and categories)

## Usage

### Quick Start
```
Open Claude Cowork
→ Claude for Small Business
→ Month-End Close
→ "Start"
```

### Step 1: Initiate Close
Claude begins by:
- Pulling your QB trial balance (all accounts)
- Checking PayPal settlements for the month
- Comparing QB to bank/PayPal statements
- Flagging any timing differences (normal during close)

### Step 2: Review Reconciliation Report
Claude shows:
- QB Operating Account Balance: $X
- Bank Statement Balance: $X
- Difference: $0 (or amount that needs investigation)

**For each difference:**
- Transaction date and amount
- QB record vs. bank record
- Likely cause (timing, duplicate, missing entry)
- Claude's recommendation

**Example:**
```
Discrepancy: $250
QB: Feb 15, Invoice #1024 paid
Bank: Feb 19, Deposit recorded
Likely cause: 3-day bank processing delay
Recommendation: Normal. QB is correct; bank will catch up on Feb 19.
Action: No entry needed. Mark as reconciled.
```

### Step 3: Resolve Discrepancies
For each discrepancy, you can:
- ✅ **Mark as reconciled** (if timing-related or explained)
- 📝 **Create QB entry** (if missing from QB)
- 🏦 **Mark as outstanding** (check deposit not yet cleared)
- 📞 **Flag for investigation** (you'll review with accountant)

Claude can auto-create QB journal entries for simple issues (like missing deposits or fees).

### Step 4: Review P&L Summary
Claude generates a plain-English P&L:

**Example:**
```
MONTH-END SUMMARY - February 2026

REVENUE
Sales (Services)        $45,000
Sales (Products)        $12,500
Total Revenue          $57,500

EXPENSES
Payroll                 $20,000
Rent                     $3,000
Supplies                   $800
Software                 $1,200
Utilities                  $600
Marketing                 $2,500
Professional Services    $1,500
Depreciation               $200
Total Expenses          $29,800

NET PROFIT             $27,700
Net Margin              48%

KEY INSIGHTS:
- Revenue up 12% vs January
- Payroll increased due to new hire onboarding
- Marketing spend good ROI (traced to 5 enterprise deals)
- Outstanding invoices: $18,500 (collected within 10 days typical)

ALERTS:
- None this month. Clean close.
```

### Step 5: Accountant Close Packet
Claude exports and organizes:

1. **Trial Balance** — All GL accounts with balances
2. **Reconciliation Detail** — Bank/PayPal rec with supporting docs
3. **P&L Detail** — Revenue and expenses by category
4. **Balance Sheet** — Assets, liabilities, equity
5. **Journal Entries** — All entries created during month
6. **Invoice Aging** — Customer invoices, age, status
7. **Bill Aging** — Vendor bills, age, status
8. **Notes** — Any anomalies or items requiring CPA review

**Output:** ZIP file with all documents organized by category.

### Step 6: Final Approval
You review:
- ✅ All discrepancies resolved or explained
- ✅ P&L makes sense (matches your expectations)
- ✅ No unexpected large transactions
- ✅ Payroll and major expenses look correct

Then you:
- 🔐 **Lock the month** in QB (prevents future edits to closed period)
- 📤 **Export close packet** to send to accountant
- 📧 **Email to accountant** with note about any issues

## Output

After completing Month-End Close:

1. **Reconciliation Report** — QB vs. bank/PayPal with discrepancy analysis
2. **P&L Summary** — Plain English + detailed GL breakdown
3. **Balance Sheet** — Current financial position
4. **Accountant Close Packet** — All supporting docs in one ZIP
5. **Month-End Checklist** — Action items completed, sign-off

## Troubleshooting

### "QB and Bank Balance Don't Match"

**Common causes:**
- Timing: QB recognizes invoice when issued; bank recognizes when payment clears
- Fees: Bank charges fees that QB may not have recorded yet
- Transfers: QB shows transfer initiated; bank shows received on different date
- Duplicate: Transaction recorded twice (rare but worth checking)

**How to fix:**
- Review last 5-10 transactions in QB vs. bank statement
- Ask Claude to flag expected timing delays
- If genuine error: Create QB journal entry to adjust
- If bank error: Call bank to investigate

### "Some QB Accounts Not Showing in Report"
- Accounts with zero balance are hidden by default
- QB may not sync inactive accounts (ask Claude to show all)
- Subaccounts may be rolled up under parent account

### "P&L Numbers Don't Match My Expectations"
- Likely cause: Timing differences between when you incur vs. record expense
- Example: January invoice; paid in February; goes in February P&L
- Work with accountant to understand accrual vs. cash basis differences

### "Close is Taking Too Long"
- QB may need to sync larger transaction history
- Run during off-hours if QB is slow
- Try a smaller date range first (week, rather than month)

## Best Practices

1. **Close at the same time each month** — End of business day on last business day
2. **Review QB daily** — Don't let transactions pile up; clean as you go
3. **Reconcile often** — Don't wait until month-end; do weekly or bi-weekly
4. **Document discrepancies** — Note why something was adjusted (helps CPA)
5. **Lock the month** — Prevents accidental changes after close
6. **Share with accountant early** — Let them flag issues before final close

## Pro Tips

### Automate the Close
- Schedule Month-End Close skill to run automatically on 28th of each month
- Claude prepares close packet; you review and approve on the last day
- Saves 30-60 minutes vs. manual process

### Revenue Recognition
- If you use accrual accounting: Show revenue when earned (not when paid)
- If you use cash basis: Show revenue when payment received
- Claude can format reports either way; confirm with accountant

### Expense Accruals
- Estimate expenses incurred but not yet invoiced (utilities, contractors)
- Add as accrual entry at month-end; reverse in next month
- Gives more accurate P&L (accrual) without manual bookkeeping

## Integration with Other Skills

- **Payroll Planning:** Uses month-end balance to forecast next month's cash
- **Invoice Chasing:** Identifies AR aging to prioritize collections
- **Expense Tracking:** Ensures all expenses categorized before close
- **Tax Prep:** Month-end closes feed into year-end tax preparation

## Related Resources

- [QB Account Setup](../docs/integration-guide.md#quickbooks-setup)
- [Bank Reconciliation Guide](../docs/integration-guide.md#bank-reconciliation)
- [Close Packet Template](../templates/close-packet-template.xlsx)

---

**Last Updated:** 2026-09-27  
**Maintained By:** Eric Boulou
