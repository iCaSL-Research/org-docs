# Issues and Pull Requests Guide

This guide outlines how to create and manage issues and pull requests in our organization's repositories, including the process for reviewing and merging changes.

## Table of Contents
- [Creating Issues](#creating-issues)
- [Working with Pull Requests](#working-with-pull-requests)
- [Code Review Process](#code-review-process)
- [Merging Pull Requests](#merging-pull-requests)

## Creating Issues

Issues are used to track bugs, feature requests, and other tasks related to the project.

### How to Create an Issue

1. Navigate to the repository where you want to create an issue
2. Click on the **Issues** tab near the top of the repository
3. Click the green **New issue** button
4. Fill out the issue template with the following information:
   - **Title**: A clear, concise description of the issue
   - **Description**: Detailed information about the issue, including:
     - What the problem or feature request is
     - Steps to reproduce (for bugs)
   - **Labels (Optional)**: Add appropriate labels (bug, enhancement, documentation, etc.)
   - **Assignees (Optional)**: Assign the issue to yourself or another team member
   - **Projects (Optional)**: Link to relevant project boards
   - **Milestone (Optional)**: Set a milestone
5. Click **Submit new issue**


## Working with Pull Requests

Pull requests (PRs) are used to propose changes to the codebase and request that someone review and merge your changes.

### Using GitHub Codespaces
Codespaces provides a complete, configurable development environment in the cloud that makes it easy to work with repositories:

1. Navigate to the repository on GitHub
2. Click the green Code button
3. Select the Codespaces tab
4. Click Create codespace on main
5. Wait for the codespace to set up 
6. Make your changes directly in the codespace
7. Use the Source Control panel in VS Code to commit and push changes (can also use git commands on terminal) 

Codespaces automatically saves your work.

### Creating a Branch

Before creating a pull request, create a new branch for your changes:

1. Ensure your local repository is up to date with the main branch:
   ```bash
   git checkout main
   git pull origin main
   ```

2. Create a new branch with a descriptive name:
   ```bash
   git checkout -b feature/descriptive-name
   ```
   

3. Make your changes and commit them:
   ```bash
   git add .
   git commit -m "Add clear description of changes"
   ```

4. Push your branch to the remote repository:
   ```bash
   git push -u origin feature/descriptive-name
   ```

### Creating a Pull Request

1. Navigate to the repository on GitHub
2. Click on the **Pull requests** tab
3. Click the green **New pull request** button
4. Set the base branch (usually `main`) and the compare branch (your feature branch)
5. Click **Create pull request**
6. Fill out the PR template with:
   - **Title**: A clear, concise title describing the changes
   - **Description**: Information about the changes, that may include:
     - What changes were made
     - Why these changes are necessary
     - How the changes address the issue
     - Any testing that was done
     - References to related issues (using `#issue-number`)
   - **Reviewers (Optional)**: Add appropriate reviewers
   - **Assignees (Optional)**: Typically yourself
   - **Labels (Optional)**: Add appropriate labels
   - **Projects (Optional)**: Link to relevant project boards (if applicable)
   - **Milestone (Optional)**: Set a milestone (if applicable)
7. Click **Create pull request**

## Code Review Process

Code reviews ensure code quality and knowledge sharing within the team.

### Conducting a Review

1. Navigate to the PR you've been asked to review
2. Click on the **Files changed** tab to see the changes
3. Review the code, looking for:
   - Code correctness
   - Documentation
   - Performance implications
4. Add comments by clicking the `+` button that appears when hovering over a line
5. Submit your review:
   - Click **Review changes** at the top right of the page
   - Choose one of the following:
     - **Comment**: General feedback without explicit approval
     - **Approve**: Changes look good and are ready to merge
     - **Request changes**: Changes needed before the PR can be merged
   - Add summary comments
   - Click **Submit review**

## Merging Pull Requests

Once a PR has been approved, it can be merged into the main branch.


### How to Merge a Pull Request

1. Navigate to the PR page
2. Scroll to the bottom of the PR
3. Choose a merge method:
   - **Merge pull request**: Creates a merge commit (preserves all commits)
   - **Squash and merge**: Combines all commits into one (cleaner history)
   - **Rebase and merge**: Adds commits individually without a merge commit
4. Add any additional details to the commit message
5. Click **Confirm merge/squash/rebase**
6. (Optional but recommended) Delete the branch after merging

### After Merging

- Close related issues or update their status
- Delete the feature branch (can be done automatically through GitHub)
- Deploy changes if applicable
- Notify relevant stakeholders about the changes

---

## Additional Resources

- [GitHub's Documentation](https://docs.github.com/en)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [GitHub Issues Documentation](https://docs.github.com/en/issues)
- [GitHub Pull Requests Documentation](https://docs.github.com/en/pull-requests)
