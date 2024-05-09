<img src="./Images/112th_crest.jpg" width="100" height="100">

# 112th Signal Battalion GitHub Lab
### Sections
- [Resources](#resources)
- [Introduction](#introduction)
- [Creating a Remote GitHub Repository](#creating-a-remote-github-repository)

### Resources
- [Git Documentation](https://git-scm.com/doc)
- [GitHub](https://github.com)
- [GitHub Markdown Formatting](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

### Introduction
- This lab will walk you through some of the most common git actions using the GitHub Source Control Management (SCM) developer platform

### Configuring SSH authentication to GitHub
- Create an SSH keypair on your computer
  - Skip this step if you have previously setup an SSH keypair with GitHub
  - Open a terminal window on your computer
  - Run the following command to generate an ssh keypair
    ```
    ssh-keygen -t rsa -b 4096
    ```
  - Accept all of the defaults by pressing enter on each prompt that is asking for input. There is no need to enter anything. Just press enter until you get to the bottom of the page
  - Navigate to the `~/.ssh` directory
    ```
    cd ~/.ssh
    ```
  - Display the contents of your public SSH key
    ```
    cat id_rsa.pub
    ```
  - Copy the entire public key
- Configure your GitHub profile to use your SSH keypair
  - Navigate to [https://github.com](https://github.com) and login
  - Click on your `user icon` in the top right of the GitHub page
  - Click on `Settings` in the drop-down
  - Click on `SSH and GPG keys` on the left-side of the settings page
  - Click on `New SSH Key`
  - Enter a name in the `Title` section
  - Paste your public key into the `Key` box
  - Click `Add SSH key`
  - Your key has been added

### Creating a Remote GitHub Repository
- Navigate to [https://github.com](https://github.com) and login
- Click on the green button labelled `New`

  ![new button](./Images/new_button.png)

- On the `New repository` creation page:
  - Enter a repository name that is the last names of the two partners completing this lab
    - Example: John Smith, and Jill Carter will make the repo `smith-carter-lab`
  - Leave description blank
  - Select the `Public` button
  - Click `Create repository` at the bottom of the page

### Make The Initial Commit to your Repository
- Clone the repository to your local computer
  - Copy the SSH clone link on your new repository's main page
    ![git clone](./Images/git_clone_link.png)
  - Open your terminal window and navigate to the directory where you want to clone your remote repository
  - Clone the remote repository to your computer (this is an example, yours will be diferent)
    ```
    git clone git@github.com:JohnFu11er/smith-carter-lab.git
    ```
- Create your first commit
  - Change into the new directory that was created when you cloned your repository
  - Only one student will perform the next steps:
    1. Create a new file named "README.md" in the repository's directory
    2. Add the text "- Initial commit" to the README.md file and save
    3. From the terminal line add your changes to the staging area
       ```
       git add .
       ```
    4. From the terminal commit your changes that are in the staging area
       ```
       git commit -m "initial commit"
       ```
    5. Push your changes to the remote repository on GitHub.com
       ```
       git push
       ```
  - Both students can now go to the repository on GitHub.com and both should see the changes made to the README.md file
  - The student that did not create the README.md file will to the next steps
    1. Open their local repository's directory and notice that the README.md file that the other student created is not there
    2. Pull the changes from the remote repository on GitHub.com onto the local repository on your computer. In the terminal, open your local repository and run the command:
       ```
       git pull
       ```
    3. You should notice that the README.md file is now in your local repository directory

### Create Two New Branches
- Each student will go to the GitHub repository and add a branch
  - Navigate to the GitHub repository that you created above
  - Click on the drop-down labeled `main` in the upper left side of the screen
  - In the input field that says `"Find or create a branch..."` enter your last name. Each of the two students will creat a branch with their last name
  - Click on the text that says `"Create branch <your_last_name> from main"`
  - At this point there should be three branches in your repository: `main`, and two student branches
  