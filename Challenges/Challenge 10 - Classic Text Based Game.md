# Challenge 10 - Classic Text Based Game
The object of this challenge is to create a classic text based game. This game will manage states using variables, and depending on states, the user will have different actions available to them.

With a state machine, your program will run in an infinite while loop and use an `elif` statement to determine what should be done each loop iteration. As a programmer you will specify states. Users can take different actions depending on the current state, then the loop runs again!

## Mild 🌶️
Create a program that satisfies the following states:

|State|Available Action|
|---|---|
|`bedroom`|`sleep`: Print a message about going to sleep.<br>`go kitchen`: Print a message about going to the kitchen and change the state to `kitchen`.<br>`go bathroom`: Print a message about going to the bathroom and change the state to `bathroom`.|
|`kitchen`|`eat`: Print a message about eating.<br>`go bathroom`: Print a message about going to the bathroom and change the state to `bathroom`.<br>`go bedroom`: Print a message about going to the bedroom and change the state to `bedroom`.|
|`bathroom`|`brush teeth`: Print a message about brushing your teeth.<br>`go bedroom`: Print a message about going to the bedroom and change the state to `bedroom`.<br>`go kitchen`: Print a message about going to the kitchen and change the state to `kitchen`.|

* The program prevents the user from typing invalid values and handles errors appropriately.
* The program only moves forward if input is valid.

## Medium 🌶️🌶️
Create a program that satisfies the following states:

| State     | Available Actions                                                                                                                                                                                                                                                                                                                  |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `village` | `trade`: Print a message about trading goods at the market.<br>`rest`: Print a message about resting by the fountain.<br>`go forest`: Print a message about traveling to the forest and change the state to `forest`.<br>`go castle`: Print a message about traveling to the castle and change the state to `castle`.              |
| `forest`  | `gather herbs`: Print a message about gathering magical herbs.<br>`hunt`: Print a message about tracking a deer.<br>`go village`: Print a message about returning to the village and change the state to `village`.<br>`go dungeon`: Print a message about entering the dungeon and change the state to `dungeon`.                 |
| `castle`  | `talk king`: Print a message about speaking with the king.<br>`train`: Print a message about training with the royal guard.<br>`go village`: Print a message about heading to the village and change the state to `village`.<br>`go dungeon`: Print a message about descending into the dungeon and change the state to `dungeon`. |
| `dungeon` | `fight monster`: Print a message about battling a monster.<br>`open chest`: Print a message about opening a treasure chest.<br>`go forest`: Print a message about escaping to the forest and change the state to `forest`.<br>`go castle`: Print a message about climbing back to the castle and change the state to `castle`.     |

* The program prevents the user from typing invalid values and handles errors appropriately.
* The program only moves forward if input is valid.

## Spicy 🌶️🌶️🌶️
Create a program that satisfies the following states:

| State            | Available Actions                                                                                                                                                                                                                                                                                                                                                             |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bridge`         | `scan sector`: Print a message about scanning nearby space.<br>`issue command`: Print a message about giving orders to the crew.<br>`go engine room`: Print a message about heading to the engine room and change the state to `engine room`.<br>`go cargo bay`: Print a message about heading to the cargo bay and change the state to `cargo bay`.                          |
| `engine room`    | `repair core`: Print a message about repairing the reactor core.<br>`boost power`: Print a message about rerouting power to shields.<br>`go bridge`: Print a message about returning to the bridge and change the state to `bridge`.<br>`go airlock`: Print a message about moving to the airlock and change the state to `airlock`.                                          |
| `cargo bay`      | `inspect crate`: Print a message about inspecting mysterious cargo.<br>`deploy drone`: Print a message about activating a helper drone.<br>`go bridge`: Print a message about returning to the bridge and change the state to `bridge`.<br>`go med bay`: Print a message about heading to the med bay and change the state to `med bay`.                                      |
| `airlock`        | `spacewalk`: Print a message about stepping into space.<br>`calibrate suit`: Print a message about adjusting your space suit systems.<br>`go engine room`: Print a message about returning to the engine room and change the state to `engine room`.<br>`go planet surface`: Print a message about descending to the planet surface and change the state to `planet surface`. |
| `med bay`        | `analyze sample`: Print a message about analyzing an alien sample.<br>`heal crew`: Print a message about treating an injured crew member.<br>`go cargo bay`: Print a message about heading back to the cargo bay and change the state to `cargo bay`.<br>`go bridge`: Print a message about returning to the bridge and change the state to `bridge`.                         |
| `planet surface` | `collect specimen`: Print a message about collecting alien specimens.<br>`build beacon`: Print a message about setting up a signal beacon.<br>`go airlock`: Print a message about returning to the airlock and change the state to `airlock`.<br>`go bridge`: Print a message about traveling back to the bridge and change the state to `bridge`.                            |


* The program prevents the user from typing invalid values and handles errors appropriately.
* The program only moves forward if input is valid.