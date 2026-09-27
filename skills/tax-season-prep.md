# Tax Season Prep Skill

Organizes your year's records ahead of tax time. Gathers invoices, receipts, deductions, and prepares everything your CPA needs for efficient tax preparation.

## What It Does

The Tax Season Prep skill:

1. **Gathers all QB transactions** for the tax year
2. **Organizes by category** (income, expenses, fixed assets, deductions)
3. **Validates that records are complete** (flags missing documentation)
4. **Identifies potential deductions** you may have missed
5. **Exports tax prep folder** organized for your CPA
6. **Creates missing items checklist** so you can gather before CPA meeting

## When to Use

- **October-November:** Start organizing (before busy year-end)
- **December 15:** Final prep review (before CPA engagement)
- **January (for prior year):** Final catch-up before filing deadline

## Setup

### Prerequisites
- QuickBooks Online (full year of transactions)
- All receipts organized or scanned (or receipt photos)
- Claude for Small Business enabled
- List of fixed assets purchased during year (vehicles, equipment, etc.)

### Configuration Steps

1. **In Claude Cowork**, toggle "Claude for Small Business" on
2. **Authorize QB connection**
3. **Select "Tax Season Prep"** skill
4. **Configure tax details:**
   - Tax year (e.g., 2026)
   - Business structure (sole prop, S-corp, C-corp, LLC)
   - CPA name and email (optional; for export)
5. **Set deduction tracking:**
   - Home office? (calculate % deduction)
   - Vehicle for business? (track mileage)
   - Estimated tax payments made? (for credits)
6. **Identify fixed assets:** Property, vehicles, equipment purchased during year

## Usage

### Quick Start
```
Open Claude Cowork
→ Claude for Small Business
→ Tax Season Prep
→ "Start"
```

### Step 1: QB Data Extraction
Claude pulls your full QB data for tax year:
- All income/revenue accounts
- All expense accounts
- Fixed asset purchases
- Loan/liability changes
- Equity account movements

### Step 2: Organize by Category
Claude organizes into tax-preparation buckets:

**Income**
- Sales/Revenue
- Service Income
- Other Income (interest, rental, etc.)

**Deductible Expenses**
- Rent/Lease
- Payroll (wages, contractor payments, taxes)
- Supplies & Materials
- Utilities
- Professional Services (accounting, legal)
- Marketing & Advertising
- Insurance
- Depreciation

**Non-Deductible/Personal**
- Personal expenses (flagged for removal)
- Loan principal (not deductible)
- Distributions/draws (not deductible)

**Fixed Assets** (for depreciation)
- Equipment purchases
- Vehicles
- Leasehold improvements

### Step 3: Validate Completeness
Claude checks for:
- ✅ **Missing documentation:** Expenses with no supporting receipt
- ✅ **Large unusual transactions:** Anything > $500 with no description
- ✅ **Personal expenses:** Items that shouldn't be deducted
- ✅ **Tax payments made:** Estimated taxes, payroll taxes, sales tax
- ✅ **Quarterly data:** Ensure all quarters represented

**Example issues Claude finds:**
```
⚠️ Missing Receipt: 
   12/15/2026 - Staples - $156.42
   No receipt attached. Recommend re-locating or noting description.

⚠️ Personal Expense Possible:
   03/22/2026 - Gas station - $65
   Only one transaction at this vendor. Confirm business use.

⚠️ Large Transaction No Description:
   07/18/2026 - Electronics Warehouse - $2,847.50
   No description. What was purchased? (Equipment = depreciable asset)

✅ Quarterly Data: All quarters present
   Q1: $0 entries, Q2: $0 entries, Q3: $0 entries, Q4: $0 entries
```

### Step 4: Identify Deductions
Claude reviews and flags deductions you might have missed:

**Potential Deductions:**
```
✓ Home Office Deduction
  Eligible: 500 sq ft home office / 2,500 sq ft total = 20%
  Deductible: Rent, utilities, insurance, depreciation (20% of each)
  Estimated value: $12,000/year
  
✓ Vehicle Mileage
  Required: Mileage log or reasonable reconstruction
  Rate: $0.67/mile (2026 rate)
  Claimed: 8,400 business miles recorded
  Deduction: $5,628
  
✓ Health Insurance Premium
  You paid $8,400 in health insurance
  Eligible as self-employed deduction
  Deduction: $8,400
  
✓ Estimated Tax Payments
  Q1: $5,000, Q2: $5,000, Q3: $5,000, Q4: $6,000 = $21,000 paid
  Credits for: $21,000
```

### Step 5: Export Tax Prep Folder
Claude organizes and exports to folder structure:

```
Tax_Prep_2026/
├── 1_Summary/
│   ├── Tax_Summary.pdf          # P&L, income, major deductions
│   ├── Estimated_Liability.pdf  # CPA's estimate of tax owed
│   └── Missing_Items_List.txt   # What you still need to provide
├── 2_Income/
│   ├── Sales_Revenue.csv        # By month, by customer
│   ├── Service_Revenue.csv
│   └── Other_Income.csv
├── 3_Expenses/
│   ├── Payroll.csv              # W2s, 1099s, payroll taxes
│   ├── Rent_Lease.csv
│   ├── Professional_Services.csv
│   ├── Supplies.csv
│   └── [all expense categories]
├── 4_Fixed_Assets/
│   ├── Equipment_Purchased.csv  # Date, description, cost
│   ├── Vehicles.csv
│   └── Depreciation_Schedule.csv
├── 5_Deductions/
│   ├── Home_Office.pdf          # Calculation worksheet
│   ├── Vehicle_Mileage.pdf      # Mileage log and calculation
│   ├── Health_Insurance.pdf
│   └── Self_Employment_Tax.pdf
└── 6_Receipts/
    ├── by_category/
    │   ├── Payroll/
    │   ├── Professional_Services/
    │   └── ...
    └── by_month/
        ├── January_2026/
        ├── February_2026/
        └── ...
```

