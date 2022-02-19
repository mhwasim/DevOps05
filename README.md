# DevOps05
DevOps Training Batch 05

Agile & DevOps

Agile is an iterative approach to project management and software development that focuses on collaboration, customer feedback, and rapid releases. It arose in the early 2000s from the software development industry, helping development teams react and adapt to changing market conditions and customer demands.

DevOps is an approach to software development that enables teams to build, test, and release software faster and more reliably by incorporating agile principles and practices, such as increased automation and improved collaboration between development and operations teams. Development, testing, and deployment occur in both agile and DevOps. Yet traditional agile stops short of operations, which is an integral part of DevOps.

DevOps is not a replacement. But, it is a direct successor to Agile. Similar to how with time, practices get better; over time, Agile has also grown its challenges, and DevOps has turned out to be the more optimized practice.

Agile vs DevOps Agile emphasizes collaboration between developers and product management. DevOps includes the operations team as well.

Agile centers the flow of software from ideation to code completion. DevOps extends the focus to delivery and maintenance.

Agile emphasizes iterative development and small batches. DevOps focuses more on test and delivery automation.

Agile adds structure to planned work for developers. DevOps incorporates unplanned work common to operations teams.

Goal of Agile is to improve the speed and quality of software development. Goal of DevOps is to improve the speed and quality of software development.

Agile was a natural replacement to Waterfall model and other Scrum practices. DevOps is not a replacement of Agile but, it is a direct successor to Agile.

==================================================================================================================

Define Continuous Integration, Continuous Delivery & Continuous Deployment

Continuous Integration:
Merge changes back to the main branch as often as possible.
Changes are validated by creating a build and running automated tests against the build.
This is to avoid integration challenges that can happen when waiting for release day to merge changes into the release branch.
Emphasis on testing automation to check that the application is not broken whenever new commits are integrated into the main branch.
Continuous Delivery:
An extension of continuous integration because it automatically deploys all code changes to different environments like testing, hotfix, production after the build stage.
An automated release process you can deploy your application any time by just clicking a button.
Can decide to release daily, weekly, fortnightly, or whatever suits your business requirements.
If truly want to get the benefits of continuous delivery, should deploy to production as early as possible to make sure that release in small batches that are easy to troubleshoot in case of a problem.
Continuous Deployment:
One step further than continuous delivery. With this practice, every change that passes all stages of the production pipeline is released to the customers.
There's no human intervention
Only a failed test will prevent a new change to be deployed to production.
An excellent way to accelerate the feedback loop with customers and take pressure off the team as there isn't a Release Day anymore.
Developers can focus on building software, and they can see their work go live minutes after they've finished working on it.

==================================================================================================================

What are the benefits of Cloud Computing

Reduced IT Costs: ==================== a. The cost of system upgrades, new hardware and software may be included in your contract b. No longer need to pay wages for expert staff c. Energy consumption costs may be reduced d. There are fewer time delays

Accessibility: ================= a. Can be accessed from anywhere if internet is available

Reliability: =============== a. Can always get instantly updated about the changes

Scalability: =============== a. Buy resources according to the need b. Can scale up the resources bought c. Can scale down the resources bought

Business Continuity: ======================= a. In case of disaster backup restored b. Minimal downtime and loss of productivity

Enable Mobility: =================== a. Gives businesses the ability to enable employees to gain access to data and applications from anywhere b. Making employees more productive when on the go

Access to Automatic Updates: =============================== a. May be included in your service fee b. Depending on your cloud computing service provider, your system will regularly be updated with the latest technology

==================================================================================================================

Difference between Git and GitHub

Git is a version control system that lets you manage and keep track of your source code history GitHub is a cloud-based hosting service that lets you manage Git repositories

Git is a free, open-source software distributed version control system (DVCS) designed to manage all source code history GitHub offers all of Git’s DVCS SCM and has some additional features. This includes collaboration functionality like project management, support ticket management, and bug tracking

Git is installed locally on a system, so developers can manage their source code history using their local machines as repositories GitHub is a cloud based, so Internet access is required. It also has a built-in user-management system and a user-friendly GUI

Git can be used without GitHub GitHub cannot be used without Git

==================================================================================================================

Stages of Git

Modified: means that you have changed the file but have not committed it to your database yet.

Staged: means that you have marked a modified file in its current version to go into your next commit snapshot.

Committed: means that the data is safely stored in your local database.

