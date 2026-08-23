## Mission Overview

Congratulations, 
Your onboarding has been successfully completed, and your Cloud Computing Portfolio has been approved by
your supervisor. 
CloudNova Technologies has now assigned you to your first official project. 
Before deploying cloud services, every cloud engineer must understand the infrastructure that powers modern
cloud computing. Your mission is to investigate the components of cloud infrastructure, identify how compute,
storage, networking, and identity services work together, and document your findings as if you were preparing
technical documentation for a client. 
Using the KillerCoda Playground, Linux tools, official cloud documentation, and your GitHub Cloud Computing
Portfolio, you will complete a series of engineering tasks that simulate the planning phase of a cloud deployment.
**Remember:** Great cloud engineers build systems—but exceptional cloud engineers document and justify
every design decision.


## Objectives

At the end of this laboratory activity, you should be able to:
- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components

This laboratory activity explored four core cloud infrastructure components using the Killercoda Ubuntu Playground as a hands-on example. Compute resources were represented by the terminal environment itself, which runs as a virtualized instance sharing physical hardware with other users. Storage resources were examined through the disk space allocated to the environment, reflecting how cloud providers assign virtual disks to instances. Networking resources were identified through the environment's assigned hostname and IP address, similar to how cloud platforms assign machines addresses within a virtual network. Finally, the operating system, Linux, served as the foundation running the entire environment, reflecting its widespread use across real-world cloud servers. A detailed breakdown of each component is available in `cloud-components.md`.

## Tools Used

- KillerCoda Ubuntu playground
- Git (version control tool used to track, commit, and manage changes)
- GitHub (where my repository is hosted, and where I commit)
- draw.io (architecture diagram)
- Bash/Linux Shell — (the command-line interface used to run all investigation commands and Git commands)
- Nano — the command-line text editor used to create and edit your markdown files (e.g., cloud-provider-comparison.md)
- Markdown — (the lightweight formatting language I used to write my .md files)

## Linux Commands Executed 

- git clone https://github.com/norberthulaton07-byte/CCM101-nhulaton.git
- git config --global user.email "user-email"
- git config --global user.name "user-name"
- git add .
- git commit -m "Add Laboratory 02 folder structure"
- git commit -m "Add Checkpoint 4 cloud provider comparison"
- git push origin main
- git pull origin main
- mkdir Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint
- touch README.md infrastructure-report.md cloud-components.md cloud-provider-comparison.md reflection.md
- mkdir screenshots
- touch screenshots/.gitkeep
- ls -R Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint
- cat /etc/os-release
- uname -r
- lscpu | grep "Model name"
- nproc
- free -h
- df -h
- df -hT
- hostname
- hostname -I
- nano cloud-provider-comparison.md
- cd
- pwd
- ls
- ls ~

## Skills Learned

This activity helped me get more comfortable using Killercoda Ubuntu Playground and GitHub (though I'm not really that confident yet), from cloning a repository to committing and pushing changes. I also picked up basic Linux terminal skills, like navigating folders, creating files, and checking system information. Editing files directly in the terminal using a text editor was new to me, but I got the hang of it. I also learned how to write and format Markdown files, which made my documentation look cleaner and easier to read.

## Challenges Encountered 

I ran into a few issues while working through this lab. When I first tried to clone my repository, I got a "repository not found" error because I forgot to replace the placeholder username in the URL with my actual GitHub username. I also encountered an "Author identity unknown" error when trying to commit, which I fixed by setting my Git email and username using `git config`. Later in the activity, my Killercoda session reset unexpectedly, which wiped my local files and folders. This was a bit alarming at first, but I learned that since I had already pushed my earlier work to GitHub, nothing was actually lost, and I just had to re-clone the repository to continue working.
