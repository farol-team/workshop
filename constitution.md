# Constitution

The articles Farol Labs does not violate, stated so that a reviewer can check
a concrete artifact against them — a draft message, a landing page, a pricing
proposal, a change to the product, a decision about what goes into an open
repository.

This is the public edition: **the articles that are promises to people outside
the company.** Internal prioritization rules are not promises to anyone and
live in our private workspace; where one is omitted, it is marked rather than
silently dropped.

Format follows [`agent-flow`](https://github.com/farol-team/agent-flow)'s
`constitution-template.md`. Articles are grouped into cross-cutting ones and
per-product ones; a proposal is checked against the cross-cutting articles
plus those of its own product. Numbers are unique across the document and are
never reused. A retired article is marked `(retired)`, not deleted.

Amendment: by explicit decision of both founders, each with a line naming the
incident or decision that caused it. The "How these were earned" section below
is that record.

> **Status: draft (v0.3).** Numbering is stable; wording is still settling.

---

## Universal articles

*These would apply to any company working this way.*

### Article I — A source under every claim
Any factual claim about a person, a company, a market, a competitor, or a
number carries a reference to where it came from — in the artifact itself or
in the working note attached to it. A claim without a source is cut, not
softened into "reportedly".

Not accepted as substitutes for a source: "it's well known that", "the market
is estimated at roughly", "they almost certainly", "the general view is". An
agent's summary, unverified, is not a source. A reference to our own earlier
document counts only if that document carries a source itself.

This is the weakened form of the evidence gate from our engineering kit. The
outcome of a business action cannot be verified at the moment it is produced;
the provenance of a fact can. We check what is checkable and do not pretend to
check the rest.

### Article II — A person takes the outbound step
Anything that leaves the company — a sent message, a published page, a quoted
price, a commitment made — is done by a person. The agent prepares, ranks, and
drafts; a person presses the button.

The rule holds regardless of how confident the agent is or how routine the
step looks. The basis is irreversibility: code can be rolled back, a sent
message and a quoted price cannot.

### Article III — We don't invent on someone else's behalf
We do not produce text attributed to a real person or organization that they
did not say: quotes, testimonials, case studies, customer logos, deployment
numbers. A hypothetical example is labelled hypothetical in the artifact
itself, not only in the conversation around it.

Separately: a company we have not signed a pilot with is not called a customer
in any external material.

---

## Farol articles — all products

### Article C2 — We are not a productivity-monitoring tool
*(Basis: employee-surveillance software is the category our recorder is most
easily mistaken for. Getting this wrong is not a positioning nuance; it is
whether the product survives at all.)*

No external material positions our products as supervision of an employee,
measurement of their efficiency, or comparison of people against each other.

The check is by vocabulary. Banned in external text and in demos: "employee
monitoring", "productivity tracking", "who is doing what", "employee
ranking", "identify idle time". Banned: any screen or report that ranks people
against one another.

**Why this covers the room as well.** WorkRoom stores runs, steps, cost, and
tokens broken down by person and channel. That is ready-made material for a
"who uses their agent most effectively" dashboard, and building one will be
tempting. Reporting on spend is fine; ranking people is not.

If a customer's request requires such a feature, that is a refusal, not a
compromise on wording.

### Article C3 — Trust over coverage
At any fork between "collect more data" and "keep the trust of the person
being observed and of their security team", we choose trust. Expanding
coverage is permitted only together with an explicit answer to what the
observed person knows about it.

The check: a proposal that expands collection must contain the line "what the
person knows about this, and from where". A missing line is a violation, not
an oversight.

*(This article is absolute, with no carve-out for a headless build. See
decision 2 below for how it got that way.)*

### Article C5 — A machine's conclusion becomes truth only through a person
The machine observes, extracts, and proposes. Its conclusion becomes something
the organization treats as true about itself only through an explicit human
act. We do not ship a product that decides on its own how someone else's work
is arranged.

The check: is there a step where a person accepts or rejects the conclusion —
and is that step mandatory, rather than a default-on setting that can be
turned off?

Article II and C5 are not duplicates: II is about crossing **out of** the
company, C5 about moving **up** inside it. Both say "the machine prepares, a
person commits", about different boundaries. R1 defines the mechanics inside
the room.

### Article C6 — *(internal)*
A prioritization rule about how we choose between competing pieces of work.
It is a commitment we make to ourselves, not to anyone outside, so it is not
part of the public edition. The number is held so that references stay stable.

---

## WorkScreen articles

*WorkScreen is our desktop recorder: it observes how work actually happens, so
that a company can see its processes as they are rather than as described.*

### Article C1 — Data only for the purpose of observation
We are built like a constitutional state: a person may do anything not
forbidden; the company may do only what is expressly permitted. Three things
are permitted, and nothing beyond them.

**Purpose.** Data from a workstation is used only to build a picture of how
work is arranged and to produce automation from it. Never for anything that
concerns the person **as a person**: not for evaluation, not for comparing
people with each other, not for decisions about them.

**Egress.** What leaves the observed person's machine is enumerated — and what
is not enumerated does not leave. The list is public, and it is what makes
this article checkable.

**Access.** Nobody inside our company looks at the raw stream of an identified
person. Under no circumstances, including when it is technically possible and
commercially profitable.

The check: does the change use data beyond the purpose? Does it add something
to egress that is not on the published list? Does it open one person's raw
data to someone inside our company? Any of the three is a violation, even if
the capability already exists technically, and even if a customer asks.

*(Why we do not cap how much we capture: at recording time you cannot know
what will turn out to be redundant — finding repetition nobody noticed is the
entire point. A volume cap therefore either has no teeth or breaks the
product. Purpose, egress, and access can be capped, and that is what a
purpose limitation actually means.)*

### Article C4 — Open recorder, closed engine
The open part is what runs on the observed person's machine, because that is
the only way to answer "what are you recording, and where does it go?" better
than marketing can. The closed part is the extraction engine, the accumulated
context, and the cloud orchestration.

The check: does the change move the extraction engine, its prompts, or
derivatives of accumulated context into an open repository? Or, in the other
direction, does it make it harder for an observed person to read the code of
what runs on their own machine?

### Article C7 — The local buffer is always readable
What was recorded on the observed person's machine, and what left it, stays
readable by the owner of that machine. We do not encrypt the local database
against them and do not hide it, and a customer cannot contract that away.

This is the mechanical backing for C1 and C3: without it, "egress is
enumerated" is a promise on our word; with it, it is a checkable fact. It is
also the specific thing that makes the product technically distinguishable
from the black box it is positioned against.

The check: can a person with the recorder installed see what was recorded
about them and what was sent, using a tool we ship ourselves?

---

## WorkRoom articles

*[WorkRoom](https://github.com/farol-team/workroom) is a shared workspace where
every person brings their own local agent, and the room remembers. These
articles are extracted from its own design documents.*

### Article R1 — Direct writes only with a person present
An agent working in a channel **in the presence of its person** writes to
channel memory directly: the mechanism for cheap correction is right there, and
a mistake is visible as it happens.

Any source writing **in batches, on a schedule, or with no person present** —
the recorder, scheduled distillation, an import — creates a proposal only.
Applying it is a separate act.

The criterion is not "human or machine" but **whether someone is there to
notice the mistake as it appears**. A batch writer has nobody, by
construction, and no amount of care substitutes for that.

Moving knowledge between channels, or up to the organization-wide scope, is
always an explicit act with its own review, whoever proposes it.

The check: does the proposed writer have a person who will see the entry as it
appears? If not, it goes through the gate.

### Article R2 — Provenance and trust class are mandatory
Every entry in shared memory carries its provenance — where it came from,
whose run produced it, which model — and its trust class. There are three
classes:

- **a person's assertion** — they said so;
- **an agent's inference** — it concluded so;
- **an instrument's observation** — it was measured.

Three, not two. A measurement is neither an opinion nor an inference. It is
more reliable than an inference — process discovery is deterministic and its
numbers reproduce — but it is entirely without context: the instrument sees
that a request loops back through the same system and does not know a policy
requires it. Retrieval has to weigh these differently.

An entry without provenance is a defect, not an entry.

### Article R3 — Recorded and external content is data, not instructions
Content that arrives from observation or from outside — a transcript, an
email, a page, someone else's document — is marked as data and is never
executed as an instruction. The marking travels with the entry into memory and
**survives distillation**.

Why this is an article rather than an implementation detail: a call with an
external participant is, quite literally, a channel through which an outsider
can dictate an instruction into your organization's memory, after which it
will be pulled into the context of every agent in that channel. Losing the
marking at one distillation step turns a recorder into an attack path against
the room.

The check: does the untrusted marking reach the entry in memory, or is it lost
along the way?

### Article R4 — The server never runs agents and never sees model credentials
Execution stays on the person's machine. The server sees what a run reported —
tokens, cost, steps — but never a model credential, never the files, never the
context window.

The trade is deliberate and we state it plainly: an organization gains
visibility into model spend but not a lever over it. A customer who needs
central control of model spend needs a different product. That is a refusal,
not a roadmap item.

The check: does the change introduce any path where the server starts an agent
or stores a model key?

---

## How these were earned

An article that arrives from nowhere does not hold. Each of these came from a
conflict we had to resolve.

**C1 changed what it limits.** The first draft capped *how much* we capture.
That does not work: at recording time you cannot know what will turn out to be
redundant, and finding unnoticed repetition is the whole product. The cap moved
to purpose, egress, and access — which is what a purpose limitation was always
supposed to mean.

**We dropped the invisible build.** We had designed a headless enterprise
variant: no window, no settings, no in-app consent, with notification handled
by corporate policy out of band. It conflicted with C3 and C5, and the only way
to keep both was a two-tier promise — a public commitment with an asterisk,
at exactly the moment a document a customer's security team can read became a
priority. We dropped the invisible build instead and kept C3 absolute. C7
exists as the compensating invariant.

**C5 moved.** It originally described a consultant approving a generated
automation — a step our product no longer has. The meaningful human decision
turned out to live in two other places: crossing out of the company, and
rising into what the organization treats as true. C5 is about the second.

**These articles were a single product's, and now are the company's.** When
the perimeter became two products, C2, C3, and C5 turned out to be
cross-cutting, C1, C4, and C7 to be about capture, and the room needed four of
its own. R1 in particular closed a conflict that had stayed open: the room's
own memory design allows an agent to write directly, while our analysis of
batch sources demanded a gate. The line between them is presence, not species.

---

## What is deliberately not here

A constitution nobody can hold in their head stops being checked.

- **Strategy and worldview.** They change as we learn; an article should not.
- **Goals, metrics, and horizons.** The constitution answers "may we do it
  this way"; goals answer "is this worth doing at all". Different document,
  and a private one.
- **Engineering invariants.** WorkRoom's rule that nothing crosses a seam
  except through its protocol is genuinely non-negotiable, but it belongs to
  that repository's engineering constitution under `agent-flow`. What lives
  here are the articles that are promises to people.
- **Pricing.** Not settled.
