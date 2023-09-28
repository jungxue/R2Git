Version control with GitHub for Rstudio

Still at the drafting stage.

### 1.0 Contents

- [1.1 Basic setups](https://github.com/jungxue/R2Git/blob/master/README.md#12-basic-setups)
- [1.2 Github Basics](https://github.com/jungxue/R2Git/blob/master/README.md#13-github-basics)
- [1.3 Example 1: Setting up a bookdown Project for Study Notes](https://github.com/jungxue/R2Git/blob/master/README.md#14-example-1-setting-up-a-bookdown-project-for-study-notes)
- [1.4 Example 2: Version control for my thesis R codes](https://github.com/jungxue/R2Git/blob/master/README.md#15-example-2-version-control-for-my-thesis-r-codes)
- [Reference](https://github.com/jungxue/R2Git/blob/master/README.md#reference)
-------------------------------------------------------------------------------------------------------------------

### 1.1 Basic setups

**Step 1** Download and install all required software

First, you need to have R (preferably also the latest version of R-Studio) and a Github account to start, and also Git bash for the commands. Here are links for you to start your download. 

- [**R**](https://cran.r-project.org/)
- [**R-Studio**](https://www.rstudio.com/products/rstudio/download/)
- [**Github**](https://github.com/)
- [**Gitbash**](https://gitforwindows.org/) [(automatic download)](https://git-scm.com/download/win)

**Step 2**  Check if you already have git installed In RStudio:

File → New Project → Version Control → Git

If you do not have git or was not set up properly, you will see this
<p align="center">
   <img  src="R2Git1.jpg">
</p>

Otherwise, you will see something like this. 
![screenshot2](R2Git2.jpg)

**Step 3** Introduce ourselves to git

You are a user, so you need to identify yourself.

Open Git Bash or use the terminal tab of R studio, and use the following code to set up your name and email.

```git
$git config --global user. name 'Your Name'
$git config --global user.email 'your@email.com'
$git config user.name
Your name
$git config user.email
your@email.com
```
Note: If you get an error `More than one value for the key user.name`, that is due to your names overriding each other.
You can use `--get-all` and you will see multiple names. 
You can use `--replace-all` option to clear all the names and rename yourself. 

```git
$git config --get-all user.name
'Your
'your
$git config git config --get-all user.name 
$git config --global user.name 'Your Name'
$git config user.name
Your Name
```

**Step 4** Secure Shell (SSH) key (optional)

SSH allows you to connect and authenticate to remote servers.

Tools → Global options → Git/SVN → Create RSA Key → View Public Key.

Copy your key and get on Github https://github.com/settings/ssh/new and associate the key with your account.

And check your connection on R terminal: 

```git
C:\Users\Tokor>ssh -T git@github.com
The authenticity of host 'github.com (192.30.255.113)' can't be established.
RSA key fingerprint is XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX:XX.
Are you sure you want to continue connecting (yes/no)? Yes
Warning: Permanently added 'github.com,XXX.XX.XXX.XXX' (RSA) to the list of known hosts.

Hi, jung! You've successfully authenticated, but GitHub does not provide shell access.

```
After all these setups bro you are all good to go! Chur. 

-------------------------------------------------------------------------------------------------------------------

### 1.2 Github Basics

Here are some of the Core concepts you need to understand before you use Github. 

**Repository**
- This is an online location that contains all your files (and history) for a particular project. You can clone on eor more local repositories to work from. 

**Commit**
- Each commit is a snapshot of your project.
- You can view and travel between commits.

**Clone**
- Copy (clone) an existing repository onto your local drive. 

**Push**
- Making the changes, you have made locally (using git) available to the online repository (GitHub).

**Pull**
- Updating your local repository to the current version in the online repository.

**Fork**
- Making a clone repository from another user's project.
-------------------------------------------------------------------------------------------------------------------

### Reference

- **Ewen Harrison** R-blogger [RStudio and GitHub](https://www.r-bloggers.com/rstudio-and-github/)
- **Blake Seer** UoA SCC [intro to git (for R users)](https://github.com/sccuoa/intro-to-git)
- **Nathan Stephens** Rstudo support [Version Control with Git and SVN](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)
