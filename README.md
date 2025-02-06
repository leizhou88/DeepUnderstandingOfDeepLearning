# Deep Understanding Of Deep Learning
Python code accompanying the course "A deep understanding of deep learning (with Python intro)"

Master deep learning in PyTorch using an experimental scientific approach, with lots of examples and practice problems.


See https://www.udemy.com/course/deeplearning_x/?couponCode=202302 for more details, preview videos, and to enroll in the full course.

# Running `pip install` May Get Error in vscode terminal

When Windows Powershell is the scripting language, directly running `pip install mypackage` may fail. The workaround is to use the following: 

```python
python -m pip install requests
```

# IMPORTANT NOTE ON `venv`

After launching vscode, always do the following to make sure proper `venv` is used - even when you open a terminal window: 

1. Open the Command Palette (Ctrl+Shift+P or Cmd+Shift+P on macOS).
1. Search for "Python: Select Interpreter".
1. Select the Python interpreter associated with your virtual environment (e.g., path/to/venv/bin/python or venv\Scripts\python.exe).