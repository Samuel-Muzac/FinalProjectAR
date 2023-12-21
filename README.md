# FinalProjectAR
Group Members: Zyan, Sid, Samuel

Instructions on how to play:
Once the project is downloaded into Unity, simply hitting play will allow the project to run.
Using a camera source, have it aimed at the image marker which is the astronaut
From there, the game will be loaded and you’ll be able to play
Using the sliders: vertical for power, 0 to 100; and horizontal for angle, 0° to 360
Where 0 degrees is straight ahead
Once you have the necessary power and angle, hit the shoot button for the ball to move
After you hit shoot and the ball stops, you can hit end turn for the next player to go.
At the end of round 3, the game ends, and the winner is displayed on screen

Implementation struggles:
One of our own goals was to try to enhance the multiplayer element with multi-device functionality. To do this we incorporated photon engine’s PUN2 package. We created the lobby scene which allowed users to create and join lobbies which would then lead to the gameplay scene, with each user being assigned their own player prefab. This did work, however there were some big problems. The first thing we needed to fix was fixing the gameplay for one user when it was the other player's turn. Using check conditions(checking ownership) we were able to fix the button usage until it was the right player’s turn. However, transferring ownership was not working correctly.

The main issue we came across was synchronization between our devices. When we were building our game, two of us were using MacOS and the other was using Windows. At first, there wasn’t much of an issue but when it came to iPhone deployment, that’s when the issues arose; sometimes the game would run smoothly but other times it wouldn’t. We think this was due to the differences in the OS systems.

We tried many solutions to do this from onPhotonSerializeView to using RPCs but were not able to get the synchronization down, especially the opponent's positions. Instead, it was as if two instances of the game were being created. Even the points were not being synchronized. We came to pretty much every office hour and tried to fix this issue using online tutorials, but ultimately after 5 days of working on the multi-device aspect, we had to scrap this feature and revert to a prior version. This is also why some aspects are not as refined as intended as a significant portion of our time went into this multi-device feature. 
