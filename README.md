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
- 

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