---

layout: ots
title: Introduction

---

Note: This module contains a lot of detail, on a first reading don't feel the need to undertand everything. It's enough for you
to feel comforable with version control as a concept.

#What is Version Control and how do Version Control Systems work?

Version Control (VC) is a common practice used to track all the changes that
occur to the files in a project over time. It needs a Version Control System (VCS) tool to work.

What the version control tools do?

*  Provide comprehensive historical information about the work done on the project
*  Help prevent the lost of information (e.g. edits being overwritten)
*  Help the project team be more efficient by using parallel development
(and often integrating with other tools such as: Ticket Systems; built Systems; project management etc.)
*  Helping individual developers be more efficient with tools such as difference reports

Think about how you work on a computer.

You create stuff, it might be a computer program you are writing, your resume for a job application, a podcast or an essay.
The process we all follow is usually the same. You create a basic draft version and you refine it over time by making lots of different changes.
You might spell check your text, add in new content, fix bugs, re-structure the whole work and so on.
After you finish your project (and maybe release it to a wider audience) the material you created can be used as the basis for a new version of the project.
But that is not the end of the story.

Let's assume we have created a computer progam. As time goes on people discover bugs and ask for new fatures, request special versions and so on. 
How do you keep track of these changes? Remove mistakes, bring old material forward into new versions, merge changes from one verwsion to another.

As well as computer code your project might have other types of files. For example icons, project plans, setup scripts, research notes etc.,
and losing all that information even when it's not part of the final project could be a disaster.


Now let's add another layer of complexity.

Our project might be big enough that we are team working on the project together and we all make changes to the digital files (also called assets).
That will introduce a lot of potential problems. For instance a developer may save their work and overwrite someone else's changes.

#So how does Version Control help keep track of your work and digital assests?

The way that a VCS works by recording a history of changes. What does that mean?

Every time a change is completed (for example fixing a bug in a project) the developer decides a logical ''save''
point has been reached and will store all the file changes that make up the fix in the VCS database.

The term often used for a group or changes that belong together like this is a __changeset__.
As well as changing lines of code in source files there might be changes to
configuration files, documentation, graphic files and so on.

Along with the changes to the files the developer will be prompted by the VCS  to provide a
description of the change with a __commit message__ which is appended to the __commit log__.

The process of storing the changes in the VCS database
(usually refereed to as the __repository__ or repo for short)
is called __making a commit__.

The hard work in making a commit is done by the VCS,
all the developer does is issue the commit command and provide the commit message.
The VCS software calculates which files have changed since the last commit and what has changed.
It then stores these changes, plus the commit message, the date, time, name of the developer (committer),
commit message and other information in the repository.

Version Control is also sometimes refereed to as [Revision Control](http://en.wikipedia.org/wiki/Revision_control )

#Why is Version Control is so important?

Imagine a software project.
It might have hundreds of files (for example source code, build scripts, graphics, design documents, plans etc.)
and dozens of people working on the project making different types of changes.
There are several problems that will happen:

1. Two people might be editing the same file at once and changes can be overwritten
1. After the project has been running for some time it's very hard to understand how the project has evolved and what changes have been made.
How can we locate a problem that might have been introduced some time ago.
Just fixing the problem may not be enough, we probably also need to to understand the change that introduced it.
1. If two people want to change the same file one will have to wait for the other to finish, this is very inefficient
1. If two people people are making (long running) changes to the project it may take some time for the both sets of changes to be compatible with each other.
If the same copy if the project is being updated with both sets of changes then the project may not work correctly or even compile

There are three core things a VCS helps do:

1. Answer the following questions: "What changes were made in the past?", "Why were they made?" and "Who made them?" (via commit history and commit comments)
1. Individual developers find this information useful as part of their daily workflow and
it also helps organisations with their compliance and audit management
1. Undo a half complete or incorrect change made in error and "roll back" to a previous version
1. Recreate a "snapshot" of the project as it was at some point in the past
1. Allow two streams of changes to be made independently of each other and then integrated at a later date (parallel development).
This feature depends on the specific features of the VCS tool you are using

You may find the following additional reading useful in introducing important ideas: <http://tom.preston-werner.com/2009/05/19/the-git-parable.html>

#Types of Tools available

Distributed vs. Centralised
:	Modern VCS (like Git) work on a distributed model (DVCS).
This means that every member of the project team keeps a complete local copy of all the changes, usually called thier private repo.
:The previous model, still widely used with tools like Subversion, is centralised.
There is only one central database with all the changes and team members only have a copy of the change they are currently working on.

##VCS operations using Git

The rest of this course will take an hands on approach by demonstrating the use of Git to manage a simple set of changes.
You should follow along on your own computer using a new test project as explained in the next module.

[Git](http://git-scm.com/) is very popular DVCS originally developed to maintain the GNU/Linux kernel source code
(the operating system that runs on lots of computers and samrtphones)
It is now used by many very large open source projects and a lot of commercial development teams.
