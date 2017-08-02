# Hay Chef...

 * Looking to add Analytics to Chef.
   - Metrics about timings: which nodes does a chef run go faster on?
   

## My questions
 1. Better support for bootstrapping Windows servers in an enterprise, firewalled, active directory environment.
   * Do more research: question might be answered.
 2. Integration at a cookbook level for running all InSpec tests ever time a chef run / bootstrap runs.
   * Use audit cookbooks.
   * Run InSpec as part of the CD pipeline.
 3. A way to turn off warnings / errors.
   * Big example: "cloned resource" (CHEF-3694), such as installing the same package in different recipes.
     - That's not a bug: that's a feature and by design!
 

