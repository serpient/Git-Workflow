# Basic Repo Setup
```
git clone <github-repo-link>
# Go to the project folder
git remote add upstream <github-repo-link>
npm install
npm start
```

# Branches
![branch diagram](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LBgap1plocY399TI_RC%2F-LD3ihnzhbIWImq3FpPW%2F-LD3lVo2t4s_QI1KSbws%2Fimage.png?alt=media&token=4bd124cf-ff78-45eb-85b6-9ab99bef113b)

#### Master Branch
The Master Branch always reflects a production ready state, and its the branch that will be deployed to the production server. Only fully tested and approved releases are pushed to this branch. Only Project Match admins will be pushing to this branch. 

#### Development Branch
The Development Branch is used for development of new features and integration of changes. Pull Requests are made from your local branches into development branch. It is only merged after it is checked by other members of the team.

#### Feature Branches
Feature branches are branched off Development, and then merged back into Development Branch once the feature is completed. All branches should following the naming convention, per the examples below:

**Rules:**

- Before you create a new branch or merge a branch, ensure that you pull changes from origin/development (central repository) to ensure that your local repository is up to date. 

- Once you have merged your changes, ensure you push those to origin/development to make them available to the rest of the team.

- As you continue working on a branch, make sure you run git pull origin development frequently, (at least once a day) so that your branch doesn’t get left behind, and to decrease the likelihood of merge conflicts.

- Branch names should start with either bug, feature, refactor, or style

- Descriptors should be hyphenated
```
bug/fixed-all-caps
feature/giant-duck-modal
refactor/add-prop-types
style/everything-is-black
```
# Git Commit Rules

## What should be a commit:
- Each commit should be a single logical change. Don't make several logical changes in one commit. For example, if a patch fixes a bug and optimizes the performance of a feature, split it into two separate commits.

- Don't split a single logical change into several commits. For example, the implementation of a feature and the corresponding tests should be in the same commit.

- Commit early and often. Small, self-contained commits are easier to understand and revert when something goes wrong.

- Commits should be ordered logically. For example, if commit X depends on changes done in commit Y, then commit Yshould come before commit X.

- Test before you push. Do not push half-done work.

## Commit Subject Name Rules:
- Limit the subject line to 50 characters.

- Capitalize the subject line

- Separate the subject name from commit description (if any)

- Do not end the subject line with a period

- Use the imperative mood in the subject line. In other words, name it as if giving a command or instruction. A few other examples: "Clean your room", "Close the door".

- When commit-ing to fix an issue brought up in a PR, refer to the PR # like so:
`[PR139]Fix typo in introduction to user guide`

To remove any confusion, here’s a simple rule to get it right every time. A properly formed Git commit subject line should always be able to complete the following sentence:

**If applied, this commit will your do (subject line here) **

 
**Examples of good commits:**

- If applied, this commit will ... refactor subsystem X for readability

- If applied, this commit will ... update getting started documentation

- If applied, this commit will ... remove deprecated methods

- If applied, this commit will ... release version 1.0.0

- If applied, this commit will ... merge pull request #123 from user/branch

**Notice how this *doesn’t* work for the other non-imperative forms:**

- If applied, this commit will ... fixed bug with Y

- If applied, this commit will ... changing behavior of X

- If applied, this commit will ... more fixes for broken stuff

- If applied, this commit will ... sweet new API methods

## Commit Body Rules
The body should be used to explain what and why vs how.  Just focus on making clear the reasons:

- why you made the change in the first place (the way things worked before the change and what was wrong with that.)

- the way they work now

- why you decided to solve it the way you did

- what side effects it might have
