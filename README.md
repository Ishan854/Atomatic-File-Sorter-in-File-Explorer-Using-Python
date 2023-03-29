# Atomatic-File-Sorter-in-File-Explorer-Using-Python
This is a python program for sorting files.  Keep the files you wants to sort in Download folder. After running the program, it will move the files from Download folder to the folders Applications, Codes, Images, Others, Sounds, Text, Videos depends on the type of file.
Step 1: Install the Modules
To automate the file sorting you need only two modules:

OS module
The OS module in Python provides functions for interacting with the operating system. OS comes under Python's standard utility modules. The *os* and *os. path* modules include many functions to interact with the file system.

To install the os module:

Go to VS code and open the terminal and type the following:

(you can also use command prompt or powershell)

pip install os-sys


Shutil module
The shutil module offers a number of high-level operations on files and collections of files. In particular, functions are provided which support file copying and removal.

To install the shutil module:

type the following code:

pip install pytest-shutil

Step 2: Lets Start Codding!!

1. Import the modules

-->import os,shutil

Define the path to directory
#Write the name of the directory here eg downloads path = '/path/to/directory'
-->path = r'C:/Users/RABINDRA SRIVASTAVA/Desktop/Data Analysis/Python Practice/'

Create a list of all the filename

-->file_name = os.listdir(path)
-->folder_names = ['csv files', 'image files','python files', 'txt files']

Add for loop to check all the files

-->for loop in range(0,4):
    if not os.path.exists(path + folder_names[loop]):
        os.mkdir(path + folder_names[loop])
        
Create a new folder if there is new type of extension and move the files

-->for file in file_name: 
    if ".csv" in file and not os.path.exists(path + "'csv files/'" + file):
        shutil.move(path + file, path + "csv files/"+file)
    elif ".jpg" in file and not os.path.exists(path + "'image files/'" + file):
        shutil.move(path + file, path + "image files/"+file)
    elif ".ipynb" in file and not os.path.exists(path + "'python files/'" + file):
        shutil.move(path + file, path + "python files/"+file)
    elif ".txt" in file and not os.path.exists(path + "'txt files/'" + file):
        shutil.move(path + file, path + "txt files/"+file)
else:
    print("There are files in this path that do not exist")
    
Step 3: The Final Code

-->import os,shutil
path = r'C:/Users/RABINDRA SRIVASTAVA/Desktop/Data Analysis/Python Practice/'
file_name = os.listdir(path)
folder_names = ['csv files', 'image files','python files', 'txt files']
for loop in range(0,4):
    if not os.path.exists(path + folder_names[loop]):
        os.mkdir(path + folder_names[loop])
for file in file_name: 
    if ".csv" in file and not os.path.exists(path + "'csv files/'" + file):
        shutil.move(path + file, path + "csv files/"+file)
    elif ".jpg" in file and not os.path.exists(path + "'image files/'" + file):
        shutil.move(path + file, path + "image files/"+file)
    elif ".ipynb" in file and not os.path.exists(path + "'python files/'" + file):
        shutil.move(path + file, path + "python files/"+file)
    elif ".txt" in file and not os.path.exists(path + "'txt files/'" + file):
        shutil.move(path + file, path + "txt files/"+file)
else:
    print("There are files in this path that do not exist")                           
