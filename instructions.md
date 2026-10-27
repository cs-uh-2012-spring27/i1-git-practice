# Instructions

In this assignment, you will familiarize yourself with two common **version control** workflows using **`git`** and **GitHub**: (1) a **centralized workflow** and (2) a branch-based (a.k.a. feature based) workflow. You will also practice creating Issues on Github and linking them to the PRs implementing them.

With the centralized workflow, you will set up a **remote** repository on GitHub and a **local** **cloned** **repository** for your own project and practice **pushing** and **pulling** to/from this remote repository on the main branch.

With the branch-based workflow, you will still use the same repository above but you will not directly work on the main branch. Instead, you will create a branch with your updates and then merge this branch using a **pull request**.

Note that with version control systems such as `git`, it is easy to verify what work has or has not been done by whom on any project via the git log. 

Execute the following instructions in order.


## Part 1: Centralized workflow

In this part, we will try out a simple **centralized workflow**, where developers work with two copies of a repository: a **local** copy, where changes are made; and a **remote** copy, where completed changes are uploaded in order to be archived and shared with others.

### Create a local Git repository

1.  Clone your remote repository on GitHub to your own local machine.

2. Make sure to change directories to the new directory that got created with your cloned repo.

3.  Create a file called `ARTICLE.md` and edit it to include the following:
    - a link to an article or web site you find interesting related to software development/engineering 
    - a short paragraph or two about what you find interesting about that article
    - Use Markdown syntax to make it look nice
    
3.  **Commit** your `ARTICLE.md` file to the local repository, including a meaningful commit message.

4. Edit the `README.md` file in the repo to include your name. Commit your change using a meaningful commit message.

### Push changes to the upstream remote repository

1.  **Push** the latest version of these two files in your local repository to your Github repository.
2.  Your two repositories should now be in-sync (i.e., what you see on your local machine should look the same as what you see on your repository on github.com)

## Part 2: Use branches for a branch-based/feature-based workflow

Note that this is the workflow you will be using for your group projects. However, in the group project, you will be working with other team members who will review your Pull Requests. Since this is an individual repo, we will ignore code review in this step but you will practice it later in the group project.

### Create a branch

1. Create a new branch in your repo using `git checkout -b <yourname>/proofread` . For example, if I were creating this branch for myself I would use `git checkout -b snadi/proofread` or `git checkout -b sarah/proofread`

### Make changes on this branch

1. Carefully proof read the content in `ARTICLE.md` and fix any typos. Add a new section at the bottom of the document called `Proof Reading` and type the sentence "Article checked for typos"
2. Commit your changes and push them. Note that these changes are pushed to the new branch. Since this is your first time pushing to the branch, git will ask you to first set the upstream for this branch. Simply run the command it asks you to use and then push.

### Create a Pull Request

1. Go to your repository on github and go to Pull Requests
2. Create a new pull request to merge the changes from your branch into the `main` branch (see [Make a pull request](https://help.github.com/articles/creating-a-pull-request/))

### Merge the Pull Request (PR)

1. Merge the pull request using the merge button on github
2. Go to your local repo and switch to the main branch (`git checkout main`)
3. Pull the latest changes using `git pull` (remember that the changes from the branch have been merged into main on the remote repository on github but your local repo still doesn't know about it and that's why this step is necessary)
4. If you view the contents of `ARTICLE.md` on your local machine, you should see the new section and statement above.

## Part 3: Organize branches around issues

During the project, every feature request/bug fix/enhancement must be recorded in a GitHub Issue first. You can then link the PR addressing this issue to the issue. That way, development is traced and we understand why these specific changes/commits were needed.

To practice issues, your new feature is about adding a table to your ARTICLE.md file. The table should outline three takeaways from the article and why they matter.

### Create an Issue

1. Follow [https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/quickstart](https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/quickstart) to create an Issue.
2. Your issue must have a meaningful title and a meaningful description. Note that whenever you describe an issue, it is important to precisely specify what is required or what is wrong. For example, the table above is underspecified so your issue description should describe what the columns of the table is.
3. Finish creating the issue and note its issue number.

### Implement the required change

1. Follow the branch-based development flow from part 2 to create a new branch for this new feature.
2. When you open a PR to merge this branch into main, make sure to reference the issue you created in the PR description (e.g., "Resolves Issue #NUM")
3. Merge the PR
4. Close the issue to signal that the work has been completed.
5. Don't forget to switch back to main and pull the changes locally!
