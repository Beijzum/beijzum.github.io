## Overview

This section will focus uploading your code onto [GitHub](https://github.com/). It is platform that hosts git repositories onto cloud, and allows developers to collaborate with each other. This section also assumes that you already have an [GitHub](https://github.com/) account. If you do not have a [GitHub](https://github.com/) account, click [here](https://github.com/join) and follow the steps of the sign-up page.

!!! warning

    Ensure that your terminal is in the `rock_paper_scissor` directory that you created previously in :file_folder: [Setting Up Your Project](./Setting%20Up%20Your%20Project.md/#create-project-folder).

## Initializing Local Git Repository

This section focuses on creating a `.git` directory to allow for version control in the terminal.

1.  Create a `.git` directory in the terminal by _typing_ the following:

    ```
    git init
    ```

    a. `.git` directory are part of the version control system that allows developers to create and retrieve different versions of any project.

    b. This allows for version rollbacks if any major mistakes occur.

    !!! success

        Successfully creating a `.git` directory will look like this:

        ![create git init](./assets/uploadS1.png)

    !!! notes

        Professional software developers will use some form of version control for work and for their personal projects.

        You will not be able to see the `.git` directory because it is *hidden* by default.

## Add Code to Git

This section focuses on adding your newly created game into version control.

2.  Stage file in the terminal

    ```
    git add rock_paper_scissor.py
    ```

    a. Staging a file means that you have marked a modified file in its current version to go into the next commit.

3.  Commit file in the terminal

    ```
    git commit -m "I made my first game!"
    ```

    a. Commits can be thought of as snapshots or milestones along the timeline of a project. A git commit command captures a state of a project at that point in time.

    b. Everything in quotation marks after "-m" is a message that tells other developers what changes you made for the current commit. You can replace the message with anything you like as long as it is wrapped in quotation marks.

    !!! success

        Successfully committing your code to your local .git directory will look like the following:

        ![add code to git](./assets/uploadS3.png)

    !!! failure

        If you forget to add and stage a file after modifying it, then the following message will be shown:

        ![add code to git fail](./assets/uploadS3Failure.png)

        Just add/stage the file and then commit the file to fix this issue.

    !!! notes

        A good practice is to have clear and concise messages that tell other developers what you changed in your commit.

## Create Online Repository on GitHub

This section focuses on creating an online repository for you to upload your project to.

4.  Login to [GitHub](https://github.com/) and create a new repository as highlighted below:

    ![make new repository](./assets/uploadS4a.png)

    a. _Click_ on the "+" sign first

    b. _Click_ on "New repository" next.

5.  Enter a repository name

    ![enter repository name](./assets/uploadS5.png)

    a. If your project folder name is not `rock_paper_scissors`, enter the name you used instead.

6.  Click create repository

    ![create repository](./assets/uploadS6.png)

    a. You may change the project visibility to private, so that only you or project collaborators can view the project.

    b. All other settings can be left as default.

    !!! success

        Successfully creating the `rock_paper_scissor` repository will move you to the next page shown below:

        ![create repository success](./assets/uploadS6Success.png)

## Connecting Local Repository to Cloud

This section focuses on connecting your local .git folder to the cloud/remote GitHub repository.

7.  Copy the new GitHub repository link:
    ![copy repository link](./assets/uploadS7.png)

    a. _Click_ on the "copy" button that is highlighted.

8.  Use the terminal to link your local repository to the cloud repository by _typing_ the following:

    ```
    git remote add origin https://github.com/your_github_username/rock_paper_scissor.git
    ```

    a. In Git, "origin" is a shorthand name for the cloud repository that a project was originally cloned from.

    b. The link after the word "origin" should be replaced with the link you copied into your clipboard in the previous step.

    !!! notes

        You may CTRL + V to paste in the terminal. Some Windows version also allow _right-clicking_ in the terminal to paste.

9.  Upload local repository to cloud repository:

    ```
    git push -u origin master
    ```

    a. "master" is the default name given to the first branch present in a Git repository when it is initialized.

    b. Some users will have "master as a default name, while some others will have "main" as a default name. If you encounter an error, try the other.

    !!! success

        Successfully uploading the local repository to the remote repository will look like the following:

        ![add remote origin image success](./assets/uploadS9Success.png)

    !!! failure

        If you type another common branch name like "main", then there is a chance that you will get a "refspec" error shown below:

        ![add remote origin image fail](./assets/uploadS9Failure.png)

        If "main" does not work, try "master". If "master" does not work, try "main".

10. Visit the GitHub repository to ensure changes have been made:

    !!! success

        Successfully uploading the project on to your GitHub repository should look like the following:

        ![github repo](./assets/uploadS10.png)

## Conclusion

By the end of this section, you will have successfully completed the following tasks important to every developer:

-   [x] Initialize a local repository
-   [x] Stage and commit files to a repository
-   [x] Create an online GitHub repository
-   [x] Connect a local repository to an online repository

**Congratulations!** 🥳🎉, you have taken your first steps towards becoming a full-fledged developer. If you have encountered any problems throughout the tutorial, the next section is a compilation of commonly encountered issues.

:material-cog-box: [Troubleshooting](Troubleshooting.md)
