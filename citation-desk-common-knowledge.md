# Common knowledge in enterprise IT — citation guardrail

This file calibrates the "does not need a citation" boundary for the Citation Desk project. Its only job is to stop the tool from flagging genuinely common knowledge and burying the real citation gaps in noise. It is not a license to skip a citation that is actually needed. Familiarity of a topic never exempts a claim from sourcing.

## The decisive test

A claim is common knowledge only when all of these hold:
- A knowledgeable peer would accept it without asking "says who?" or "where's that number from?"
- It is broadly known and non-controversial in enterprise IT.
- It is conceptual, definitional, or settled history, not a specific measurement or finding.
- It is not traceable to a single originator whose distinctive wording is being reused.

The instant a claim carries a specific number, a named attribution, a date-specific fact, or anything reasonable practitioners would dispute, it leaves the common-knowledge zone and needs a source. No exceptions for familiar topics.

## Common knowledge: no citation needed

- **Definitions and general purpose of established technologies.** What an API, container, microservice, data lake, SIEM, or CI/CD pipeline is and what it is broadly for.
- **How widely adopted practices generally work, conceptually.** The general shape of agile, version control, a software release pipeline, or incident response.
- **The existence and general identity of major vendors and products.** That AWS, Azure, and Google Cloud are major public cloud providers; that Docker is a containerization tool; that Splunk is an observability and SIEM platform.
- **The existence and general purpose of well-known frameworks and regulations.** That GDPR governs personal data of EU residents, that HIPAA governs US health data, that FedRAMP authorizes cloud services for US federal use.
- **Settled, uncontested tech history.** That the iPhone launched in 2007, that the public web emerged in the early 1990s.
- **Established terms that happen to have a known coiner.** Terms like technical debt and zero trust are now common vocabulary and can be used freely without citing their originator every time. Attribution is only triggered when the originator's distinctive wording or specific original formulation is quoted or closely paraphrased.
- **Non-controversial industry observations not dressed as findings.** That documentation tends to drift out of date as products change, or that security and convenience often trade off.

## Always cite, even on familiar topics

This is the part of the guardrail that protects the tool's integrity. Flag every one of these regardless of how well known the subject is:
- Any statistic, percentage, dollar figure, market size, growth rate, adoption rate, or survey result.
- Any claim attributed to a named analyst, study, report, vendor, or person.
- Any specific factual claim about what a named company or product did, launched, priced, or announced, especially anything tied to a date.
- Any current-state claim: who leads a market, the latest version, current pricing, the present threat landscape. These change and must be sourced.
- Any specific capability, benchmark, or performance claim about a technology.
- Specific regulatory requirements, thresholds, deadlines, or penalty amounts.
- Any contested assertion or opinion stated as fact, where reasonable practitioners would disagree.
- Any distinctive framework, term, or framing originated by an identifiable author, which is the close-paraphrase and plagiarism lane.

## Contrastive pairs

Use these to locate the line.

- "An API lets two systems exchange data." Common knowledge. // "Stripe's API handles a given request volume per second." Cite.
- "Zero trust assumes no implicit trust inside the network." Common knowledge. // "Zero trust adoption reached a given percentage last year." Cite.
- "AWS, Azure, and Google Cloud are major public cloud providers." Common knowledge. // "One of them holds the largest market share." Cite, because that is a ranking claim.
- "GDPR governs personal data of EU residents." Common knowledge. // "GDPR penalties can reach 4% of global annual revenue." Cite, because that is a specific regulatory threshold.
- "Containers package an application with its dependencies." Common knowledge. // "Container adoption grew by a given amount year over year." Cite.
- "Documentation drifts out of date as products change." Common knowledge. // "Outdated documentation costs enterprises a given dollar amount annually." Cite.
- "Technical debt is the cost of choosing an easy fix now over a better solution later." Common knowledge as established vocabulary. // Quoting Ward Cunningham's original metaphor word for word. Attribute.

## When in doubt, flag it

If a call is genuinely ambiguous, treat the claim as needing a citation. An unneeded flag costs Will a few seconds to dismiss. A missed citation is the exact accountability failure this tool exists to catch. Bias toward sourcing.
