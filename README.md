# Zenith

Zenith is a tool to automate mouse movement for easier gameplay. It utilizies capturing and image processing for best results. It should not be used in actual player vs player games or matches since it creates an unfair advantage over normal players.

# About

Zenith works with only very few FPS games but has a lot of different features to offer. Zenith is made in C++ but the algorithm can also be replicated in Python.
An example code can be found at the bottom of this repository.

# Features

1. Target Priority
   - Nearest
   - Lowest
     
2. FOV
   
3. Speed
   
4. Adjustable for all resolutions

# Installation and Usage

> Based on Python example

1. Install Python 3.11 or higher
   
2. Install necessary packages for screen capturing and image processing
   
3. Create your own file based on the example below or use our given file
   
4. Make sure to name your file `main.py`
   
5. Run the program with Python using the command below
```
py main.py
```

# Optional Adjustments

- You can add CUDA acceleration for faster results if you own a NVIDIA GPU
  
- You can compile your program as an .exe for easier execution

# Important Information

Many games prohibit the usage of scripts in public games or in their game entirely. Before using anything, make sure you are allowed to in the first place, otherwise your access might get restricted.

# TSLynx / Vyper

- Discord: @vyperized
  
- Discord Server: https://discord.gg/gk8424YbDr

# Python Example Code

```py
# necessary imports

FOV = 60
sens = 1.00
speed = 2

screen = [1920, 1080]

screen_center = [screen[0] / 2, screen[1] / 2]

# function to move cursor
def move(x, y):
  # replace with your actual logic
  print("")

while True:
  # here you will need a function to find contours of entities
  # this can be done through contrast or color detection as example
  for entity in entities:
    # fov check
    if abs(x - screen_center[0]) < FOV and abs(y - screen_center[1]) < FOV:
      delta_x = x - screen_center[0]
      delta_y = x - screen_center[1]
      # adjust values to sensitivity
      delta_x = delta_x * 1.00 / sens
      delta_y = delta_y * 1.00 / sens
      # apply speed
      delta_x = delta_x * speed
      delta_y = delta_y * speed
      # move mouse accordingly
      move(delta_x, delta_y)
```
