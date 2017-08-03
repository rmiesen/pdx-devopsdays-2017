# Dissecting the Chef Role Cookbook

 * This is a cookbook pattern for using roles.
 * Roles
   - Used to define infrastructure
   - Either in JSON or Ruby.
   - Contains name, description, run-list, and attributes
 * Limitations
   - Not versionable.
   - Can create a lot of mess.
 * How to use roles in a safe, versionable fashion.
   - Create a cookbook that contains a role.
   - Contains:
      ```
      metadata.rb
      roles/default.rb
      attributes/default.rb
      ```
   - Move your run_list into a recipe
   - Move your attributes to the attributes file.
   - Can version this, run kitchen on it like any other cookbook.
