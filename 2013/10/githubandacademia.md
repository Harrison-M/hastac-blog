Hello!  My name is Harrison Massey, and I'm quite proud to be one of the 2014 HASTAC scholars.  There's a lot I want to talk about in regards to open access and open-source software, but something that's been on my mind a lot recently has been the use of [GitHub](https://github.com) in academia.  As the [most-used open source project hosting site in the world][1], GitHub is sure to be a vital component for not only open-source academic software projects, but also for open education initiatives.  Git's distributed architecture and the layer of relatively simple tools provided by GitHub make the website an excellent tool for synchronizing document work amongst many teammates and outside collaborators.

However, despite the features of GitHub that make Git more accessible, there's still a number of conceptual barriers that have to be overcome to use and understand Git:

##Decentralization

Git's decentralized nature makes it an excellent tool for coordinating collaborative editing.  It 1) keeps collaborators from stepping on each others' toes and 2) the hosting service for the "central" repository collaborators are working on can be changed at a moment's notice.  However, for people who are more accustomed to working on the same copy of a document simultaneously (such as on Google Drive or Wikipedia), the processes of working with the distributed architecture can be jarring.

The easiest way to think about this process is to consider how you might perform analog review or annotation of a document.  A friend wants you to edit their paper, so they print off a copy and hand it to you.  You take the copy, bleed red onto the page to indicate changes, then hand the paper back to them.  They can then look at those changes, which have not affected their original document file, and decide which changes they want to include in their original.

Git and GitHub operate in a similar fashion: if I want to change something, I make a copy of it, make the changes, then submit those changes.  The names used for this process in Git, however, are not very intuitive, and a number of intermediary steps are added to this model as well that make the process initially difficult to understand.

##Specialized language

###Repository

A repository is a group of documents that share a folder and revision history.  A single repository might encompass the code files for a single software program or the HTML source for a website.  In Git, a repository is the main target of operation, so most of the actions I'm discussing are applied to whole repositories.

###Forking

When your friend's document gets printed off and handed to you, a "fork" essentially happens.  When you fork a project in GitHub, the entire repository gets copied from the owner's GitHub account to your GitHub account, including the files and the change history.  This allows you to make edits to their files without disrupting anything they are working on.

The process of forking is at the heart of open collaboration on GitHub.  It allows an individual or core team to coordinate closely on a work while still inviting contributions from those outside the team.  It also avoids the need for features like Google Drive's "sharing" access controls, since changes don't automatically affect the original document.

###Cloning

While it is possible to edit text files right on GitHub, I have to "clone" the repository from GitHub to my local machine if I want to use my own text editor or upload other types of files.  This makes a copy of the entire repository, including its change history, on my machine.  This can be difficult to understand at first, especially if you are using one of the GitHub desktop apps.  The apps will show you all of your repositories, making it seem like they are available for editing, when there is actually an additional step to perform before edits can be made.  To extend our previous metaphor, a clone is akin to making a photocopy: you now have a new sheet of paper that you can edit separately.

###Commits

A "commit" is a set of changes made to a repository.  Unlike a change entry in Google Drive or Wikipedia, a commit's changes can span any number of files in the repository.  These commit groupings are purely defined by the user.  When you want to define a commit, you choose ("add") which changes you want to include in a particular commit.  You then add a description, which is used to describe what the group of changes accomplishes.

Unfortunately, our metaphor falls apart a bit at this point.  Imagine, perhaps, that you sit down to edit the paper across multiple sessions and use a differently colored pen each time.  Each color grouping would represent a commit.

###Pushing

