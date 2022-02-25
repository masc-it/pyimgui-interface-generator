# Generate public interfaces for pyimgui

Missing autocomplete for pyimgui? 

![](https://github.com/masc-it/pyimgui-interface-generator/raw/master/example_autocomplete_vscode.PNG)

## requirements
    pip install -r requirements.txt

## run

    python run.py "your-pyx"

## usage example

The file core.pyx in this repo comes from the pyimgui docking branch. Let's say I want to extract all static and member functions in it:

    python run.py core.pyx

What now?

Copy *imgui.pyi* in your virtual environment root folder.

Note: Reload your IDE so that it correctly recognizes the interface. 

Enjoy your auto-complete :)

## Disclaimers

- The *imgui.pyx* in this repo contains imgui constants too, but this is not implemented in the code (yet) and has to be done manually.
- Private member functions are included (change regex to exclude them)
- This is an early alpha, code is not refactored and bugs might be hiding.