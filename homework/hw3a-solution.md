# HW3A Solution - Git and Version Control

## Part 1: Repository Cloning

I successfully cloned the class repository from `https://github.com/olearydj/INSY6500` to `~/insy6500/class_repo`.

### Key Commands Used

- `git clone <url>` - Create local copy of remote repository
- `git log` - View commit history
- `git remote -v` - Check remote repository connections
- `git status` - Check status of repository compared to main branch
- `git commit -m` - Commit changes with message

## Part 2: Portfolio Repository Creation

I created my personal course repository with:

- Professional README.md describing the project
- Proper .gitignore to exclude unnecessary files
- Organized directory structure for homework, projects, and notes

### Understanding Git Workflow

The three-stage workflow:

1. Working Directory: Where I edit files
2. Staging Area: Where I prepare commits with `git add`
3. Repository: Where commits are permanently stored with `git commit`

## Part 3: GitHub Publishing

Successfully published repository to GitHub:

- Used `git remote add origin` to connect local repo to GitHub
- Used `git push -u origin main` to upload commits
- Verified all files and commits are visible on GitHub

### The Remote Connection

My local repository is now connected to GitHub:

- `git remote -v` shows the remote URL
- `git push` will send my commits to GitHub
- `git pull` will get updates from GitHub (if changes are made on GitHub)

### Details

Complete this section with details from your setup:

- Repository URL: https://github.com/mattressdog/py4eda-work
- Output of `git remote -v`:
origin  https://github.com/mattressdog/py4eda-work.git (fetch)
origin  https://github.com/mattressdog/py4eda-work.git (push)
- The output of `git log --oneline`:
14ac47b (HEAD -> main, origin/main) Add hw3a solution document
09f43fb Initial commit: Add README and .gitignore

## Questions

### Reflections

#### Question 1: Git Workflow Benefits

You've now experienced the basic Git workflow: edit files, stage changes, commit with messages, and push to GitHub.

a) Before this assignment, how did you typically manage different versions of your work (e.g., assignments, code, documents)? Compare that approach to using Git. What are 2-3 specific advantages Git provides?

Admittedly, most of the coursework I have done to date has not needed or required version control. I find version control tools to be used for software applications rather than academic research and report writing. 
A key advantage to git is, if hosting in multiple locations, it can be a great way to safeguard important documents. As Dr. O'Leary said in lecture, Git makes it difficult to lose data via its many tools used to back up different versions. 
Git also keeps a log of how many additions (or editions for that matter) there have been. It is a great resource for understanding how a file has developed throughout its history. 
Some of the built-in tools are also very important to the overall development process for any document or file, especially the diff tool. Diff allows the user to see changes made to the file by comparing between two commits. 
Git developer have made the Diff tool much easier to use than it was when I began using Git in 2013 and I am very thankful for that. 

b) Describe a situation from your academic or professional work where Git's commit history would have been valuable. What problem would it have solved?
I am one of the poor souls who shamefully rm -rf an entire section of a work directory. With the help of git, I would have been able to restore most of that work. Any work unrestored is work not pushed to the branch. 
In another case, my team was doing a research project using custom software that was being actively developed (but unfortunately not tested). We were able to identify which commits in the git commit history worked for our research without issue.  

#### Question 2: Repository Organization

You now work with two repositories that serve different purposes:

- `class_repo` - cloned from the instructor, read-only reference
- `my_repo` - your own work, pushed to GitHub

a) Explain why it's important to keep these separate. What would happen if you tried to put everything in one repository?
It is very important, even in a world with version control software, to keep original copies of documents and files. The main reason to keep the two repositories separate is to have a clear barrier between who did what work. 
`my_repo` is for work that I complete. in this case, the class repo is for work the professor has completed and is presenting. These naturally belong in separate categories and thus should be in separate repos.  

