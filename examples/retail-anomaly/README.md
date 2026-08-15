# Retail Anomaly — 8-team backlog examples

This is a set of adapted backlog examples for the **Context-Aware Multi-Branch Retail Anomaly Intelligence** cohort project (30 students / 8 teams / 9 weeks). Sits alongside the main `ml-product-backlog-template` — each team's directory here is an instance of that template, adapted to the specific team's mission and cross-team dependencies.

## What's here

- **`cross-team-contact-points.xlsx`** — the master list of every producer→consumer dependency across teams. Two sheets: "Cross-team contacts" (40 rows, one per dependency edge) and "Topic map" (9 Kafka topics with producer + consumer teams).
- **`team-1-data-foundation/`** through **`team-8-product-experience-and-ops/`** — per-team card sets. Each contains only the epics that actually apply to that team's mission (research teams don't have Corpus because Team 1 owns it; Team 7 has no Modeling because they own no models; etc.).

## What's in each team directory

Only the epics that apply to the team's actual work. A short team README explains the omissions and lists the applicable epics. Under each epic, only the cards with meaningful coordination work — the team lead can (and should) add more intra-team cards as they decompose weekly issues.

## New section in every card: "Cross-team contact points"

Where a card involves other teams (which is often), a dedicated **Cross-team contact points** section appears between "Upstream / Downstream contract" (intra-team) and "Definition of Done." It names the other team(s), the Kafka topic or API contract, the timing, and the risk if late.

This is the value-add over the base template. See `cross-team-contact-points.xlsx` for the complete graph.

## What to do with these

Each team lead should:

1. Copy their team's directory into their own repo (or leave it in a shared location for reference).
2. Adapt the cards further — team-specific details, actual student assignments, real dates.
3. Use the cross-team spreadsheet as a live document — update it as topic schemas evolve or new dependencies emerge.
4. Add more cards (intra-team, week-by-week) as the sprints unfold. These examples cover coordination-heavy work; day-to-day execution cards are the lead's job.

The examples don't cover every possible card — that's not the point. They give leads and students a working reference for what a good card looks like in this project's specific context.
