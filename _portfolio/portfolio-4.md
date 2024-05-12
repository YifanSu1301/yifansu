---
title: "Robot Juggling (Continue...)"
excerpt: "In this study, our focus is on maximizing the robots' coverage of the targets."
collection: portfolio
---
## Motivation

This project is mainly inspired by the videos shown in the class 16-299 taught by the professor Chris Atkeson and his previous work. Additionally, I researched many related studies and found that previous attempts at robot juggling generally used something easier to control as the robot's hand, such as a board.

With the development of humanoid robots, there are increasingly more robotic hands similar to human hands. Therefore, I am curious whether it is possible to control a robotic hand similar to a human hand to complete this task.

There are many studies on the interaction between robotic hands and objects, such as grasping, in-hand manipulation, etc. These papers all demonstrate that controlling a robotic hand to interact with objects is a complex task, and these works are trained using model-free Reinforcement Learning (RL).



## Model-free RL

Firstly, the biggest problem encountered is that robot juggling is not as simple as just making a robot stand up. It's difficult to design a universal reward function and then just let the robot learn from it. This task is hard to express with a mathematical formula. Initially, I wanted to use a mathematical formula to express the trajectory of a ball's movement for it to learn from, but ultimately, I found that it would explore many strange actions, such as the way the hand throws the ball.that is different from how humans throw a ball

Therefore, I decided to use curriculum learning, starting with smaller tasks, so that I can control its actions through subtasks. Each subtask would be easier to design a reward function for. For example, having the robot hand first learn to throw a ball upwards, then throw another ball to the other hand, catch it, and then proceed to use both hands...

### Results:
![final_1](/images/portfolio/juggling/final_1.mp4){: .align-left width="400px"}
![final_2](/images/portfolio/juggling/final2.mp4){: .align-left width="400px"}
![final_3](/images/portfolio/juggling/final_3.mp4){: .align-left width="400px"}
![final_4](/images/portfolio/juggling/final_4.mp4){: .align-left width="400px"}

## Learn from demonstration

However, manually designing reward functions is indeed very complex, so we tried to extract useful information from videos to allow the robot to learn from them. The key aspects of juggling are the movements of the hands and the motion of the balls. Therefore, we extracted the movement trajectories of the hands and the balls from juggling videos, and let the robot learn these trajectories to try and replicate the movements in the videos.

### Results:

![ShadowHand](/images/portfolio/juggling/shandowhand.gif)

### Next...

Trying more fun things, will update here...

