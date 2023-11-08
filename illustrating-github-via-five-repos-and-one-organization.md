# Illustrating GitHub via five repos and one organization
Git and GitHub can support very sophisticated development workflows. Often I don't need that much, but sometimes I do. Below is a tour of five GitHub repos and one GitHub organization, starting out simple, then introducing some more advanced features. 

----

* **[JASMIN](https://github.com/tpronk/JASMIN)** Solo project, using GitHub as a versioned cloud storage.

  * [Just pushing commits to the server, often no commit message](https://github.com/tpronk/JASMIN/commits/master)
  * [README file](https://github.com/tpronk/JASMIN#readme) formatted with [GitHub flavored MarkDown](https://gist.github.com/Myndex/5140d6fe98519bb15c503c490e713233)
  * [Single branch with outdated name: master](https://github.com/tpronk/JASMIN/branches).
  *  "This repository has been archived by the owner on Sep 30, 2023. It is now read-only".

----

* **[jsQuestPlus](https://github.com/kurokida/jsQuestPlus)** Two-person project; a bit more coordination. 

  * [Proper commit messages](https://github.com/kurokida/jsQuestPlus/commits/main)
  * [Main, dev, and feature branches](https://github.com/kurokida/jsQuestPlus/branches)
  * Some governance via [Forking](https://github.com/tpronk/jsQuestPlus) and [Pull Requests (PRs)](https://github.com/kurokida/jsQuestPlus/pull/8)
  * [GitHub Discussions for dialogue on the code](https://github.com/kurokida/jsQuestPlus/discussions)

----

* **[splithalfr](https://github.com/tpronk/splithalfr)** Pet project where I try out fancy DevOps.

  * [Commit messages have PsychoPy-style tags: ENH, BF, ...](https://github.com/psychopy/psychopy/blob/dev/CONTRIBUTING.md#3-committing-your-changes)
  * [Software releases](https://github.com/tpronk/splithalfr/releases) numbered via [SemVer (x.y.z)](https://semver.org/) and [documented](https://github.com/tpronk/splithalfr/releases/tag/v2.2.2) via ["keep a changelog"](https://keepachangelog.com/en/1.1.0/)
  * Linking GitHub Discussions, Issues, and Pull Requests:
    1. Sera asked a question in [discussion #3](https://github.com/tpronk/splithalfr/discussions/3)
    2. This points to a bug described in [issue #4](https://github.com/tpronk/splithalfr/issues/4), with a link to dicussion #3
    3. The bug is fixed in [Pull Request #8](https://github.com/tpronk/splithalfr/pull/8), with a link to issue #4
  * Non-GitHub DevOps:
    * [Distribution via package manager (CRAN)](https://cran.r-project.org/package=splithalfr)
    * [Automated tests via R ecosystem](https://github.com/tpronk/splithalfr/tree/main/tests)

----

* **[psychojs_testing](https://github.com/psychopy/psychojs_testing)** A CI/CD pipeline with an advanced testing workflow

  * [Documentation in a GitHub Wiki](https://github.com/psychopy/psychojs_testing/wiki)
  * [CI/CD Workflows via GitHub Actions](https://github.com/tpronk/psychojs/actions/workflows/Automated%20Test%20(full).yml). Click "Run workflow" to see the inputs.
  * [Workflow credentials in GitHub Secrets](https://github.com/tpronk/psychojs/blob/main/.github/workflows/Automated%20Test%20(full).yml#L29)
----

* **[rs-report-workflow](https://github.com/tpronk/rs-report-workflow)** Extracting software mangement metadata from repos
  
  * Obtain repo-data via a [Python module](https://github.com/PyGithub/PyGithub) that talks to the [GitHub REST API](https://docs.github.com/en/rest)
  * Extract information with some [machine learning (SOMEF)](https://github.com/KnowledgeCaptureAndDiscovery/somef/)
  * [Credentials in environment variables](https://github.com/tpronk/rs-report-workflow/blob/77290a5050ffee34be7debae9fe7b4b0e72bf623/src/01.scrape.py#L34); needs an update to SOMEF: [SOMEF issue #591](https://github.com/KnowledgeCaptureAndDiscovery/somef/issues/591)

----

* **[AmsterdamUMC](https://github.com/AmsterdamUMC)** Pilot GitHub organization

  * [Teams ogranized in Amsterdam UMC departments and groups](https://github.com/orgs/AmsterdamUMC/teams/everyone/teams)
  * Roles: admins, team contacts, and members
  * [Organization-level discussion with accouncements](https://github.com/orgs/AmsterdamUMC/discussions/2)
  * [Project for AmsterdamUMC repos to feed to rs-report-workflow](https://github.com/orgs/AmsterdamUMC/projects/1?pane=info)



