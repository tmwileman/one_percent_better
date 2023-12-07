Current Streak: 3
All Time Best Streak: 11
All Time Total: 14

# scratch build
#Tags: #ScratchBuild #CICD #Compile #Development

# What's a scratch build?
A "scratch build" refers to a type of software build that is created from scratch. This means that the application is built entirely from the base source code without using any previously compiled components or intermediate artifacts. 

# Why are scratch builds important?
- **Ensure build integrity** - Scratch builds ensure that the entire software can be built from its source code from the ground up. This is critical for verifying that all parts of the codebase work together correctly after changes and updates.

- **Identify Hidden Dependencies** - Building from scratch ensure hidden dependencies can be found and documented. These could be specific library versions or external tools that are assumed to be imported but aren't.

- **Prevent local development issues** - Local environments sometimes contain elements or hide issues that would appear in a production environment.

- **Testing the build process** - Testing the build process self is a crucial step in development. Conducting regular scratch builds helps ensure this process works as expected.

- **QA** - In CI and deployment pipelines, scratch builds serve as a QA step. Incorporating a scratch build each time a commit is made helps ensure each change doesn't break the code.

# Summary
Scratch builds are a best practice in software development. They ensure reliability, consistency, and correctness of the build process. Scratch builds are a key part of maintaining software quality, especially in complex systems with multiple contributors.