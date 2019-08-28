## Install Python
As a first step, let's focus on getting Python installed and running. I am going to focus on a Windows-targeted installation; if you're using any other OS please see the OS-specific installation instructions [here](https://realpython.com/installing-python/).
For a Windows installation, navigate your browser to the official python [Releases for Windows](https://www.python.org/downloads/windows/) page. Near the top of the page there should be a link to the *Latest Python 3 Release - Python 3.X.X*; click it! The simplest installation method involves downloading the executable installer and merely executing it.
<div style="border:1px solid black">
BRIEF NOTE ON VERSIONS AND ARCHITECTURES

Python is presently operating under version 3 (Python 3), yet still provides downloads and some support for Python 2. There are few linguistic differences between the versions, yet several of the more modern ML packages specifically support Python 3. Please download Python 3 for this tutorial. If you require the legacy Python 2 for any reason, both versions can be installed side-by-side.

Python 3 supports both 32- and 64-bit architectures, yet some of the more important ML packages only support 64-bit. So, let's focus on the 64-bit version.
</div>

## Setting environment variables

Let's make an admission, Windows is stupid.  And it's not just Windows, it's all operating systems! They facilitate you in finding and organizing files and executables on your machine, yet they rarely fix themselves or spontaneously learn things.  This is a long way of saying that we need to manually teach Windows the command we will use to start python (and pip), and what Windows should do with that command.  This is deemed 'setting environmental variables' or adding to a search path. [These](https://datatofish.com/add-python-to-windows-path/) instructions should help you teach Windows how to do what you want.

## Testing Python
Let's quickly verify that python is installed and that the environmental variables are set.  Launch your Command Line, which can be done in Windows by search "CMD" and executing it.
This will give you an "old school" DOS prompt, that black screen that no one under the age of 30 remembers, and no one under 45 remembers how to use. As a good habit, before launching Python, I set the directory to the root, which typically for Windows is the C:\ drive.  This can be done by typing "cd\", meaning change director to nothing.

```console
C:\Users\ross.hoehn>cd\
C:\>
```
After achieving the root directory, and thanks to us setting the environmental variables above, merely typing "python" at the c-prompt will launch the Python environment.  You will immediately be greeted with the version information of your Python install (mine is 3.6.7 and is 64 bit).

```console
C:\>python
Python 3.6.7 (v3.6.7:6ec5cf24b7, Oct 20 2018, 13:35:33) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

You will also know that you are in the Python environment as the prompt at which you type is represented by ">>>".  Now, to install some packages for our project, we cannot do this from the Python environment, so we will need the means to leave the environment.  This command is conveniently "exit()".
```console
>>> exit()
C:\>
```

*close this issue if you correctly installed Python*