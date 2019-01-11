## Why jupyter
- 

## Setup
- apart of anaconda already
- just move to the top of the directory you want, make sure the python path is set and run:
```bash
jupyter notebook
```

## Themes
- to change the theme: https://stackoverflow.com/questions/46510192/how-to-change-the-theme-in-jupyter-notebook
- then hit p, opens up a search bar to seach through all shortcuts

## Virtual Envs
- using a virtaul env with jupyter: https://anbasile.github.io/programming/2017/06/25/jupyter-venv/

## debugging
- if you get frozen see if you can run anything in another cell
    - if not, try to stop the kernel, still not working restart it
- make sure to exit ipdbs before running a cell again
    - notice you'll also need to redefine classes
- save the notebook to see changes in other cells register in your cell

## Shortcuts
- https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/ 
    - l -> shows line numbers on cell
    - b -> new cell below
    - m -> switch to markdown
    - y -> switch to code
    - i -> stop the kernel
    - r -> restart the kernel
    - p -> search all jupyter commands
        - only present in the theme above I think
        - this is really handy to move cells up and down in that theme too
- if you use ``` ``` in a markdown box you can then paste jupyter outputs into it and they'll keep their format

## Helpful Features
- export to html or pdf
    - file -> export
- port to python code
    - file -> export -> python code