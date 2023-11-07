---
sidebar_position: 50
title: 5. Contribute your changes
---

# Contribute your changes back to the ARK Modding team

## Commit your changes and push them to your fork

In git a "commit" is a "snapshot" of your changes. When you create a commit then such a snapshot is saved locally on your machine. 
If needed commits can be reverted, this allows you go back to an earlier version of your work (represented by the previous commit).

:::tip
In order to protect your work it is recommended to commit your changes frequently. 
:::

To persist your changes on GitHub.com you need to "push" your commits to your forked repository. This does not yet affect the ARK Modding documentation, but your changes will be saved on GitHub.com and can no longer be lost even if your local machine breaks down.

If you are using the GitHub Desktop client the following pages document how to commit and push your changes: [Select changes to include](https://docs.github.com/en/desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project-in-github-desktop#selecting-changes-to-include-in-a-commit), [Push changes](https://docs.github.com/en/desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project-in-github-desktop#write-a-commit-message-and-push-your-changes)

## Create a pull request

A "pull request" (PR), somewhat unintuitively, is a request to merge your changes into "upstream" repository, in this case the ARK Modding documentation repository.

When you create a pull request you are asking the ARK Modding team to review your changes and merge them into the ARK Modding documentation repository. That means you need not be afraid of breaking anything, the ARK Modding team will review your changes and only merge them if they are correct and useful, and GitHub allows an in-progress PR to be updated with new commits, so you can add to it as needed.

To create a pull request you need to:

1. Visit your forked repository on GitHub.com
2. Click the "Contribute" button above the file list and select "Open pull Request"
    ![Open Pull Request Button](/img/docs/contrib/open_pr.png)
3. You will be taken to a page showing a comparison between the current state of the ARK Modding documentation and your forked repository. Here select "Create Pull Request".
4. Now enter a descriptive title and a useful description of your changes, then click "Draft pull request" or select "Create pull request" from the dropdown.   
    ![Create Pull Request Button](/img/docs/contrib/create_pr.png)    
    A draft pull request will indicate to the ARK Modding team that your changes are not yet ready to be merged, a normal pull request that you are ready for your changes to be merged.
    :::tip
    Make sure to check the "Allow edits by maintainers" checkbox, this allows Staff to directly fix small issues in your pull request without having to ask you to do it.
    :::
5. Now just wait for the team to review your changes and either merge them, or ask you for final adjustments.