==================================================================================================================

Methods of Git Reset

Hard: ======== makes everything match the commit you've reset to. This is the easiest to understand, probably. All of your local changes get clobbered. One primary use is blowing away your work but not switching commits: git reset --hard means git reset --hard HEAD, i.e. don't change the branch but get rid of all local changes. The other is simply moving a branch from one place to another, and keeping index/work tree in sync. This is the one that can really make you lose work, because it modifies your work tree. Be very very sure you want to throw away local work before you run any reset --hard.

Mixed: ========= It is the default, i.e. git reset means git reset --mixed. It resets the index, but not the work tree. This means all your files are intact, but any differences between the original commit and the one you reset to will show up as local modifications (or untracked files) with git status. Use this when you realize you made some bad commits, but you want to keep all the work you've done so you can fix it up and recommit. In order to commit, you'll have to add files to the index again.

Soft: ======== It doesn't touch the index or work tree. All your files are intact as with --mixed, but all the changes show up as changes to be committed with git status (i.e. checked in in preparation for committing). Use this when you realize you've made some bad commits, but the work's all good - all you need to do is recommit it differently. The index is untouched, so you can commit immediately if you want - the resulting commit will have all the same content as where you were before you reset.

Merge: ========= Was added recently, and is intended to help you abort a failed merge. This is necessary because git merge will actually let you attempt a merge with a dirty work tree (one with local modifications) as long as those modifications are in files unaffected by the merge. git reset --merge resets the index (like --mixed - all changes show up as local modifications), and resets the files affected by the merge, but leaves the others alone. This will hopefully restore everything to how it was before the bad merge. You'll usually use it as git reset --merge (meaning git reset --merge HEAD) because you only want to reset away the merge, not actually move the branch. (HEAD hasn't been updated yet, since the merge failed)


=========================================Assignment 2=========================================

Docker Containers vs Virtual Machines

a) Docker is container based technology and containers are just user space of the operating system Virtual Machine is not based on container technology and made up of user space plus kernel space of an operating system
b) Docker containers when running share the host OS kernel Virtual Machines share hardware resource from the host

c) Docker container is just a set of processes that are isolated from the rest of the system, running from a distinct image that provides all files necessary to support the processes Virtual Machine has Operating System & Application which run completely in isolation

d) Docer reduced IT management resources, reduced size of snapshots, quicker spinning up apps, reduced & simplified security updates, less code to transfer, migrate and upload workloads Virtual Machine reduced physical IT management resources, can be huge in size of snapshots, time required spinning up apps, complex security updates, large transfer, migrate and upload workloads

e) Docer container is faster to build Virtual Machine require time to build

d) Docker container / image is easy to portable Virtual Machine require more resources

References are taken from below link: https://devopscon.io/blog/docker/docker-vs-virtual-machine-where-are-the-differences/

==================================================================================================================

Docker Architecture

a) Docker follows client-server architecture
b) Docker Client, Docker Host and Docker Registry are three main components of architecture

c) Docker Client: users commands (CLI) and REST APIs to communicate with the Docker Deamon (Server) docker build, docker pull, docker run are some commands used at docker client Dockr client can communicate with more than one docker deamon.

d) Docker Host: is used to provide an environment to execute and run applications It contains the docker daemon, images, containers, networks, and storage

e) Docker Registry: manages and stores the Docker images. There are two types of registries in the Docker: Pubic Registry: is also called as Docker hub Private Registry: is used to share images within the enterprise

References are taken from below link: https://www.javatpoint.com/docker-architecture

==================================================================================================================

Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 on a custom network named assignment-2

--> docker container run -d --name assignment-2 --publish 9090:80 --network=assignment-2 nginx

==================================================================================================================

Write command to see logs of the above container

--> docker container logs assignment-2

==================================================================================================================

Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html 

--> docker container run -it --name=assignment-2 -p 9001:80 > /usr/share/nginx/html/index.html

==================================================================================================================

Exit the above container, and now recreate the container by Volume using bind mounting

--> docker container run -it --name=assignment-2 -p 9001:80 -v /usr/share/nginx/html/:/workingfolder/

==================================================================================================================

Command to exec into the above container and replace the default index.html to a custom one, which says that â€œI am becoming a Docker Expertâ€ and it should be persisted for the next times.

--> cd workingfolder
	cat > index.html
	â€œI am becoming a Docker Expertâ€
	^C