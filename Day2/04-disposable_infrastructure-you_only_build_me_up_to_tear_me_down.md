# Disposable Infrastructure: You Only Build Me Up To Tear Me Down
**Author:** Paige Bernier

## Disposable Infrastructure: definition
 * A tale of two versions
   - v1: not built by disposable infrastructure.
     + Much time spent debugging services.
   - v2: can be spun up by the CD engine, so long as you have the rights to do so.
 * **Disposable Infrastructure:** Automating the process of provisioning, configuring, and destroying infrastructure.
   - Aka: "single click deployment."
 * Un-definitions:
   - Not necessarily "immutable infrastructure"
   - No "pets" or "snowflakes" infrastructure. Everything _must_ be recreatable on-demand!

## Infratron
 * A wrapper tool around provisioning, configuration, and deployment tools.
 * DI (Disposable Infrastructure) process:
   1. Parse
   2. Provision
   3. Configure
   4. Verify/Package

## Toolchain
 * Requirements:
   - Cloud provider-agnostic.
   - Easy to share environments.
   - Full deploy in under 10 minutes.
 * Cloud: AWS.
 * Provisioning: Terraform.
   - Workflow:
     + `terraform plan`: lists what actions Terraform would do if you actually run it.
     + `terraform apply`: Actually applies actions to infrastructure.
       * Live state of infrastructure tracked in files, can---and should---be added to VCS
     + `terraform graph`: Creates a dependency graph of your infrastructure.
     + `terraform destroy`: Destroys all created infrastructure.
 * Configuration: Ansible
   - Configurations are called playbooks and are written in YAML.
   - Can tag individual playbooks.

## AMIs: to bake or not to bake?
 * **AMI:** Amazon Machine Image
 * Is the service mature enough?
 * How many Instances are involved?
 * Are we ready to change the deploy story?
 * How fast do we need to deploy something and how big is the scale?
 * HashiCorp's `packer` can help here.

## Gotchas:
 * Testing: a little iffy.
   - Note taker's comment: use a System Test level tool like InSpec (from the Chef stack, but it likes Ansible too).
 * The tools sometimes lie to you.
 * Fail early, quickly, and loudly.

## Why?
### The case for Disposable Infrastructure
 * Enables you to spin back up the exact environment a customer has to reproduce a bug.
 * Test new changes.
 * Peace of mind that the infrastructure can be rebuilt from the ground up.

### Pros:
 1. Reproducible.
 2. Configuration-driven.
 3. Extensible.
 
