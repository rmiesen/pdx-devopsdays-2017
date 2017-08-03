# I got a lot of problems with infrastructure-as-code and now you're gonna hear about it
**Author:** Max Timchenko

## Agenda
 * What is IaC (Infrastructure as Code)
 * Promises of IaC
 * Problems of IaC
 * Solutions to problems

## Definition of IaC
 * IaC is the process of managing and profvisioning computing, network, and other infrastructure through machine-redable definition files.

## Promises of IaC
 * Business case for IaC
   - IaC is cheaper.
   - IaC is faster.
   - IaC reduces risk.
   - IaC improves availability.
 * Developer case:
   - Infrastructure is just code: uses the same workflow as software development.

## Problems with IaC
 * Most IaC solutions are not programming languages.
   - That includes HCL (Hashicorp Configuration Language)
 * The learning curve for an IaC tool is steep.
 * Boilerplate:
   - 1 simple service (install and cron) 166 lines of code (chef).
   - 2 AWS S3 buckets: 193 lines of code with ACL.
 * Code-related problems:
   - New language, concepts.
   - Boilerplate did not go away
   - High-level docs still needed
 * Cloud providers have lots of caveats, details, not obvious.
 * Summary: there's no free cake.
   - Note taker's commentary: The author stated in the presentation that he's been learning all of this for the last three months. He seems to be suffering from "drinking from a firehose" syndrome. IaC and all the related concepts is complex. You are effectively learning a new programming language, a new framework, a whole new set of tools---some of which are not fully matured---and a whole new workflow. That's going to take at least 6 months to master.


## What to do about it
 * Note taker's commentary: I disagreed with all of his "solutions". You want turnkey configuration, you already have it: they're called "cookbooks", "playbooks", etc. :) IaC is hard, but "voodoo infrastructure" is much harder. Apply proper SCM (Software Configuration Management) practices. Understand your infrastructure and project requirements. If you don't have a business need for this "awesome new tech", then don't use it! Don't just throw tech at the problem and stir/pray: engineer a solution. That's what you're paid for!