### Step 6: Missing Items Checklist
Claude generates checklist of items you still need:

```
TAX PREP CHECKLIST - 2026

Items to Gather:
☐ Home office documentation (room dimensions, business use %)
☐ Vehicle purchase receipt (1040 Schedule C, Line 27)
☐ Estimated tax payment confirmations (Q1-Q4)
☐ Charitable donation receipts (> $250 each)
☐ Business travel expenses summary
☐ Health insurance premium statements
☐ Equipment depreciation schedules
☐ 1099s from vendors (if subcontractors paid > $600)
☐ Loan documents (debt interest deductible)

Questions for CPA:
? Should S-corp make 2953 election for tax treatment?
? Multi-member LLC or single-member for liability?
? Estimated tax payments sufficient, or will we owe?
? Home office deduction advisable, or too aggressive?

Optional Deductions to Discuss:
- Quarterly subscriptions ($0/month × 12 = $0/year) - depreciable?
- Meals & entertainment (new rules: 100% meals with clients)
- Office redecorating ($0) - asset or expense?
```

### Step 7: CPA Hand-Off
Claude prepares export for your CPA:

**You can:**
1. ✅ Review export in Claude
2. ✏️ Add notes or corrections
3. 📧 Email tax prep folder directly to CPA
4. 📥 Create password-protected link to folder

Claude can auto-email to CPA with cover letter:
```
Subject: 2026 Tax Preparation File - [Your Name]

Dear [CPA Name],

Attached is the complete 2026 tax preparation file for [Business Name].

Organization:
- Folder 1: Summary of income and major deductions
- Folder 2-5: Detailed transactions by category
- Folder 6: Supporting receipts and documentation

Missing items: See attached checklist. I'll send these separately as gathered.

Questions for our meeting: See notes in Summary folder.

Ready to meet on [date] at [time].

Thanks,
[Your Name]
```

## Output

After completing Tax Season Prep:

1. **Tax Prep Folder** — Organized with all income, expenses, deductions, receipts
2. **Missing Items Checklist** — What you still need to gather
3. **Tax Summary** — Your estimate of tax owed/due
4. **P&L Detail** — Business profit calculation for filing
5. **Deduction Analysis** — Identified deductions with calculations
6. **CPA Cover Letter** — Ready to send with folder

## Troubleshooting

### "QB Data is Incomplete"
- Some transactions missing from QB
- Action: Add missing transactions to QB before export
- Or: Provide detail to Claude (receipts, invoices, statements)

### "Some Receipts Are Digital Only"
- You have email receipts but not photos
- Action: Forward to Claude or save to folder
- Claude will organize them in tax prep folder

### "I Don't Know If Expense is Deductible"
- Create note in QB with the question
- Claude will flag for CPA review
- CPA can advise during tax prep

### "Estimated Liability Seems High"
- Common: You forgot to account for tax payments already made
- Check: Are estimated tax payments included?
- Ask: Does this include self-employment tax?
- Review with CPA before filing

## Best Practices

1. **Start early** — October is ideal; don't wait until January
2. **Keep digital receipts** — Scan or photo paper receipts throughout year
3. **Categorize accurately** — Spend 10 minutes/week cleaning QB
4. **Track deductions** — Mileage log, charitable donations, etc.
5. **Communicate with CPA** — Review tax prep folder before filing
6. **Plan for next year** — Use this year's prep to improve next year's tracking

## Advanced Features

### Estimated Tax Planning
Claude can forecast next year's taxes based on this year:
- If you made more: estimated payments will increase
- If business grew: plan for higher quarterly payments
- If you took deductions: forecast impact on next year's liability

### Entity Structure Review
If you're considering S-corp or LLC election:
- Claude shows income thresholds where entity change makes sense
- Estimated tax savings from structure change
- Note: Work with CPA for final recommendation

### Multi-Year Comparison
Track year-over-year:
- Revenue growth/decline
- Expense trends
- Tax liability changes
- Deduction patterns

## Integration with Other Skills

- **Month-End Close:** Ongoing close ensures clean year-end data
- **Expense Tracking:** Categorized expenses feed into tax prep
- **Payroll Planning:** Payroll records and tax payments included
- **Invoice Chasing:** AR aging and bad debt tracking for tax purposes

## Related Resources

- [IRS Publication 334 (Tax Guide for Small Business)](https://www.irs.gov/publications/p334)
- [Self-Employment Tax Worksheet](https://www.irs.gov/forms-pubs/form-1040-se)
- [Tax Prep Checklist Template](../templates/tax-prep-checklist.md)

---

**Last Updated:** 2026-09-27  
**Maintained By:** Eric Boulou
