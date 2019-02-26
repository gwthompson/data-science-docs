# Pycharm

## Shortcuts (mac)
- shift,shift to search your project
- move between tabs: control + tab 
- move between windows: option + tab
- right click on file -> git -> compare with branch
- right click git -> add to add a file not being observed
- Shift+cmd+A -> search all pycharm commands
- Shift+Shift -> search all files in project (also searches classes and methods)
- Option+O -> search classes and objects
- Mastering PyCharm keyboard shortcuts - Help | PyCharm https://buff.ly/2CCXbzY


## refactoring
- highlight block of code, right click, in pycharm have a refactoring option, in vscode can extract methods and variables
- right click and search for dependencies
- right click and rename (will rename for the whole module)
- cmd + option + L => reformat all code properly


## Additional
- click on error lightbulb to surround with try catch
- changing names: highlight function / class name then select refactor and can rename it and all its usages
- cmd option m to extravt method
- command option l to reformat all code
- when you commit will even give you alerts about erros
- TODOs: https://www.jetbrains.com/help/pycharm/using-todo.html
- see bottom right for what git branch you're on
- get vim idea plugin 
    - > tabs in
- to change the color of your code :) :
    - view -> quick switch theme -> choose your theme
- tutorial (in case you're interested): https://www.jetbrains.com/help/pycharm/quick-start-guide.html
- # TODO 
    - will bold this entire line for you in a special colour for later (#cool)
- setting a virtual env in pycharm:



## Pycharm Professional
this will allow you to run local python scripts from your local pycharm in the docker container or in a vm via ssh!!

install professional version: https://www.jetbrains.com/pycharm/download/#section=windows

    
## Configuring pycharm with docker
- enable docker support in pycharm as detailed here:
    - https://www.jetbrains.com/help/pycharm/docker.html
    - wouldn't worry about the rest of this tutorial past enabling docker support
        - probably easier from cli
- configure docker as remote interpreter
    - ie allow you to run local python scripts in the docker container
    - https://www.jetbrains.com/help/pycharm/using-docker-as-a-remote-interpreter.html


## connecting to vm as a remote interpreter from pycharm
- https://www.jetbrains.com/help/pycharm/configuring-remote-interpreters-via-ssh.html
    - the default might be python 2.7
        - /usr/bin/python => python 2.7
    - instead do /usr/bin/python3.4 for python 3.4
        - or which ever version is in your /user/bin 
- specify the local path to your local workspace and your remote path to the remote workspace
- tools/start ssh session will get you into the command line on the vm too
- be aware about whether you want to copy over your local directory or import a directory from the vm
    - if you don't want to copy your local when creating the remote interpreter be sure not to select the option to do this, unless you first extract the entire folder and store it locally


    

## connecting to a virtualenv on a vm using a remote interp (which is often what we have)
- repeat steps above for connecting into a vm
- **and set the interpreter path inside your virtualenv**
    - like /home/developer/cyber/cyber_env/bin/python3
    - then you'll have all those packages at your disposal
- you can copy over the whole working directory up to the vm when you make the remote interpreter
- or you can not and just deploy the folders you want
    - right click on a folder in pycharm and then select deploy/upload
    - then can run this code from your local pycharm and it will run on the vm for you
- if you're not finding a certain file:
    - can just redo the setup for the remote interp

## Helpful stuff when working in pycharm with remote interpretor
- right click a folder and deploymeny/synchronize to see all the differences between the local and remote folder
    - then can move from one to the other or delete in one or the other
- right click folder/file deployment/upload to to upload into the vm


## conencting to local virtualenv
- https://www.jetbrains.com/help/pycharm/creating-virtual-environment.html
- **and set the interpreter path inside your virtualenv**
    - like /home/developer/cyber/cyber_env/bin/python3
    - then you'll have all those packages at your disposal
- setting python path   
    - https://stackoverflow.com/questions/17198319/how-to-configure-custom-pythonpath-with-vm-and-pycharm
    - never actually got this working though