# Version control
Below, you can learn how to get started with version control, as well as find guides and guidelines for typical tasks undertaken by Amsterdam UMC researchers.

## Getting started
A basic guide to git is available via the [Software Carpentry](https://swcarpentry.github.io/git-novice/). Slightly more advanced guides can be found at the [Code Refinery](https://coderefinery.github.io/git-intro/#) and [The Turing Way](https://the-turing-way.netlify.app/reproducible-research/vcs.html).

## Where to host your code repository?
Please host your repository under the [Amsterdam UMC organization on GitHub](https://github.com/AmsterdamUMC). To get access to this organization, get in touch with Thomas Pronk.

## How to name your code repository?
Please keep the following in mind:
* Only use lower-case characters for words; abbreviations can be in UPPER-CASE
* It is not required to add Amsterdam UMC to your repository name

For example, if you create a repository for a software application called "Epic EEG Tool", then name the repository `epic-EEG-tool`. Under the Amsterdam UMC organization, the URL to your repository would then look like this: `https://github.com/AmsterdamUMC/epic-EEG-tool`

## How to prevent accidentally committing personal/sensitive data to the repository?
To be sure that no personal or sensitive data ends up in your repository, we recommend setting up multiple lines of defense, as outlined below.

### 1. Have a directory structure that separates code from data
Assume our example Epic EEG Tool is part of a project (called "Epic EEG Project") that also includes data, then create a folder structure like this.
```
# The root directory of your project
/epic-EEG-project/
# The code of your project; this will be under version control
/epic-EEG-project/epic-EEG-tool/
# The data of your project
/epic-EEG-project/data/
```
Structuring your project as above will ensure that data is less likely to accidentally end up in the directory under version control (`/epic-EEG-project/epic-EEG-tool/`), and so end up on GitHub.

### 2. Add the extensions of your data files to `.gitignore`
The `.gitignore` file specifies which files and directories are ignored by git (details [here](https://git-scm.com/docs/gitignore)). Imagine our Epic EEG Project includes participant data files with the extensions `.bids` and `.csv`. A `.gitignore` file like the one below would exclude these files from version control.
```
*.bids
*.csv
```

### 3. Be careful when pushing to GitHub
Whenever you push a set of changes to your remote repo (GitHub), take a quick look to check whether no personal/sensitive data is accidentally included. Be careful with secrets (e.g., passwords, API keys, OAuth IDs), personally identifiable information (e.g., email addresses), and internal server names. 

When publishing a private repository as a public repository, just removing sensitive data from your files does not suffice; after all, the removed data is still in the version control system. Therefore, create a new local repository, copy the files you want to publish to the new repository, and push it to GitHub. If this is not acceptable because you really must retain the version history but without the sensitive data, [follow these guidelines](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository).

### 4. What not to put on GitGub
The guidelines in these pages concern the publication of code written by Amsterdam UMC employees, so as to share this code with the world. Therefore, only put code on the Amsterdam UMC GitHub that was written as part of your employment for Amsterdam UMC (or AMC/VUmc). Moreover, do not put on GitHub or other public version control platforms any code:
* **Of which the Amsterdam UMC has no intellectual property rights.** Of course, your repository may contain libraries, components, image files, and source files that originated partly or entirely from outside the Amsterdam UMC. But their license should be compatible with [the license of your repository](choosing-license.md).
* **As a private repository.** Cloud-based version control is not highly secure. Hence, if you want a private repository for development of your code (as opposed to sharing your code with the world) you should not use the Amsterdam UMC GitHub if security is important. Either store the repository on a share (_afdelingsschijf_) or request access to the Amsterdam UMC Gitlab, which is hosted on the Amsterdam UMC intranet (ask the ICT service desk). 
