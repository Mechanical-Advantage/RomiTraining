# Lesson 01: Intro To Git

In the past, you may have been frustrated by not always having the most up-to-date version of code. This is especially difficult with large teams all trying to work on the same project. Git and GitHub are **source control** tools, which have a few key functions:

* Keeping a record of your changes.

* Coordinating developing across a large team.

* Allowing you to know who made what changes.

* Reverting back to a previous state when necessary.

Below are a few useful definitions:

* *Git* is a source control system, available on the command line or through VSCode.

* A *repository* (or *repo*) contains all of the code and history of a project.

* A *clone* is a copy of the repository stored on your local computer. This is what you're editing in VSCode.

* *GitHub* is a website which hosts repositories online, and contains extra tools to coordinate between developers.

* A *commit* is a snapshot of the code. You should get in the habit of creating a commit whenever a new feature, bug fix, etc. is completed and tested. For this curriculum, that will usually be at the end of each meeting or lesson.

* A *branch* stored an series of commits which are not part of the main codebase (though it may be *merged* later). This could be used to develop a new set of features, or divide up workspaces between developers.

* To download new commit from GitHub, we run a *pull* command. You should always *pull* before starting to work on code.

* To upload new commits stored locally, we run a *push* command.  You should always *push* after you make a new commit.

While this can get complex, our goal during this curriculum is to get you comfortable with the basic functions of Git. Please follow these steps to get set up:

1. Install Git by downloading it from git-scm.com

1. Create a GitHub account if you don't have one already. Navigate to github.com and click on "Sign Up", then follow the steps.

2. Send us your GitHub username so that we can invite you to the team organization. This is necessary before you can write to any of the team's repositories.

3. Find the "FallTraining2021Code" repository in our organization, then copy the clone URL by clicking on the green "Code" button.

3. Open VSCode and search the command palette for "Git: Clone", then paste in the URL. Once it completes, open the cloned repository.

4. Search for "Git: Checkout to..." and select your group. This switches the clone to your group's branch, so that your code remains separate.

**When you're ready to make a commit:**

1. Find the source control tab in VSCode.

2. Look at each of the modified files to make sure the the changes are as you expect, then click the plus next to each one to include them in the commit.

3. Enter a commit message to describe your changes concisely. Commit messages are usually written in present tense - for example, "**Add** auto routine for destroying field carpet" not "**Added** auto routine for destroying field carpet".

4. Click the check icon to finish the commit.

5. Click the three dots and then "Push".