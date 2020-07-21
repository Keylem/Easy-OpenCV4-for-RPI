# Easy-OpenCV4-for-RPI
İn this guide I want to show hou how to install OpenCV4 for python 3 on Raspberry Pi without compiling it from source code.

1-Check if you've installed/tried to install it with "pip list" command.
  If it already exists; delete it with "sudo pip3 uninstall opencv-contrib-python"
  
2-Install some dependencies for OpenCV4
type:

sudo apt-get install libhdf5-dev libhdf5-serial-dev libhdf5-103
sudo apt-get install libqtgui4 libqtwebkit4 libqt4-test
sudo apt-get install libatlas-base-dev
sudo apt-get install libjasper-dev

3-Next, we will update pip so we can install OpenCV without compiling anything.
type "wget https://bootstrap.pypa.io/get-pip.py" to get the update and "sudo python3 get-pip.py" to install the update.

4-And the last thing we'll do is to tell raspberry pi that this library exists. This step is very important and if you don't do, it can't find __init__ file of this library and give an error. to do that on your "home" directory edit .bashrc file.
type:

sudo nano .bashrc

and at this line to the bottom of the ".bashrc" file:

export LD_PRELOAD=/usr/lib/arm-linux-gnueabihf/libatomic.so.1

then, source it with:

source .bashrc

That's it 🥳 you can import it with "import cv2" command and check it's version with "cv2.__version__"




