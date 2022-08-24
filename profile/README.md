# The Center for Innovative Design and Analysis GitHub Organization

This is the main GitHub page for the Center for Innovative Design and Analysis (CIDA) at the Colorado School of Public Health (CSPH). 
In order to be invited to CIDA-CSPH, please contact Camille Hochheimer, Ryan Peterson, or Max McGrath.

## How to organize project repositories (PRs)

- Each PR should be nested in Teams [and prefixed by the team name or abbreviation?]
- Each PR should have all subdirectories one would expect for a project: Admin, Background, Code, DataProcessed, DataRaw, Dissemination, and Reports
- Each PR should have a readme.md file
- Each PR should have a .gitignore file which tells Git not to track data and other large binary files

## Useful team resources on Git/GitHub
- TBD 

## Moving projects over from GitLab 

1) On GitHub, navigate to "Create a new repository" [or click here](https://github.com/organizations/CIDA-CSPH/repositories/new)
2) Select "CIDA-CSPH" as the Owner of the new repository
3) Name the folder the same thing as it was in GitLab with a prefix for the branch and an underscore, e.g. for a Pulmonary Branch project called "My_Project", name this "Pulmonary_My_Project"
4) Open a Terminal window (or Rstudio's terminal, window's PowerShell, or Git Bash) 
5) Navigate to your local project repository
6) Pull all changes from GitLab (ensure you are up-to-date)
7) Run the lines below in a terminal to a) add the new remote repository and b) list all remote repositories 

```
git remote set-url --add origin https://github.com/CIDA-CSPH/Pulmonary_My_Project
git remote get-url --all origin
```

8) Run the line below to delete the existing GitLab repository (copying the GitLab URL from the previous step)

```
git remote set-url --delete origin http://cidagitlab.ucdenver.pvt/pulmonary_temp/My_Project.git
```

9) Run the following to push to the new GitHub repo

```
git branch -M main
git push -u origin main
```

10) Add the remote repository to its proper GitHub Team by either a) going to the team's page -> repositories -> add repository or b) going to the repo's main page and going to settings -> Collaborators and teams -> Add teams 