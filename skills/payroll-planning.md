# Payroll Planning Skill

Automates the most critical payroll task: ensuring you have cash to make payroll on time.

## What It Does

The Payroll Planning skill connects to your QuickBooks and PayPal accounts to:

1. **Pull current cash position** from QB
2. **Review recent settlements** from PayPal (incoming customer payments)
3. **Forecast cash flow** for the next 30 days based on payment patterns
4. **Rank overdue invoices** by amount and days outstanding
5. **Queue payment reminders** for customers who owe money
6. **Generate payroll approval report** with recommended payment date and amount

## When to Use

- **Weekly:** Every Monday to monitor cash position
- **Before payroll:** 3-5 days before payroll date to ensure funds are available
- **After large expenses:** To adjust forecast after major payments or purchases

## Setup

### Prerequisites
- QuickBooks Online or Desktop (connected to Claude)
- PayPal Business account (connected to Claude)
- Claude for Small Business enabled

### Configuration Steps

1. **In Claude Cowork**, toggle "Claude for Small Business" on
2. **Authorize connections:**
   - Select QuickBooks → Sign in → Grant Claude access
   - Select PayPal → Sign in → Grant Claude access
3. **Select "Plan Payroll"** skill from available options
4. **Confirm QB account** (QB will show your company name)
5. **Set payroll schedule:**
   - Frequency (weekly/bi-weekly/monthly)
   - Payroll date
   - Typical payroll amount

## Usage

### Step 1: Initiate the Skill
```
Open Claude Cowork
→ Claude for Small Business
→ Plan Payroll
→ "Start"
```

### Step 2: Review Claude's Analysis
Claude will pull and display:
- Current QB cash balance
- PayPal settlements (last 30 days)
- Upcoming expected payments
- 30-day cash forecast chart
- Overdue invoice list (ranked by age and amount)

### Step 3: Approve or Adjust
Claude will present a payroll recommendation:
- ✅ "You have $X. Payroll of $Y can be processed."
- ⚠️ "You're short $X. Recommend delaying payroll 2 days or accelerating invoice follow-up."
- ❌ "Insufficient funds. Recommend vendor negotiation or short-term financing."

**You can:**
- Approve the recommended payroll date
- Adjust the payroll date based on expected payments
- Ask Claude to prioritize collection of specific invoices

### Step 4: Execute Payment Reminders
Claude queues payment reminders for overdue invoices. **You review and approve each email before it sends.**

Sample email Claude drafts:
```
Subject: Payment Due - Invoice #1042

Hi [Customer Name],

I noticed Invoice #1042 for $[amount] is now [X days] past due (due date: [date]).

Could you prioritize this payment? We can accept payment via:
- Bank transfer
- Credit card
- Check

Let me know if you have questions about the invoice or need a payment plan.

Thanks,
[Your Name]
```

## Output

When you complete the Payroll Planning workflow, Claude provides:

1. **Cash Forecast Report** — 30-day projection with payment schedule
2. **Payroll Approval Document** — Signed-off recommendation for payroll processing
3. **Invoice Chase List** — Prioritized customers to contact with email drafts
4. **QB Entry Log** — Record of all follow-up actions logged to QB

## Troubleshooting

### "QB Connection Failed"
- Check your QB login credentials in Claude settings
- Verify QB account is active (not in demo mode)
- Re-authorize connection: Settings → Connected Apps → QB → Reauthorize

### "PayPal Balance Doesn't Match QB"
- This is normal if QB and PayPal have different reconciliation dates
- Claude flags these discrepancies—review them with your accountant
- Common: QB records invoice; PayPal records when payment clears (2-3 day lag)

### "Cash Forecast Shows Negative Balance"
- You likely need to accelerate customer collections
- Claude will prioritize which invoices to chase
- Consider: invoice incentives (2% discount if paid in 5 days), payment plans, or interim financing

## Best Practices

1. **Run weekly, not just before payroll** — Catch cash problems early
2. **Always approve email reminders before sending** — Personalize tone if needed
3. **Track success** — Note which follow-up strategies work best with your customers
4. **Coordinate with sales** — Let sales team know about high-priority collections
5. **Review QB regularly** — Ensure QB is up-to-date (invoices marked correct status, payments recorded)

## Integration with Other Skills

- **Invoice Chasing:** For detailed follow-up on overdue accounts
- **Month-End Close:** For reconciling QB cash position
- **Expense Tracking:** To ensure all expenses are recorded (reduces cash surprises)

## Related Resources

- [QB Reconciliation Guide](../docs/integration-guide.md#quickbooks-reconciliation)
- [PayPal Integration](../docs/integration-guide.md#paypal-integration)
- [Cash Flow Template](../templates/cash-flow-summary.xlsx)

---

**Last Updated:** 2026-09-27  
**Maintained By:** Eric Boulou
