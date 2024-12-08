<img width="611" alt="image" src="https://github.com/user-attachments/assets/3ecf8e58-ac4c-4e99-b132-ff851d21dd8b">


# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

-   Git is a version control system that helps track changes in code,
    enabling teams to collaborate on projects efficiently. It is
    important because it allows developers to work on the same project
    without overwriting each other\'s changes and makes it easy to
    track, manage, and revert changes if needed.

2.  How does Git track changes in a project?

-   Git tracks changes using a system of snapshots. Each time you
    \"commit,\" Git saves the current state of your project. It compares
    the changes with the previous snapshot and stores only the
    differences. This allows for efficient tracking and reverting if
    necessary.

3.  What is the difference between a local repository and a remote
    repository in Git?

-   **Local Repository:** This is stored on local machines such as your
    computer and contains your project files and history.

-   **Remote Repository:** This is stored on a server (like GitHub or
    GitLab) and can be accessed by others for collaboration.

4.  What are the basic Git commands?

-   **git init:** Initialize a new repository.

-   **git add:** Stage changes to be committed.

-   **git commit:** Save changes to the repository.

-   **git status:** Check the status of changes.

-   **git push:** Send changes to a remote repository.

-   **git pull:** Update your local repository with changes from the
    remote repository.

5.  How do you check the status of a Git repository?

-   To check the status of Git repository use the command 'git status'.

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

-   Branches purpose is to allow developers to work on testing features
    or bug fixes without affecting the main codebase.

> **To create a branch:** git branch branch-name
>
> **To switch to a branch:** git checkout branch-name
>
> Command 'git checkout --b branch-name' can also be used for creating
> and switching.

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

-   GitLab Desktop and GitHub are platforms for hosting remote
    repositories and facilitating team collaboration. Git is the version
    control tool used locally to manage code changes, while GitLab and
    GitHub provide social coding, open-source and web-based features
    like issue tracking, pull requests, and CI/CD integration.

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

> **Step 1:** Copy the repository URL from GitLab or GitHub.
>
> **Step 2:** Run this command in your local repository: git remote add
> origin repository-URL
>
> **Step 3:** Push your changes: git push -u origin main

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

> **Step 1:** Clone the remote repository: git clone repository-URL
>
> **Step 2:** Create a new branch for your changes.
>
> **Step 3:** Commit and push your changes.
>
> **Step 4:** Open a pull request (GitHub) or merge request (GitLab) to
> get your changes reviewed and merged.
>
> **Step 5:** Pull updates regularly to keep your branch updated: git
> pull

10. How do you resolve merge conflicts in Git?

> **Step 1:** Identify the conflict by running git status.
>
> **Step 2:** Open the conflicting file and manually fix the conflicting
> code.
>
> **Step 3:** Mark the conflict as resolved: git add file-name
>
> **Step 4:** Commit the resolution: git commit

11. What is a pull request, and why is it used in GitHub?

-   A pull request is a request is a proposal to merge a set of changes
    from one branch to another in GitHub. It is used to review, discuss,
    and approve changes before merging them into the main
    branch/codebase.

12. What are some best practices for writing commit messages?

-   Keep the subject line concise.

-   Use the imperative mood.

-   Regular commits.

-   Commit related changes.

-   Separate subject and body.

-   Include tests in commits.

-   Use branches.

-   Fix a workflow.

-   Capitalize the subject line.

-   Write good commit messages or names.

-   Include a brief description of why the change was made if needed.

-   Keep the subject line under 72 characters.

-   Reference issues.
