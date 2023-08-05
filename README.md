# SoC-StreetFighter2
This is the repo containing my final project for SoC 2023 by WnCC, IIT Bombay
* For visiting my main repository for SoC 2023 consisting of all
* My final project was to train an RL agent to play the Street Fighter 2 game.
* I have chosen to use Deep Q Learning Algorithm for training my agent with the help of tensorflow to build the neural network.
* Guidelines for running the project:
  - Currently the code(StreetFighterArohanH.ipynb) uploaded in github is for testing the model and the model has been trained for two different initial values of learning rates for several number of epsiodes.
  - The first training period used initial learning rate of 0.005 and it had been trained for 2000 episodes and the second used the value of 0.05 which was for around 400 epsiodes.
  - So for testing the game for the first training period, change the str(self.epsilon) to 1 and str(self.learning_rate) to 0.005 in self.filepath_best and accordingly do the changes for second training period to 1 and 0.05 respectively.
* Conclusions:
  - For the first training period, the agent did not perform at all as the corresponding Q values that the neural network predicted for different actions were same   for all the states(which could be observed visually as the fighter used the same move everytime) which shows that that the neural network didn't train properly which may be due to reasons like overfitting etc.
  - After investigating and discussing with my mentor, I came out with certain possible reasons like very high number of observation space parameters of the environment compared to the number of neural units in the hidden layers etc.
  - For the second training period, I changed certain parameters like initial learning rate, doubled the number of neural units in the hidden layers of the neural network, added dropout layers(for avoiding overfitting) etc. The game showed a little improvement but still the problem of same Q values for different states persisted. I also had a plan to use opencv library of python for decreasing observation space parameters by using techniques such as gray scaling and resizing the environement, but this could not be implemented as the virtual environement that I had used (basically which consisted python 3.6) is not compatible with opencv and hence I could not install it within the virtual environment.
  - This is a project that I would even continue after Seasons of Code by trying out some other techniques like CNN, using opencv(if possible somehow) etc so that I can improve the performance of the RL Agent.
    
  