b) Think about your future coursework or projects. Describe how you might organize multiple repositories. For example, how would you handle a group project versus individual assignments versus reference materials?
For future work, I would likely have different repositories in the same way one needs different environments for separate projects using conda. Each project requires different dependencies, and also could have different permissions settings for group member access.
I envision reference materials being in a different repo likely one that is read only like the class_repo in this case. Individual assignments would be housed in an overall class repository like my_repo but that would depend on how different each assignment is.  

#### Question 3: Commit Messages and History

Look at the commit messages you wrote during this assignment (use `git log --oneline` if needed).

a) Compare these two commit messages:

   - "update"
   - "Add hw3a solution documenting Git workflow and repository structure"
   
   Which is more useful? Why? When might you need to find this commit again in the future?
   
   It is obvious that the second commit message is more useful than the first. I admit I have been lazy at some points in my professional career and have omitted useful information from some commit messages to save time. This has not yet come back to haunt me but perhaps it never will with the skills gained in this class. 
   This is a great message because I may want to follow the procedure of setting up a git repository like this in the future and I need to see the process again. I could also want to see the state of this document before 2025 me stained it with these disagreeable-at-best answers. 
   
   
If you would like to learn more about best practices for these important messages, you might be interested in:

- The [Conventional Commits specification](https://www.conventionalcommits.org/en/v1.0.0/) - a popular convention where commits start with prefixes like `feat:`, `fix:`, `docs:` to enable automation
- [How to Write a Git Commit Message](https://cbea.ms/git-commit/) - a comprehensive guide to writing effective commit messages

b) Imagine you're working on a data analysis project over several weeks. Describe how you would decide when to make a commit. What makes a good "unit of work" for a single commit?
In my opinion, I like to commit work between states of software brokenness and repair. By this I mean, in order to add features to the project, the code doesn't work until the feature is in a workable state. This does not always work out. 
There are often times where the length of time between workable states is days or a week. I would then commit changes before leaving my workstation for a period of time. I have not yet come across a good guideline for how often commits should be done, but I'm open to suggestions. 
I am aware that I'm not supposed to push broken code to master. I would NEVER do a thing like that ;-)

### Understanding Git Concepts (10 points, Graduate Only)

Graduate students: Add a sub-section titled "### Graduate Questions" with concise answers to the following:

#### Question 1: The Three-Stage Model

Git uses three stages: Working Directory → Staging Area → Repository. Many version control systems skip the staging area and commit all changes directly.

Without a staging area, you'd have to commit everything at once with a message like "various updates" - making it hard to understand your history later. The staging area lets you **review and organize** your changes before committing, creating a clean, understandable history where each commit represents one logical change.

a) Think about the work you did in this assignment. You created README.md, .gitignore, and hw3a-solution.md. Why was it valuable to commit the README and .gitignore together first, then commit hw3a-solution.md separately later? What would have been lost if you'd committed everything at once?

Though I think little would have been lost in this case, but if working on a larger project, sometimes multiple files need changes before a commit can be made. In this case it is important to separate the commits in a staging area so developers can keep track of the commits through the log. 
Because we're developing the skill of writing useful commit messages, staging unrelated files and committing in batches is a good practice for clearly documenting changes made to the repo. 

b) Imagine you're working on a homework assignment over several days. You:
   - Write code to load data
   - Start working on a new analysis function (half-finished)
   - Fix a typo in a comment
   - Update your README
   
   Which of these changes should you commit now, and which should you wait on? Why? How does staging help you make this decision?
   
   In my opinion, any code that is not finished should not be committed unless there are other circumstances involved (someone else fixing my awful code). I would likely commit the README first, and commit the code to load data and typo-in-comment together. 
   My opinion again, but small changes in comments do not always need to be pointed out in commit messages. Staging helps by allowing me to pick and choose which files I want to include on certain commits which is a great feature. It also means that if the load data code is wrong I am not having to go back and update the README as well. 

c) Explain how `git status` helps you make decisions about what to stage and commit. When in your workflow should you use it?

