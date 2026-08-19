## Mission Overview

Congratulations, your onboarding has been successfully completed, and your Cloud Computing Portfolio has been approved by your supervisor. CloudNova Technologies has now assigned you to your first official project.

Before deploying cloud services, every cloud engineer must understand the infrastructure that powers modern cloud computing. Your mission is to investigate the components of cloud infrastructure, identify how compute, storage, networking, and identity services work together, and document your findings as if you were preparing technical documentation for a client.

Using the KillerCoda Playground, Linux tools, official cloud documentation, and your GitHub Cloud Computing Portfolio, you will complete a series of engineering tasks that simulate the planning phase of a cloud deployment.

 **Remember:** Great cloud engineers build systems—but exceptional cloud engineers document and justify every design decision.

## Mission Objectives

At the end of this laboratory activity, you should be able to:

- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Tools Used

- KillerCoda Ubuntu playground
- Git (command line)
- GitHub (web editor + direct commits)
- draw.io (architecture diagram)
- Markdown

## Linux Commands Executed

**Linux commands**
- `cat /etc/os-release`
- `uname -r`
- `lscpu`
- `nproc`
- `free -h`
- `df -h`
- `mount`
- `hostname`
- `hostname -I`

**Git commands**
- `git config`
- `git clone`
- `mkdir`
- `touch`
- `git add`
- `git commit`
- `git push`

## Skills Learned

- **Using Git from the command line** — This was my first time using `git add`, `git commit`, and `git push` from the command line.
- **GitHub authentication** — I encountered the "Password authentication is not supported" error when trying to push my files. This helped me learn about using a Personal Access Token for GitHub authentication.
- **Basic Linux commands** — I practiced using Linux commands to check system information, including the operating system, CPU, RAM, storage, mounted filesystems, hostname, and IP address.
- **Markdown formatting** — I learned that Markdown formatting affects how a document is displayed. I also fixed an issue where my report appeared as one paragraph instead of being separated into different lines and sections.
- **Git file tracking** — I learned that Git does not track empty folders. This explained why my `screenshots/` folder did not appear in the repository until I added a file inside it.

## Challenges Encountered

- **GitHub authentication** — My first Git push failed because password authentication is not supported. So I learn how to make one token.
- **Linux command syntax** — I made simple typing mistakes such as `cat/etc/os-release` instead of `cat /etc/os-release` and using `run mount` instead of `mount`. These mistakes taught me that Linux commands need to follow the correct syntax.
- **Empty folders in Git** — My `screenshots/` folder did not appear in GitHub because it was empty. I learned that Git tracks files and not empty directories. I just add the folder in github website instead
- **Markdown formatting** — Some of my Markdown content did not initially display the way I expected. I had to adjust the formatting and spacing so that the content appeared as separate sections and lines.
