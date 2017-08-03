# Real Time Configuration: Enforcing Policies with Kubernetes Initializers
**Author:** Kelsey Hightower

## Policy
 * A set of guidelines or rules that determine a course of action.
 * So, how well are you enforcing your policies.

## Admission Controllers:
 * A process that intercepts requests to the Kubernetes API server prior to the persistence of that object.
   - Checks a request to make sure it complies with policy, flunks it out if it doesn't.

## Infrastructure as Code
 * Useful, but can result in spaghetti code if not careful.

## Monoliths vs Microservices
 * IaC (Infrastructure as Code) tends to be monolithic (not necessarily a bad thing).
 * Orchestration platforms are more like microservices (not necessarily a good thing).
   - Advantage: can make changes in isolation from the rest of the codebase and IaC.

## Initializers
 * A list of pending pre-initialization tasks s stored in every object's metadata.
 * [Envoy](https://lyft.github.io/envoy/)---a service initializer---can be used to add in dynamic "micro policy" to Kubernetes.
 * A list of admission controllers and initializers in-play for a container are added to a container as annotations.
