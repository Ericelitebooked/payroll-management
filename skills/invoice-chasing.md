# Invoice Chasing Skill

Automates the follow-up process that keeps money flowing. Monitors overdue invoices and sends professional payment reminders on your behalf.

## What It Does

The Invoice Chasing skill:

1. **Monitors all QB invoices** for status and age
2. **Identifies overdue accounts** (0-30, 30-60, 60+ days past due)
3. **Generates professional payment reminder emails** at 1st, 2nd, and 3rd notice stages
4. **Logs all follow-ups** in QB for audit trail
5. **Flags accounts** with consistent payment issues or changing patterns
6. **Personalizes emails** based on customer history and payment patterns

## When to Use

- **Daily:** Automatic monitoring (optional)
- **Weekly:** Deliberate invoice chase session
- **Triggered:** When a specific invoice reaches 30 days past due

## Setup

### Prerequisites
- QuickBooks Online (required for invoice access)
- Claude for Small Business enabled
- Approval process configured (you approve emails before sending)

### Configuration Steps

1. **In Claude Cowork**, toggle "Claude for Small Business" on
2. **Authorize QB connection** if not already done
3. **Select "Chase Invoices"** skill
4. **Configure reminder schedule:**
   - 1st Notice: Due date + 7 days
   - 2nd Notice: Due date + 20 days
   - 3rd Notice: Due date + 35 days
5. **Set escalation rules:**
   - Escalate to yourself if invoice > 60 days overdue
   - Escalate to sales if customer has pattern of late payment
6. **Choose contact method:**
   - Email only (default)
   - Email + phone (if you provide phone numbers)

## Usage

### Quick Start
```
Open Claude Cowork
→ Claude for Small Business
→ Chase Invoices
→ "Start"
```

### Step 1: Review Overdue Invoices
Claude displays a dashboard:
- Customer name and invoice number
- Invoice amount and date
- Days overdue
- Payment history (is this customer usually late?)
- Status of previous reminder emails

### Step 2: Choose Chase Strategy
**Option A: Full Automatic** (Recommended for first time)
- Claude identifies all overdue invoices
- Generates reminder emails for each
- You review and approve in batch

**Option B: Targeted Chase**
- You select specific customers to focus on
- Claude generates personalized outreach
- You approve individual emails

**Option C: High-Priority Only**
- Claude prioritizes by amount + days overdue
- Focuses on your top 5-10 outstanding invoices
- You approve high-impact reminders first

### Step 3: Review & Approve Emails
Claude shows a preview of each email:

**1st Notice (Professional Reminder)**
```
Subject: Payment Reminder - Invoice #1234

Hi [Customer],

Our records show Invoice #1234 (dated Jan 5, for $2,500) is now 7 days past the due date of Jan 12.

If you've already sent payment, thank you—please disregard this note.

If you have questions about the invoice or need a payment arrangement, let me know. 
We can also accept payment by:
- ACH / Bank transfer
- Credit card
- Check (if preferred)

Payment details: [your payment instructions]

Thanks,
[Your Name]
```

**2nd Notice (Escalated)**
```
Subject: URGENT: Payment Due - Invoice #1234

Hi [Customer],

Invoice #1234 is now 20 days overdue. This invoice was due on Jan 12 and hasn't been paid or negotiated.

To avoid service interruption or credit holds, please process payment today:
- [Bank transfer details]
- [Credit card payment link]
- [Check payment address]

If this invoice is in dispute, contact me immediately at [phone] so we can resolve it.

Thanks,
[Your Name]
```

**3rd Notice (Final Warning)**
```
Subject: FINAL NOTICE - Payment Required - Invoice #1234

[Customer Name],

Invoice #1234 is 35+ days overdue. Despite previous reminders, this remains unpaid.

Payment is required within 3 days to avoid:
- Service suspension
- Credit hold on future orders
- Transfer to collections

To arrange payment or discuss this issue, contact me immediately:
[Your Phone] / [Your Email]

[Your Name]
```

**You can:**
- ✅ Approve as-is
- ✏️ Edit tone, wording, or add personal details
- 🚫 Skip (don't send to this customer)
- 📞 Mark for manual follow-up (you'll call instead)

### Step 4: Send & Track
Claude sends approved emails and logs each one in QB:
- Email record attached to invoice
- Date/time recorded
- Customer status updated to "Reminder Sent"

### Step 5: Monitor Responses
If QB is connected to your email:
- Claude flags customer responses
- Alerts you if payment is committed or disputed
- Updates invoice status as payments clear

## Output

After running Invoice Chasing, you get:

1. **Sent Reminders Summary** — List of customers contacted, amounts, and dates
2. **QB Audit Trail** — All emails logged to invoice records
3. **Follow-Up Report** — Customers who need manual follow-up or escalation
4. **Collections Dashboard** — Real-time status of all outstanding invoices

## Troubleshooting

### "QB Connection Lost"
- Verify QB is still authorized in Claude settings
- Re-authorize if needed: Settings → Connected Apps → QB → Reauthorize
- Check QB account status (not suspended or demo mode)

### "Some Invoices Not Showing"
- QB may not be fully synced
- Invoices marked as "Draft" or "Paid" won't appear (expected)
- Check QB directly if you think an invoice is missing

### "Email Bounced"
- Claude will flag invalid email addresses
- You can update customer contact info in QB
- Re-run Invoice Chasing to resend to corrected address

### "Customer Complained About Tone"
- You can customize email templates
- Ask Claude to adjust tone (more/less formal, friendly, firm, etc.)
- Create custom templates for VIP customers if needed

## Best Practices

1. **Customize for your relationship** — Aggressive for strangers, friendly for long-term customers
2. **Don't spam** — Respect the 3-notice progression; manual follow-up after that
3. **Track results** — Note which approach works best with different customer segments
4. **Coordinate with sales** — Sales team should know about payment issues with customers
5. **Update QB religiously** — Incorrect invoice status defeats automation

## Advanced Features

### Customer Segmentation
- **New Customers:** Friendly early reminders (due date + 10 days)
- **Long-Term Customers:** Skip 1st notice, start at 2nd (due date + 20 days)
- **Chronic Late Payers:** Require pre-approval/deposits on future orders
- **High-Value Customers:** Manual follow-up instead of automated emails

### Automated Collections
- Set threshold: "Emails only for invoices < $5,000"
- Personal calls for invoices > $5,000
- Escalate to attorney/collections for invoices > 60+ days overdue

### Payment Incentives
- Offer 2% discount if paid in 5 days
- Offer payment plan: 50% now, 50% in 30 days
- Include in reminder emails for quick resolution

## Integration with Other Skills

- **Payroll Planning:** Identifies priority collection targets for cash flow forecast
- **Month-End Close:** Ensures all invoices are accounted for before close
- **Expense Tracking:** Reconciles customer payments against QB

## Related Resources

- [QB Invoice Setup Guide](../docs/integration-guide.md#quickbooks-invoicing)
- [Invoice Tracker Template](../templates/invoice-tracker.xlsx)
- [Payment Terms Best Practices](../docs/faq.md#payment-terms)

---

**Last Updated:** 2026-09-27  
**Maintained By:** Eric Boulou
