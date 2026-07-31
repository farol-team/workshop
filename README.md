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

| | |
|---|---|
| [**WorkRoom**](https://github.com/farol-team/workroom) | A shared workspace where every person brings their own local agent, and the room remembers. |
| [**agent-flow**](https://github.com/farol-team/agent-flow) | Board-driven multi-agent development workflow for Claude Code — human-approved plans, an adversarial test critic, evidence-gated acceptance, compounding project memory. Used in production on our own repos. |

We also keep two curated maps of the space:
[awesome-agent-services](https://github.com/farol-team/awesome-agent-services)
and
[awesome-agentic-web](https://github.com/farol-team/awesome-agentic-web).

## On GNAP and GNAL

[GNAP](https://github.com/farol-team/gnap) — Git-Native Agent Protocol — was
our exploration of coordinating agent teams over git with zero servers. It
remains **research**, and GNAL with it. WorkRoom is built on server
architecture instead; the reasoning is that shared memory with real identity,
permissions, and audit is a database problem before it is a protocol problem.

If you arrived here from GNAP: it is not abandoned, but it is not the bet.

## What will live here

- **Constitution** — the articles we do not violate, in a form where a
  reviewer can check an artifact against them. Not published yet: an article
  is a promise, and we are resolving two conflicts in the draft before making
  promises in public.
- **Kits** — the mechanism half of how we work, starting with the business
  counterpart to `agent-flow`.
- **Skills** — reusable capabilities, the way `agent-flow` packages them.
- **Design notes** — why each mechanism exists, and which failure earned it.

Status: this repository is new and mostly empty. It fills up as things
stabilize enough to be worth someone else's time.

## License

MIT, unless a subdirectory says otherwise.
