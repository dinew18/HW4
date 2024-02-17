I used this to get certain color RGB values




import pyautogui
from PIL import ImageGrab
import time

def get_mouse_color():
    x, y = pyautogui.position()

    screenshot = ImageGrab.grab()

    rgb_color = screenshot.getpixel((x, y))

    return rgb_color

if __name__ == "__main__":
    try:
        while True:
            color = get_mouse_color()
            print(f"RGB Color at mouse position: {color}")
            time.sleep(1) 
    except KeyboardInterrupt:
        print("Program terminated.")
