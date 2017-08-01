# QAELK: Are our tests any good?
## Roadmap
 * problems with testing at Puppet
 * Why we built QAELK
 * What is QAELK?
 * How we're using QAELK?
 * QAELK v1 vs v2
 * Demo of QAELK v2.
 * Goals, Dreams, etc.


# Speech
 * Thesis: You can use data to make your test suites more efficient & cheaper using **science**.
 * Testing at Puppet:
   - Too Many
     + Pipelines
     + Supported platforms
     + Configurations
     + Jenkins restarts
     + difficult to keep track of it all
 * Why QAELK?
     + Are our tests providing value?
     + What makes a test valuable
     + which tests tell us our code is broken?
 * QAELK: Quality Assurance ElasticSearch Logstash Kibana(Grafana)
   - A dashboard for aggregating and visualizing data about our acceptance testing
 * Helps us make data-informed decisions based on:
   - Test duration
   - Test flakiness.
   - Other things.
 * How we use QAELK;
   - Identify most expensive tests
   - Identify flaky tests
   -  See failure history of tests
 * QAELK Phase 1:
   - First attempt at testing metrics in CI based on ELK.
   - Aggregated acceptance testing results.
   - Learning things about how our tests run in CI.
   - Keep acceptance testing valuable.
 * QAELK Phase 2:
   - Replace the stack:
     + Google BigQuery (Replaces ElasticSearch)
     + Custom application Dr. Teeth (replaces Logstash)
     + Looker (replaces Kibana/Grafana)
 * Benefits of the new stack
   - Custom dashboards built in looker
   - ***FILL IN***
 * What's Next?
   - Go beyond the Proof of Concept phase.
   - Polish what we have.
   - Integrate with existing tools at Puppet that identify transient errors.
   - Dynamically tier tests based on pass/fail rates.
