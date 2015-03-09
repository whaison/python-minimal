The minimal set of python 2.7.6 files needed to run TLSNotary on windows.

Here is how I narrowed down exactly which files are being used:

Download and install https://www.python.org/ftp/python/2.7.6/python-2.7.6.msi on Windows.
Perform a TLSNotary audit but dont quit TLSNotary yet.
In order to know which files in DLLs dir are in use, try to delete them one by one - Windows will warn you if file's in use.
In Lib dir all those files which were used will have corresponding files with .pyc extension 

Note that python.exe opens a console which is not great for UX. Luckily we have console-less python.exe
Delete python.exe and rename pythonw.exe into python.exe when releasing.

