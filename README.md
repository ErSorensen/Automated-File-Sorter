# Automated-File-Sorter

import os, shutil

path = r"INSERT PATH HERE"

file_name = os.listdir(path)

folder_names = ['png files', 'jpg files', 'webp files', 'xcf files', 'gif files', 'ini files', 'pdf files']

for loop in range(0,7):
   if not os.path.exists(path + folder_names[loop]):
       print(path + folder_names[loop])
       os.makedirs((path + folder_names[loop]))

for file in file_name:
    if ".png" in file and not os.path.exists(path + "png files/" + file):
        shutil.move(path + file, path + "png files/" + file)
    elif ".jpg" in file and not os.path.exists(path + "jpg files/" + file):
        shutil.move(path + file, path + "jpg files/" + file)
    elif ".webp" in file and not os.path.exists(path + "webp files/" + file):
        shutil.move(path + file, path + "webp files/" + file)
    elif ".xcf" in file and not os.path.exists(path + "xcf files/" + file):
        shutil.move(path + file, path + "xcf files/" + file)
    elif ".pdf" in file and not os.path.exists(path + "pdf files/" + file):
        shutil.move(path + file, path + "pdf files/" + file)
    elif ".gif" in file and not os.path.exists(path + "gif files/" + file):
        shutil.move(path + file, path + "gif files/" + file)
    else: 
        print("There are files in this path that were not moved")

