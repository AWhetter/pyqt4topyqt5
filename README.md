pyqt4topyqt5
============

A fork of pyqt4topyqt5 to add some additional functionality:
* Can customise the input and output module names.
* Can edit files in place.

## Usage
```bash
// install the tool
python -m venv .venv
.venv/bin/pip install .

pyqt4topyqt5 [-h] [--nosubdir] [--followlinks] [-o O]
             [--diff [DIFF]] [--diffs] [--nolog] [--nopyqt5]
             [--replace IN_MODULE] [--replace-with OUT_MODULE]
             path
```

Basic example: porting the content of `pyqt4app` to pyqt5 in the directory `pyqt5app`:
```bash
pyqt4topyqt5 pyqt4app -o pyqt5app
```

I like to use the following, where I'm moving from PySide to Qt.py
and I want the files to be edited in place:
```bash
.venv/bin/pyqt4topyqt5 --nolog --replace PySide --replace-with Qt src/ -o src/
```
