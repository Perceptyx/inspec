# Functional Testing Area for Example Plugins

## What example tests are provided?

Here, since this is a CliCommand plugin, we provide one set of functional tests:

 * inspec_resource_lister_test.rb - Runs `inspec resource-lister` in several circumstances, and verifies the output from the process.

## What are functional tests?

Functional tests are tests that verify that your plugin works _as would be seen by a user_. Functional tests generally do not have inside knowledge about the inner workings of the plugin.  However a functional test is very interested in changes that you plugin make to the outside world: exit codes, command output, changes to files on the filesystem, etc.

To be picked up by the Rake tasks as tests, each test file should end in `_test.rb`.

## Unit vs Functional Tests

A practical difference between unit tests and functional tests is that unit tests all run within one process, while functional tests might exercise a CLI plugin by shelling out to an inspec command in a subprocess, and examining the results.

