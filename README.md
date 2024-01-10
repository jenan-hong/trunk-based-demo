# Trunk-Based Development

## Introduction

Trunk-Based Development (TBD) is a source-control branching model where developers collaborate on code in a single branch called 'trunk'. This approach resists any pressure to create other long-lived development branches by employing documented techniques. As a result, developers avoid merge hell, do not break the build, and live happily ever after.

![truck flow](https://trunkbaseddevelopment.com/trunk1c.png)

## Benefits of Trunk-Based Development

TBD offers several advantages:

- **Continuous Integration and Delivery (CI/CD):** TBD is a key enabler of CI/CD. When developers commit their changes to the trunk multiple times a day, it becomes easy to satisfy the core requirement of CI/CD.
- **Avoid Merge Conflicts:** TBD helps avoid merge conflicts and does not break the build.
- **Faster Development and Deployment Cycles:** With TBD, developers can make smaller and more frequent code changes, leading to faster development and deployment cycles.
- **Improved Collaboration:** All developers are working on the same codebase, which can lead to improved collaboration and communication among team members.

## Challenges of Trunk-Based Development

Despite its benefits, TBD also presents some challenges:

- **Testing:** TBD requires a robust testing process to ensure that code changes do not break existing functionality.
- **Code Review:** With all developers working on the same codebase, it can be challenging to review all changes and ensure that they meet the necessary standards.
- **Conflicts:** With all developers working on the same codebase, conflicts are more likely to occur.
- **Communication:** Effective communication is essential for successful TBD.
- **Discipline:** TBD requires a high level of discipline among team members to ensure that the development process is followed correctly.

Compared to other solutions like GitFlow and other branching models that feature multiple long-running branches, TBD offers benefits such as faster feedback, improved collaboration, reduced code complexity, agility, faster time to market, and support for continuous delivery and DevOps practices.

## Release Flow: A Variation of Trunk-Based Development

![release flow](https://devblogs.microsoft.com/devops/wp-content/uploads/sites/6/2018/04/branchstrategy-cherrypick1.png)

The Visual Studio Team Services (VSTS) team at Microsoft follows a trunk-based development approach, but unlike some trunk-based models, they do not continuously deploy the master to production. Instead, they release their master branch every sprint by creating a branch for each release. When they need to bring hotfixes into production, they cherry-pick those changes from the master into the release branch. The team prefers trunk-based development because it simplifies the branching structure, and there’s a single master branch that everybody works in.

## Shift Left: A Testing Strategy

![release flow](https://learn.microsoft.com/en-us/devops/_img/shift-left.png)

The concept of 'Shift Left' emphasizes the importance of extracting maximum value from testing, given the time and effort it takes away from other tasks such as feature development. It discusses the skepticism around unit testing due to bad experiences with poorly-written unit tests, or fear that unit tests will replace functional tests. The strategy suggests a pragmatic approach to implementing a DevOps test strategy, focusing on building momentum. It also discusses the concept of a DevOps test taxonomy, which classifies individual tests by their dependencies and the time they take to run. The strategy categorizes tests across four levels: L0 and L1 tests are unit tests, L2 are functional tests that might require the assembly plus other dependencies, L3 functional tests run against testable service deployments, and L4 tests are a restricted class of integration tests that run against production. The strategy also discusses the concept of shift-left or shift-right strategies, which involve moving different test types earlier or later in the process. The strategy concludes by stating that if tests can run in every environment from local development through production, they have the same reliability as the product code.

## References

- [Trunk Based Development](https://trunkbaseddevelopment.com/)
- [Release Flow: How We Do Branching on the VSTS Team](https://devblogs.microsoft.com/devops/release-flow-how-we-do-branching-on-the-vsts-team/)
- [Shift Left: A Testing Strategy](https://learn.microsoft.com/en-us/devops/develop/shift-left-make-testing-fast-reliable)
