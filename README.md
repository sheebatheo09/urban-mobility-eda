# Urban Mobility Fleet — Exploratory Data Analysis

**Python · SQL · Tableau**

> Operational analysis of an electric car-sharing fleet to uncover 
> inefficiencies and optimise agent dispatch decisions.

---

## Business context

Free-floating electric car-sharing fleets face a core operational tension:
a vehicle charging at a station could either be rented by a customer 
(free, no cost) or sit idle past 100% charge (triggering overstay fees).
Dispatching an agent too early wastes resources. Too late means fees.

This project answers two questions:
1. How efficiently is the fleet being operated — where are the gaps?
2. At what battery level should an agent be dispatched?

---

## Dataset

- 45,000+ rental and charging records across 52 vehicles
- Fields: vehicle ID, rental start/end timestamps, battery levels, 
  mission type (rental vs charging), agent activity logs
- *Data anonymised — company name and identifiable fields removed*

---

## Methodology

- End-to-end data cleaning: duplicates, timestamp conflicts, 
  conflicting mission states
- Operational KPI analysis: utilisation rates, mission type breakdown,
  agent activity patterns
- **Sequential vehicle timeline analysis**: tracked each vehicle's 
  state transitions to model customer rental probability at each 
  battery level

---

## Key findings

| Finding | Detail |
|---------|--------|
| Agent scheduling misalignment | Agents most active 7–10am; peak customer demand is 15–17h |
| Optimal dispatch threshold | **85% battery** — point where rental probability drops to ~50% |
| Overstay risk window | Vehicles left charging beyond 85% show sharply rising fee exposure |

---

## Recommendation

Dispatch agents when battery reaches **85%** — this is the tipping point 
where the cost of waiting (overstay fees) outweighs the benefit of a 
potential customer rental.

---

## Stack

`Python` `Pandas` `SQL` `Tableau` `Jupyter Notebook`


