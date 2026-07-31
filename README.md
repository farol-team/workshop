# Workshop

How Farol Labs works: the constitution we hold ourselves to, the kits we use,
and the reasoning behind them.

This is the mechanism, not the content. Our own goals, numbers, and
commercial reasoning live elsewhere and stay private — the same split we
already use in [`agent-flow`](https://github.com/farol-team/agent-flow),
where the kit is shared and each project's constitution belongs to that
project.

## The bet

Teams working with agents need durable shared context more than they need
better agents.

Agents improve every few months, and people have preferences. What does not
improve on its own is what an organization knows about itself: how its work
actually happens, and what it has already learned and paid for. Bind a
workspace to one agent and you rebuild when the landscape moves. Bind it to
the context, and it outlives any particular agent.

Everything here follows from that.

## What we build

Two products, two halves of the same idea.

| | |
|---|---|
| **WorkScreen** | Desktop software that records how work actually happens — screen, actions, meetings — so a company can see its processes as they are rather than as described. |
| [**WorkRoom**](https://github.com/farol-team/workroom) | A shared workspace where every person brings their own local agent, and the room remembers. |

An organization loses what it knows twice over. It never had an honest picture
of how its work is actually done: ask people and you get what they believe they
do, put a consultant at their shoulder and it is accurate but does not scale.
And whatever it does learn evaporates — every agent session starts from zero,
and the same ground gets bought again next quarter.

WorkScreen is about the first loss, WorkRoom about the second. One observes,
the other remembers. Neither is interesting without the other: a picture nobody
keeps is a report, and a memory with nothing honest in it is a wiki.

The recorder is open source, because that is the only real answer to "what are
you recording, and where does it go" — see articles C1, C4, and C7 of the
[constitution](constitution.md). It is currently published under its earlier
name, [`gilb-recorder`](https://github.com/gilb-ai/gilb-recorder).

### Tools we built for ourselves

[**agent-flow**](https://github.com/farol-team/agent-flow) — board-driven
multi-agent development workflow for Claude Code: human-approved plans, an
adversarial test critic, evidence-gated acceptance, compounding project
memory. Extracted from our own repos and used in production on them.

We also keep two curated maps of the space:
[awesome-agent-services](https://github.com/farol-team/awesome-agent-services)
and
[awesome-agentic-web](https://github.com/farol-team/awesome-agentic-web).

## What will live here

- [**Constitution**](constitution.md) — the articles we do not violate, in a
  form where a reviewer can check an artifact against them. Includes what the
  recorder may and may not do with what it sees, and what may be written into
  a room's shared memory.
- **Kits** — the mechanism half of how we work, starting with the business
  counterpart to `agent-flow`.
- **Skills** — reusable capabilities, the way `agent-flow` packages them.
- **Design notes** — why each mechanism exists, and which failure earned it.

Status: this repository is new and mostly empty. It fills up as things
stabilize enough to be worth someone else's time.

## License

MIT, unless a subdirectory says otherwise.
