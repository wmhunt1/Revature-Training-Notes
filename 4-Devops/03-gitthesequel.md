* Git
    * Git is a Distributed version control system
        *  People can have different versions of things
        * Not one source of truth 
    * Git has features that lets you work on multiple versions of a project at the same time
    * With the ability to work on different features at the same time, git also includes features that allows you to communicate any changes you’d want to make to the working version
* Branching
    * It is best practice to have a different branch for any new features you might want to add to the working project 
    * Commands: 
        * git checkout -b <branch-name> 
            * Creates a new branch starting at the current commit
        * git branch <branch-name>
            *  Creates new branch without switching 
        * git checkout <branch-name>
            *  Switch branches freely git push Operates on current branch 
        * git pull origin <branch-name>
            *  Pull from a certain branch (like main)
* Branching Terminology
    * Remote branch 
        * Branch in your remote repository 
    * Local branch 
        * Branch in your local repo Can change origins May not necessarily have a remote counterpart 
    * Tracking branch aka upstream branch
        *  Local branches that have a direct relationship to a remote branch
* Pull Requests
    * Don’t just push to main 
    * When you want to merge a completed feature to the main branch, you create a pull request
    *  With a pull request you are opening any changes you want to commit to main for peer review, and comments from your other team members 
    * Any changes you’ve made on the branch with an open pull request gets added to the pull request
* Merge Conflicts
    * In hell, people who are guilty of git crimes get sentenced to resolve merge conflicts for all eternity using vim
    * What happens when two versions of code are incompatible 
        * The code has been edited at the same point by different people 
        * This is why we pull often 
    * When dealing with merge conflicts, have utmost patience, communication is key