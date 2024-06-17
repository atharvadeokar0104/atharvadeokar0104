import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation

# Define the stages of the flower growth
stages = [
    "   @   \n   |   \n\/|\/\n   |   \n   |   \n  / \\  ",
    "   @   \n   |   \n\\/|\\/\\\n   |   \n   |   \n  / \\  ",
    "   @   \n   |   \n\\/|\\/\\\n   |   \n   |   \n /   \\ ",
    "   @   \n   |   \n\\/|\\/\\\n   |   \n   |   \n /   \\ ",
    "   @   \n   |   \n\\/|\\/\\\n   |   \n   |   \n /   \\ ",
]

# Function to update the frame of animation
def update(frame):
    plt.cla()  # Clear the previous frame
    plt.title(f'Flower Evolution Frame {frame}')
    plt.axis('off')
    plt.text(0.5, 0.5, stages[frame], ha='center', va='center', fontsize=12)

# Create a figure
fig = plt.figure()

# Animate the frames
ani = FuncAnimation(fig, update, frames=len(stages), interval=1000, repeat=True)

plt.show()
