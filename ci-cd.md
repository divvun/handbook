= Continuous integration and deployment

== Overview

Continuous integration (CI) is a method by which software developers ensure that the software, resources and tools that are committed to a common source control repository are tested for their ability to be built, and ensure that the code can be run and build on a system other than an individual developer's machine. This raises the quality of the tools being developed and ensures that at any time the tool can be delivered to a user with less risk.

It has been core to Divvun's strategy for a number of years to make the delivery of language technology as easy as possible for all stakeholders. As part of this, we have settled on using GitHub Actions to delivery the majority of our language resources (spellers, grammar checkers, etc), keyboards, and other software.

Continous deployment (CD) is the deployment cousin of CI. This is the part of the process pipeline that takes the successful build, when certain criteria are met, and delivers this to a place that a user can access.

As for the continuous delivery part of the equation, due to the specific nature of the types of problems Divvun solves, we use our own tools, specifically the Pahkat framework -- this includes a set of servers, clients and repositories with the specific goal of making it as easy as possible for users to keep their tools up to date, while making it as easy as possible for maintainers to keep their resources up to date for the users.

== GitHub Actions

GitHub Actions is a service offered by GitHub, the source management community website. It is a continuous integration tool, meaning that it will build, test or otherwise do any other programmed function in a build process when triggered by certain actions. These actions can include pushing new data to a repository, proposing a patch via a pull request, or such things as a manual build trigger.

This build process is described in YAML files (a file format that is basically a superset of JSON) in repositories that are enabled for GitHub Actions in a directory named `.github/workflows/`.

A core aspect of this service is the concept of an "action" -- this is a piece of code, usually programmed in TypeScript (a language similar to JavaScript but with strong types), which can be placed as a step within your workflow YAML file. This means that for Divvun users, it is very easy to set up a build using our code signing infrastructure, or to generate a Windows installer, or to do any number of other operating system specific actions without being a subject matter expert.

=== Spellers

The resources for speller builds live in repositories following the pattern `https://github.com/giellalt/lang-XXX`, where `XXX` is the ISO 639-3 language code for the given language.


=== Keyboards

== Pahkat

=== Overview

Pahkat is everything

=== Main repository

The main repository is hosted at https://pahkat.uit.no/main/. This repository holds keyboards, spellers, and other linguistic data required for end-user consumption. This is the default repository configured to be used in Divvun Manager and used by the Divvun Installer.

This repository has two channels, the default stable channel, and the slightly misnamed nightly channel. Nightly channel builds are the most recent build from a given package's repository. Stable are manually promoted stable builds.