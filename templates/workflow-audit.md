# AI Workflow Audit Template

Use this template to review one workflow and decide whether AI-assisted automation is worth building.

## 1. Workflow name

Example:

Refund approval, invoice review, support ticket triage, customer onboarding, lead qualification.

---

## 2. Business context

What team owns this workflow?

It affects who?

Why does this workflow matter?

---

## 3. Current trigger

What starts the workflow?

Examples:

- new email arrives
- customer submits a form
- payment fails
- a support ticket is created
- a new order is placed
- document is uploaded
- an internal request is submitted

---

## 4. Current tools

List every system touched during the workflow.

Examples:

- Gmail
- Slack
- Google Sheets
- Notion
- Airtable
- HubSpot
- Shopify
- Stripe
- Jira
- Linear
- internal admin panel
- database
- custom API

---

## 5. Current human steps

Write the manual process step by step.

Example:

1. Support manager opens the ticket.
2. Reads the message.
3. Checks customer account.
4. Decides urgency.
5. Assigns the ticket to the right person.
6. Writes an internal summary.
7. Sends a Slack notification.

---

## 6. Decision points

Where does a person inspect, classify, approve, reject, summarize, or route something?

Examples:

- Is this urgent?
- Which team should handle it?
- Is the customer eligible?
- Is the document valid?
- Is the payment suspicious?
- Should this be escalated?
- What should be the next action?

---

## 7. Input data

What data is needed to make the decision?

Examples:

- customer message
- order history
- payment status
- subscription plan
- uploaded document
- previous support tickets
- CRM notes
- internal policy
- product category
- country / market

---

## 8. Output

What should the workflow produce?

Examples:

- classification
- summary
- recommendation
- draft reply
- ticket assignment
- status update
- risk score
- extracted data
- approval request
- notification

---

## 9. Risk level

Choose one:

- Low
- Medium
- High

Explain why.

Low-risk example:

AI creates a summary that a human reviews.

Medium risk example:

AI suggests an action, but human approval is required.

High risk example:

AI makes a customer-facing or financial decision without review.

---

## 10. AI fit

Choose one:

- Good AI candidate
- Possible AI candidate
- Better solved with traditional automation
- Not worth automating now

Explain your choice.

---

## 11. Best automation type

Choose one or more:

- AI classifier
- AI summarizer
- AI data extractor
- AI assistant
- AI agent with human approval
- rules-based automation
- API integration
- dashboard / reporting automation
- not worth automating

---

## 12. Human approval

Where should a human stay in the loop?

Examples:

- before sending customer response
- before issuing refund
- before updating CRM
- before assigning high-priority status
- before changing payment or subscription data

---

## 13. Business value

Choose the main value:

- saves time
- reduces errors
- improves response speed
- improves reporting
- improves customer experience
- reduces support load
- improves compliance
- unlocks a new workflow

Add rough estimate if possible.

Example:

This workflow happens 80 times per week and takes 5 minutes each time.  
Estimated manual time: around 6–7 hours per week.

---

## 14. First prototype

What can be prototyped in 1–3 days?

Example:

Build a small internal tool that accepts a support ticket text, classifies urgency, suggests owner, and generates an internal summary.

---

## 15. Production requirements

What would be needed to make it production-ready?

Examples:

- authentication
- logging
- error handling
- human approval UI
- API integration
- monitoring
- audit trail
- prompt/version control
- fallback behavior
- data privacy review

---

## 16. Next action

What is the smallest useful next step?

Example:

Test the workflow on 20 real historical tickets and compare AI classification with human decisions.