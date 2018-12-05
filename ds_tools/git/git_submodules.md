# git submodules

### The dangers we face
- Every time you add a submodule, change its remote's URL, or change the referenced commit for it, you demand a manual update by every collaborator
- Forgetting this explicit update can result in silent regressions of the submodule's referenced commit.
- Because lifecycles are separate, updating a submodule inside its container project requires two commits and two pushes.
    - one for the module and another of the submodule

### Helpful commands:
```
# cloning w submodules:
git clone --recursive git@example.org:repo
# or
git clone git@example.org:repo
git submodule init --recursive

# grabbing changes to a submodule
git submodule update --init --recursive

# grabbing updates to a branch
git pull 
git submodule sync --recursive # sync up 
git submodule update --init --recursive #  SUPER IMPORTANT 

# grabbing updates to a submodule
git submodule update --remote
# There is an easier way to do this as well, if you prefer to not manually fetch and merge in the subdirectory. If you run git submodule update --remote, Git will go into your submodules and fetch and update for you.

# Updating a submodule inside your repo
git submodule update --remote --rebase -- path/to/module
cd path/to/module
# Local work, testing, eventually staging
git commit -am "Update to central submodule: blah blah"
git push
cd -
git commit -am "Updated submodule X to: blah blah"

# adding a submodule
git submodule add clone_url folder_name
```

## .gitmodules

#### specifying branch in .gitmodules:

in .gitsubmodules add the branch = 
```
[submodule "lib/net_prep"]
	path = lib/net_prep
	url = https://git.analytics.deloitte.ca/CRISP/pqs-ml-preprocessing
	branch = dev
```

## Resources:
tutorial: https://medium.com/@porteneuve/mastering-git-submodules-34c65e940407
- can scroll down to the bottom for TLDR
cheat sheet: https://www.systutorials.com/5520/git-submodule-cheat-sheet/
- removing submodule: https://stackoverflow.com/questions/1260748/how-do-i-remove-a-submodule