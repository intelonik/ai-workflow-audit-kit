# Example: Support Ticket Triage

## 1. Workflow name

Support ticket triage.

---

## 2. Business context

The support team receives customer tickets through email and helpdesk software.

A support manager manually reviews new tickets, decides priority, assigns the right owner, and writes a short internal summary.

The process is straightforward but repetitive. It slows down response time and creates inconsistent ticket quality.

---

## 3. Current trigger

A new customer support ticket is created.

---

## 4. Current tools

- Helpdesk system
- Gmail
- Slack
- Jira or Linear
- Internal admin panel
- Customer database

---

## 5. Current human steps

1. Support manager opens the new ticket.
2. Reads the customer message.
3. Checks the customer account.
4. Checks whether the customer is paid, trial, or enterprise.
5. Decides urgency.
6. Decides which team should handle it.
7. Writes an internal summary.
8. Assigns the ticket.
9. Sends a Slack message if the issue looks urgent.

---

## 6. Decision points

The support manager decides:

- Is this urgent?
- Is this a bug, billing issue, product question, or account issue?
- Which team should handle it?
- Should this be escalated?
- Does the customer need a fast response?
- Is more information needed from the customer?

---

## 7. Input data

Useful data for the workflow:

- ticket subject
- ticket message
- customer email
- customer plan
- customer account status
- previous tickets
- product area
- known incidents
- internal escalation rules

---

## 8. Output

The workflow should produce:

- ticket category
- urgency level
- suggested owner/team
- short internal summary
- suggested next action
- escalation recommendation
- optional draft reply

Example output:

```json
{
  "category": "Billing",
  "urgency": "Medium",
  "suggested_team": "Finance Support",
  "summary": "Customer was charged twice after upgrading their plan.",
  "next_action": "Check Stripe payment history and confirm whether duplicate charge exists.",
  "escalate": false
}
```

---

## 9. Risk level

Medium.

The AI should not directly reply to the customer or change billing data automatically.

It can safely prepare classification, summary, and suggested next action, but a human should approve the final decision.

---

## 10. AI fit

Good AI candidate.

Reason:

The workflow is repetitive, text-heavy, and depends on classification and summarization. AI can reduce manual reading and improve consistency.

---

## 11. Best automation type

Best fit:

- AI classifier
- AI summarizer
- AI assistant with human approval

Not needed for the first version:

- fully autonomous AI agent
- complex multistep automation
- automatic customer replies

---

## 12. Human approval

Human approval should happen before:

- replying to customer
- escalating ticket
- updating billing data
- changing subscription data
- closing ticket

The first version should only suggest actions.

---

## 13. Business value

Main value:

- faster first response
- less manual sorting
- better ticket summaries
- more consistent escalation
- reduced support manager workload

Example estimate:

If the team receives 100 tickets per week and triage takes 3 minutes per ticket, that is around 5 hours per week of manual work.

If AI reduces this by 50%, the team saves around 2.5 hours per week and improves response speed.

---

## 14. First prototype

Build a small prototype that accepts ticket text and returns:

- category
- urgency
- suggested team
- internal summary
- suggested next action

The prototype can be tested with 20–50 historical tickets.

Success criteria:

- category is correct in at least 80% of cases
- urgency is useful in at least 80% of cases
- summary saves time for the support manager
- no customer-facing action happens without approval

---

## 15. Production requirements

To make this production-ready:

- connect to helpdesk API
- add authentication
- store AI output
- add human approval UI
- log all AI suggestions
- allow manual correction
- monitor wrong classifications
- keep prompt/version history
- define fallback behavior if AI fails
- avoid sending sensitive data to unsupported tools

---

## 16. Next action

Take 20 historical support tickets and manually fill this table:

| Ticket | Human category | Human urgency | AI category | AI urgency | Useful? |
|---|---|---|---|---|---|
| #1 | Billing | Medium | Billing | Medium | Yes |
| #2 | Bug | High | Product Question | Medium | No |

Then compare the result and decide whether the prototype is worth building.