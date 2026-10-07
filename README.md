# Heist Boss Simulator — One-Page GDD

> **Pitch:** You owe a crime boss money. Pick a heist, hire a crew of randomly generated misfits, plan the job on a timeline, then watch it play out in real time and manage the chaos as it unfolds. FTL-style pause-and-react, RimWorld-style quirks, top-down view.

**Core fantasy / lightbulb moment:** The heist succeeds *despite* the chaos, either because of a thorough plan or because you rolled with the punches.
**References:** FTL (pause and manage chaos), RimWorld (quirks, top-down readability).
**Story:** Minimal. The boss and the debt exist only as pressure.

> Items marked *(proposed)* are recommendations from the design chat that haven't been confirmed. Treat them as tunable.

---

## Core Loop

**Contract → Shop & Hire → Plan → Execute → Payout / Loss → Reputation update → repeat**

A run ends when you have no money left. Runs are independent.

---

## Core Systems

### 1. Run Economy
- Money is your health. Crew fees and shop purchases are paid **up front** as flat fees *(proposed)*.
- **Profit = take − crew cost − shop spend.** A heist isn't pass/fail: you either made money or lost it.
- **$0 means the run is over.**
- **Escalation:** spend more to make more. Bigger investments unlock bigger heists with more crew, more rooms and bigger payouts.
- Boss debt: a fixed total, with a payment due every N heists *(proposed; endless mode is the alternative)*.

### 2. Heist Contract
- **MVP locations:** House, Museum, Bank (in rising difficulty).
- **Robbery Info** is randomized but drawn from each location's own pool of sections (e.g., House: dog, safe, laptops; Museum: lasers, alarms, cameras, guards; Bank: huge safe, gold bars, armed guards).
- Each location type defines a **task template** of abstract tasks (e.g., Bank: Entry → Bypass Security → Breach Vault → Grab Loot → Exit) *(proposed)*.
- **The player plans blind.** Intel and the task template are visible; the map layout isn't.

### 3. Crew
- Roles are offered **randomly** each heist, so the same location can be robbed in different ways depending on who's available.
- Each role slot offers **3 randomly generated prospects** with varying cost, stats and quirks.
- **Roles unlock methods.** Some tasks need a specific role. General tasks can be done by anyone, with a time penalty. (Example: Safe Blaster = fast and loud, Lock Picker = slow and quiet, anyone else = brute force with a penalty.)
- Stats: 3–4 simple ones that affect task speed and success *(proposed: Speed, Stealth, Muscle, Smarts)*.
- Quirks: RimWorld-style traits that interact with rooms and events, both good and bad.
- Crew don't carry over, but the same people can show up for hire again.
- Role pool (draft): Muscle, Hacker, Demolitionist, Tunneler, Contortionist, Master of Disguise, Plant, Lock Picker, Burglar, Decoy, Forger, Arsonist, Lookout, Hypnotist, Gambler, Getaway Driver, Safe Blaster.

### 4. Shop
- Sells the gear, tools and intel the heist calls for (drills, disguises, schematics, etc.). Items unlock methods or reduce penalties.

### 5. Plan Phase
- **One timeline per crew member.** You drag abstract tasks onto the timelines.
- Every crew member needs an **Entry task** and an **Exit task**.
- Task duration depends on role and stats. Tasks can depend on each other (vault after alarm) *(proposed)*.
- The plan timeline uses the same clock as the execution timer.

### 6. Execution Phase
- **Real time with pause.** The location is **procedurally generated** as a top-down room map with crew, NPCs (guards, civilians) and objectives.
- Abstract plan tasks are mapped onto real rooms and objects. **The gap between plan and reality is where the chaos comes from.**
- Crew follow their timelines until you step in. You can pause and **reassign or send crew** to improvise or do extra jobs *(proposed)*.
- Rooms interact with crew roles and quirks.
- Chaos sources for MVP *(proposed)*: guard patrols, escalating alarms, quirks misfiring.
- **Timer hits 0 → police arrive.** Loot carried out the exit is banked. Anything (or anyone) still inside is lost or caught *(proposed)*.

### 7. Push-Your-Luck Loot
- Extra loot beyond the plan is scattered around the map. Grabbing it costs time and exposure.
- This is the central tension of execution: **stick to the plan or get greedy.**

### 8. Reputation (Notoriety)
- Injured, killed or abandoned crew lower your reputation.
- Low reputation means **worse crew pools** ("people don't want to work with a bad planner").

---

## MVP Scope
- 3 locations: House, Museum, Bank
- About 6 roles to start, with 3 prospects per slot
- Plan timeline, an execution sim with pause and reassign, the economy, and reputation

## Later / Hooks into Core Systems
- **Funny locations** (zoo, baseball stadium, card shop, Santa's workshop, the Louvre) → new contract templates
- More locations (post office, mall, lab, restaurant, military base) → contract system
- Crew badges or rarity tiers → crew system
- Crew synergies and rivalries → quirks × execution
- Scouting phase that partially reveals the map → plan system

## Open Questions
- Are tasks generated from the map, from a fixed list, or from the crew? (Current proposal: a template per location, with methods based on role.)
- Final stat list and what each stat does mechanically.
- Debt structure: fixed total with payments vs endless.
- Art style: hand-drawn sketchbook (as in the mockups) vs something cleaner.

---

## TODO
- List of rooms
- list of task's
- list of roles
- list of stats
- list of quirks
