---
title: Python Style Guide
permalink: /editor/python-style-guide
layout: default
---


Should follow PEP 8: https://www.python.org/dev/peps/pep-0008/

Use the tools `yapf` and `pylint` to achieve this.

## Installing yapf:
`pip install yapf`

## Installing pylint
`pip install pylint`

## Running pylint:
`python -m pylint Case.py`

## Running yapf:
`python -m yapf --style pep8 -i Case.py`

## Automatically execute pylint with pep8
https://pypi.org/project/autopep8/#installation

`python -m autopep8 --in-place .\Properties.py`