Admittedly, `git status` is the first thing I do to ensure the file I checked is being tracked by git. if I don't see README has changed in my git bash, I check to make sure I'm not in the wrong repo (very sad if I am). 
It also allows me to see which files have changes made so I can sort through which ones need to be included in the desired commit. It's a great tool. 

#### Question 2: Local vs. Remote Repositories

You experienced both local repositories (on your computer) and remote repositories (on GitHub).

a) Git is described as a "distributed" version control system. Based on your experience with `class_repo` and `my_repo`, explain what this means. How is it different from just storing files in Google Drive or Dropbox?

Like the professor said in lecture, Git makes it hard to lose things. If the git repo is set up on different storage devices, any pushed changes that are lost locally can be recovered. In cloud services, though I don't know much about them other than that they are large network storage drives, 
if a file is stored in the cloud and that gets deleted, it cannot be recovered without the help of your friendly NSA. Cloud services also do not version control anything. It's like having an additional storage drive rather than a repository with recovery tools. 

b) You can work on your local repository (`my_repo`) even without an internet connection - making commits, viewing history, etc. Then later you can `git push` to sync with GitHub. Explain why this architecture is valuable for developers. What workflows does it enable?
This allows developers to commit work in smaller chunks and push to the branch in one larger submission. This is valuable so developers can document the changes made to the files separately and to more detail rather than waiting to document changes for each push. It is also valuable to be able to make commits before the code is ready to submit. 
These features are also designed to work in group settings  and in a group development scenario, the repo manager doesn't want to have to approve 20 pushes from one developer. Git can get complicated and these tools sometimes make it more, but often make group development less complicated. 

c) Describe the relationship between `git clone`, `git pull`, and `git push`. Why can you `pull` from `class_repo` but not `push` to it, while your `my_repo` allows both?

As I understand it, git clone is used for the initial pull of a git repo and it established the connection between the original repository and the local clone that is stored on the local machine. the `pull` command is used to update the local repo with the shared repo. 
`git push` then allows a user to push changes (often multiple commits) to the repo if the user has permissions to do so. Permissions limit the users ability to push to class_repo since it is not meant to be totally public. files can be pulled down but cannot be edited and pushed back. my_repo is a public repo where the owner (me) can make changes and push.  

#### Question 3: Professional Portfolio

You've created a public repository on GitHub that will be visible to potential employers or collaborators.

a) Throughout the remainder of this course, you'll add more work to this repository. What should you consider when deciding what to commit? How do you balance showing your work process (including mistakes and iterations) versus presenting polished final products?

I do not concern myself with hiding mistakes I have made. The development process is simply that, a process. I hope to find a balance that allows me to track changes effectively with commit messages without obfuscating the process with too many commits. 
Each product will be made available as a polished final product but will also come with the versions that are unpolished via git. 

b) Your README.md is the first thing people see when they visit your repository. What makes a README effective for a portfolio repository versus a README for an open-source project someone might want to use?

I believe the README is a good way for any observer to understand what is contained in the portfolio. There is no other way a reader would know what code is being provided than if they were to look at the README.  For an open-source project, a README is sometimes treated differently. 
There doesn't appear to be a set standard as to what goes into a project README if basing that on what README's exist. They can contain installation/system requirements, or simply contain credits, or both. either way, the READMEs in these cases serve two distinct purposes. 

c) Reflect on the value of building this public portfolio during your coursework rather than waiting until you're job searching. What habits should you develop now to make this portfolio valuable later?

The value of building a public portfolio is great. As a seasoned engineer, I recall my time job searching out of college in 2013 and many companies misunderstood what technical skills students at that time were graduating with. With a public portfolio, a company can see the level of work a student is capable of. 
The company can then evaluate the candidate based on the quality of work, level of effort, or areas of expertise the candidate may have at the time of consideration. Overall having a public portfolio is a good idea. 
