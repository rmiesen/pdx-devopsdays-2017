# Adopt a Painless Continuous Delivery Culture, add more Business Value
Author: Geshan Manandhar
@geshan

"Your deploys should be as **boring, straightforward, and painless** as possible."

## Deployment, 5 years ago 
 * Send an email to the deployment engineer, they deploy it
 
## Deployment, now:
 * All automated with ***FILL IN***

## Continuous Delivery
 * A software development discipline where you build software in such a way that it can be deployed on demand at any time.

## Continuous Delivery vs Continuous Deployment
 * The only difference is that the deployment of the resultant is a manual step in Continuous Delivery whereas in Continuous Deployment it's an automated process.

"Your work responsibilities boil down to two things, either **add value to customers*8 or **save cost** for the business"

## How we do Continuous Deployment at Namshi
### Tech stack
 * ~100 micro-services
 * Servers on AWS and managed by salt stack and Terraform.
 * Small part of backend is in PHP, NodeJs + Js.
 * All apps are Dockerized
 * Apps are deployed with Kubernetes

### Easy deploy process
 * User --> Nancy Deploy --> HU Bot --> Kube deploy --> Deploy output --> HU Bot --> Deploy Result --> User
 * Every change is tracked both app code and infrastructure code.

### Continuous Delivery pipeline
 1. Code is pushed to GitHub on a feature branch.
 2. Tests run on CI server (Travis).
 3. Changes are peer reviewed.
 4. Changes are tested on staging.
 5. Changes are pushed to production w/ a tag.
 6. Logs and resources are monitored.
 7. After sometime, tag is merged to master.
 
### DevOps Adoption Outcomes
 * Migrating to a REST-based JSON API triggered a transformation
 * Moving to microservices enabled us to ship changes faster
 * A culture of central logging and monitoring is important
   - [Sematext](https://sematext.com/)
   - New Relic
 * Shipping Docker containers is more consistent than shipping just code.
   - Eliminates any discrepancies between dev, test, and stage by automating the configuration.
 * Feature flags and canary deployments keep us on the safe side
   - Canary deployment: Deploy to a small percent of the customer base rather than all of the customer base.
 * We used [GoReplay](http://goreplay.org) to replay production traffic to staging.
 * Vegeta helped us load test some of our customer facing app.
   - Vegeta: a versatile HTTP load testing tool built out of a need to drill HTTP services.

## Organization Transformation Steps
 1. Start with an automated CD (Continuous Delivery), ZDD (Zero-Downtime Deployment).
 2. Introduce testing and implement CI (Continuous Integration).
 3. Kickoff logging and monitoring for the team.
 4. Follow on with Infrastructure as Code with a Disaster Recovery.
 5. Put in configuration management tools in practice.
 
## Key Takeaways
 1. Automate your process, track each change.
 2. If you can, always do small, atomic deployments with GitHub flow.
 3. Strong culture of logging and monitoring will take you a long way.
 4. Infrastructure as Code software and configuration management tools are life savers.
 5. Do effective postmortem discussions and implement action items.
