# Exploring CI/CD Pipelines using the AWS Ecosystem

## Today's Progress

- **Continuous integration/continuous delivery (CI/CD)** is a topic I've wanted to revisit for a while. I've worked as a solo developer for the past few years, and while source control has been a constant practice of mine the entire time, many of the newer tools (like GitHub Actions) and emerging best practices weren't at the top of my priorities during the constant pace of project deadlines. The overall promise of CI/CD has been very enticing, and I'm happy to use this cloud journey as an opportunity to revisit and rebuild my use of best practices in this area.

- I'm deliberately reviewing these practices now, so that I can incorporate and build upon them as I work on more **#100DaysOfCloud** projects and my personal portfolio projects.

- Read the AWS documentation on [CI/CD concepts](https://aws.amazon.com/devops/#cicd), as well as the specific documentation for their suite of developer tools: [CodeCommit](https://docs.aws.amazon.com/codecommit/), [CodeBuild](https://docs.aws.amazon.com/codebuild/), [CodeDeploy](https://docs.aws.amazon.com/codedeploy/) and [CodePipeline](https://docs.aws.amazon.com/codepipeline/).

- Worked through AWS' [tutorial](https://aws.amazon.com/getting-started/tutorials/continuous-deployment-pipeline/) on setting up a continuous deployment pipeline. I first used an existing GitHub repo of mine, then set up a new CodeCommit repo for the process.

- Watched an excellent presentation by AWS' Chris Munns and iRobot's Ben Kehoe from re:Invent 2017 [Building CI/CD Pipelines for Serverless Applications](https://www.youtube.com/watch?v=dCDZ7HR7dms) (recommended by [@chris_the_nagy](https://twitter.com/chris_the_nagy/status/1286400291810816002)).

## CI/CD Principles

It's important to be clear on the distinctions between the 3 concepts in this area, which were somewhat blurred together in my understanding:

- **continuous integration (CI)**: code changes are merged into a central repository and automated builds are generated and tests are automatically run.
- **continuous delivery (CD)**: code changes are automatically _prepared_ for a release to production.
- **continuous deployment**: a complete workflow combining CI & CD, so that changed are merged, built/tested and then _automatically_ deployed to production.

As noted in the AWS documentation and in the AWS workflow pictured below, the critical distinction between continuous _delivery_ and _deployment_ is _"the presence of a manual approval to update to production. With continuous deployment, production happens automatically without explicit approval."_

![The CI/CD Workflow](../static/continuous_integration.4f4cddb8556e2b1a0ca0872ace4d5fe2f68bbc58.png)

## Continuous Integration

- Like many DevOps concepts, CI is both a cultural commitment/set of practices and a suite of tooling.

- The primary reason to adopt CI is to rapidly surface any merge conflicts or bugs arising from fresh code.

- The existence of automated E2E testing doesn't free developers from the responsibility to develop and run unit tests locally prior to commits.

## Continuous Delivery

- CD deploys all code changes into a testing environment and/or a production environment after the build stage.

- The end result of CD is a built package that is ready to be deployed and which has been extensively tested in an environment identical to, and under tests to simulate the stresses and demands of, the final production space.

- Types of tests that are often employed during CD in the testing environment include:

  - UI testing
  - load testing
  - integration testing
  - API reliability testing

## Continuous Deployment

- With automated deployment, code that passes the tests (and any other criteria set) is autonomously deployed into live production.

- There are additional tooling/configuration requirements necessary when considering adopting a fully-autonomous deployment setup, beyond automated testing:

  - Must have real-time monitoring and alerts, to enable assessment of the changes (positive and negative) in the production state before and after changes are deployed.

  - Must have the ability to revert or roll back a deployment, if a breaking change or other bugs surface after deploying.

  - Ideally, changes will be able to be automously deployed in a canary or green-blue setup, where the stability of the new changes can be monitored prior to roll out across all production servers.

  - Also ideally, the monitoring/alert system should be able to trigger a rollback autonomously, after which the developers can assess the situation without the ongoing crisis of a problem deployment weighing on them.

## Visit Me on GitHub

- This blog post is also viewable on my [#100DaysOfCloud Github repo](https://github.com/quinceleaf/100DaysOfCloud/blob/main/Journey/001/Readme.md), where you can also follow my progress.

## Useful Resources

Note: I have an annual subscription to [Packt](https://www.packtpub.com) – highly recommended! – so I am able to read or watch any of their books or videos, so I will often have their resources listed. Tip: Packt makes available **one book or video for free every day** – sign up for an account (free), visit their [Free Learning](https://www.packtpub.com/free-learning) page each day to see if the offered title interests you, and permanently add it to your library or download it.

- [Building CI/CD Pipelines for Serverless Applications / AWS re:Invent 2017](https://www.youtube.com/watch?v=dCDZ7HR7dms)
- [Effective DevOps with AWS, 2nd ed / Packt ](https://www.packtpub.com/virtualization-and-cloud/effective-devops-aws-second-edition)
- [What is Continuous Integration? / AWS](https://aws.amazon.com/devops/continuous-integration/)
- [What is Continuous Delivery? / AWS](https://aws.amazon.com/devops/continuous-delivery/)
- [Tutorial: Set up a Continuous Deployment Pipeline using AWS CodePipeline / AWS](https://aws.amazon.com/getting-started/tutorials/continuous-deployment-pipeline/)

## Social Proof

[Twitter](https://twitter.com/quinceleaf/status/1286857082646466560)
[LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:6692620807883104256/)