Once you have one or more commits on your clone, you can "push" them to GitHub.  This uploads the commits on your machine to the original repository on GitHub that you created the clone from.  In our metaphor, this copies edits from your photocopy to your original printout (let's pretend we have magic ink that can do this).  It's important to note that until you do this, your changes will not appear on GitHub.

If you're using the official GitHub desktop application, this will be labeled as "publish" or "sync."  "Sync" actually downloads the latest version of your repository from GitHub, then uploads your commits to GitHub, but you will likely primarily use the button for uploading.

###Pull Requests

Finally, a "pull request" does exactly what it says on the somewhat strangely-phrased tin: it asks the owner of the repository you forked to include your changes in the original, much like handing a red ink-stained page back to a writer.  This request encapsulates any commits you created yourself along with a name and description for the request, letting the original owner know what the commits accomplish in aggregate.  It's generally a good idea to make a pull request that accomplishes a single task as opposed to several; that way, if the owner likes one change and doesn't like another, it's easier to just include the part they like.

You can create a pull request using the green compare button near the top-left of the repository screen or by pressing the "new pull request" button in the pull request view on a GitHub repository.  You then tell GitHub to "compare across forks," and you select your fork from the "head fork" dropdown.  This compares your copy with the original repository, allowing you to select commits for the request.

###Issues

When you create a pull request, it will also show up as an "issue" on the original repository.  An issue can be anything from a bug report on a software application to discussion question for a document writing team.  Issues are numbered, which allows you to refer to them from commits or other issues using "#" and the issue number (e.g. "#23").  Issues can also be tagged with "labels" such as "bug" or "discussion," which allow you to categorize issues into a versatile set of different purposes.

##Putting it all together

So, to contribute to another person's GitHub repository, you usually follow the following steps:

1. **Fork** the target repository
2. **Clone** your fork of the repository to your computer
3. Make your edits
4. Create a **commit** (or commits) to encapsulate your changes
5. **Push** your changes to your fork on GitHub
6. Create a **pull request** that asks the original owner to include the commits from your fork in their original copy
7. Wait for the repository owner to respond, and conduct any discussion about the pull request in the corresponding **issue**.

It is possible to skip a number of these steps by using GitHub's browser-based text editor.  However, I recommend going through this process at least once before using it.  The online editor uses a lot of this terminology to explain what's going on behind the scenes, which makes the interface confusing if you're unfamiliar with the process.

##When Git might not be the best collaboration system

Git and GitHub are very good tools for asynchronous, open collaboration.  However, if you're trying to run a live editing session or keep your documents private, you may want to choose a different tool.

For live, synchronous editing, you probably want a system with features such as cursor sharing and chat.  Etherpad, Etherpad Lite, and Google Drive are all better for this than GitHub, since changes show up immediately and don't require "commits."

For private editing, you have to pay for a premium GitHub account to have access to private repositories.  Google Drive, Dropbox, and other file sharing services will give you fine-grained access controls for free.  However, it should be noted that GitHub provides [5 private repositories to students for free for two years and offers discounts to educational institutions](https://github.com/edu), so this shouldn't be an absolute deterrent.

It's also worth noting that Git and GitHub have a longer setup time than many other collaborative tools, which is fine if all your collaborators have used it before.  If one or more participants don't have it set up, though, you may want to opt for a speedier option if time is of the essence.

##Git started!

If you're unfamiliar with Git, the easiest way to get started is to sign up on the [GitHub front page](http://github.com) and then download one of the GitHub desktop applications ([Windows](http://windows.github.com/) or [Mac](http://mac.github.com)).  Then, if you are a HASTAC scholar and leave a comment here (or maybe we should start a forum post) with your GitHub username, I have a [GitHub organization](https://github.com/hastac-scholars) set up for us that I'll add you to.

You can also view the [Markdown](http://daringfireball.net/projects/markdown/) file for this post and all my future blog posts in my [hastac-blog](https://github.com/Harrison-M/hastac-blog) repository, where I'm posting them to share the source and solicit corrections to spelling, grammar, and the like.

The terminology surrounding Git and GitHub can be scary and confusing, but once you get used to it, GitHub can become a key part of your collaborative workflow.  The abilities to solicit edits in an organized fashion and conduct discussion through associated "issues" are quite valuable, and the tool is flexible enough to fit a number of collaborative processes.

If any of you are already using GitHub for academic projects, I'd love to hear about it!  I've barely scratched the surface of Git's abilities and uses, so continued discussion would be great.

##Further reading

These links have been pulled from the reading list from [Kim Knight's Fall 2013 Fashioning Circuits class](http://fashioningcircuits.com/?page_id=1436).

* ["A Gentle Introduction to Version Control" by Julie Meloni](http://chronicle.com/blogs/profhacker/a-gentle-introduction-to-version-control/23064)

* Konrad Lawson's GitHub guides:

*   * ["Getting Started with a GitHub repository"](http://chronicle.com/blogs/profhacker/getting-started-with-a-github-repository/47393)
    * ["Direct Editing and Zen Mode in GitHub"](http://chronicle.com/blogs/profhacker/direct-editing-and-zen-mode-in-github/47497)
    * ["Forks and Pull Requests in GitHub"](http://chronicle.com/blogs/profhacker/forks-and-pull-requests-in-github/47753)
    * ["Files and Repository History in GitHub"](http://chronicle.com/blogs/profhacker/file-and-repository-history-in-github/48047)

* ["Git Basics" from *Pro Git* by Scott Chacon](http://git-scm.com/book/en/Getting-Started-Git-Basics)

[1]: http://readwrite.com/2011/06/02/github-has-passed-sourceforge "Github Has Surpassed Sourceforge and Google Code in Popularity"
