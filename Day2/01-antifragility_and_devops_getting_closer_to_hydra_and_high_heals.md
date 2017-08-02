# Antifragility and DevOps: getting closser to Hydra and High Heals
**Author:** Jan de Vries

## Worries
 * increasing Complexity.
 * Projects.
 * Silos.
 * Command and Control management.
 * Culture in general.

## Under the hood of DevOps: Antifragility
 * Book on Antifragility: "Antifragile" by Nassim Nicholas Taleb.
 * Make change less risky:
   - Make Change easy.
   - **FINISH**

## Asymmetry is key
 * Definition:
   - Anything that has more upside than downside from random events / shocks is antifragile.
   - The opposite is fragile.
 * To discover whether a system is fragile or antifragile, you must a system with one variable's worth of imput to see if adjusting it up or down causes it to become fragile.
   - Example of a variables:
     + Number of deployments per month.
     + Number of tasks coordinated in a project.

## The Opposites of fragile:
 * Robust
 * Resilient
 * Antifragile
 * Example systems:
   - Fragile systems break almost immediately.
     + Agile development is fragile ("agile is fragile").
   - Robust systems are stable to a point, then break.
   - Resilient systems might break at a point, but will go back to stable.
   - Antifragile systems only get better over time.

## How to become less fragile, even antifragile in IT?
 * Introduce stress, change into a system.
   - Examples: 
     + Continuous Deployment.
     + Canary release.
     + A/B testing.
     + Chaos engineering.
       * Latency monkey.
       * Janitor monkey.
       * Conformity monkey.
       * Chaos gorilla.

## Asymmetry is key: Optionality
 * An option is a contract which gives the buyer the right, but not the obligation, to buy or sell an underlying asset or innstrument at a specified strike point. **FINISH**

## Tinkering in IT
 * Covered in book "The Phoenix Project".
 * The third way: continual experimentation.

## Via Negativa
 * The best way for a person or organization to become antifragile is to decrease their downside: things, people, action, habits, or systmes that make you vulnerable to volitility or risk.
 * Get rid of:
   - Hand-offs between teams (spotify).
   - Politics, fear, and ego.
   - Technical debt == what you feel the next time you want to make a change (Gene Kim).
   - Inequalities between MTTR (Mean Time To Repair) and MTBF (Mean Time Between Failures).
 
## Asymmetry is key: Transferring fragility
 * If one party has the downside and another the upside, fragility is being transferred from one party to the another.
 * The reverse: skin in the game.

## Skin in the game missing (projects)
 * The project model leads to:
   - Chasing date, time, cost, and features over benefit
   - Result: PMs do not account for the costs of maintaining the project afterwords.
 * Suggestion: merge in a project team into a hierarchy with infrastructure.
 * 9 square model:
   - **INSERT GRAPHIC FROM ONLINE PRESENTATION: <http://aslbislfoundation.org/nl/?wpfb_dl=1198>**
 * The periodic table of DevOps tools
 * High-heel organization: the goal? **VALIDATE**


## Advise for IT:
 * Watch spotify videos.
 * Read pheonix project.
 * Reduce tech debt.
 * Reduce MTTR.
 * Get rid of silos & projects.
 * Tinker.
 * Release the chaos monkey.
 * Ensure that decision makers have skin in the game (can get sacked).
 
## Advice for Business and IT
**`while (1):`**
 1. Identify the constraint.
 2. Exploit the constraint.
 3. Subordinate everything to the system's contraint.
 4. Elevate the system's constraint.
 5. Identify te next constraint.

## Beware The Cuckoo Effect!
 * "Any foreign innovation in a corporation will stimulate the corporate immune system to create antibodies that will try and destroy the change."
