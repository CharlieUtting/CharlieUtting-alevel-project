# 2.1 Design Frame

## Systems Diagram

&#x20;

<figure><img src="../.gitbook/assets/Untitled (1) (1).jpg" alt=""><figcaption></figcaption></figure>

This diagram shows the different parts of the game that I will focus on creating. I have split each section into smaller sub-sections. Throughout the development stage, I will pick one or two of these sections to focus on at a time to gradually build up and piece together the game. I have broken the project down this way as it roughly corresponds to the success criteria.

## Usability Features

Usability is an important aspect to my game as I want it to be accessible to all. There are 5 key points of usability to create the best user experience that I will be focusing on when developing my project. These are:

### Effective

For my game to be affective the game needs to be simple but with some level of difficulty. This will mean that collecting items and upgrading will have to be very simple. It will also have to a simple combat system which will just consist of shooting at the enemies and if the enemies collide with you then they will take away your health.

#### Aims

* You are able to upgrade your weapon.
* The materials you collect stand out.
* The UI showing how much of a material you have and how much you need to upgrade will be has to be displayed clearly.

### Efficiency

The speed and accuracy to which a user can complete the goal. To do this I will both have an easy menu to save a game and to load a game and I will need an intuitive control system so that the game is easy to pick up and understand what your objectives are.

#### Aims

* Create a menu system that is quick and easy to navigate through
* Create a controls system that isn't too complicated but allows the player to do multiple actions.
* Have a clear explanation of the aim at the beginning of the game.

### Engaging

The solution is engaging for the user to use. To do this the game will primarily be difficult so the player will have more determination to finish it and it will have five roads that will act as levels and will have a clear difficultly increase. The game will also be more engaging if it has a darker theme as this will increase the fear and adrenaline of the person playing.

#### Aims

* Create a series of roads that will act as levels to work through
* Incorporate a style of game art the suits the theme of the game

### Error Tolerant

The solution should have as few errors as possible and if one does occur, it should be able to correct itself. To do this, I will write my code to manage as many different game scenarios as possible so that it will not crash when someone is playing it.

#### Aims

* The game doesn't crash
* The game does not contain any bugs that damage the user experience

### Easy To Learn

The solution should be easy to use and not be over complicated. To do this, I will create simple controls for the game. I will make sure that no more controls are added than are needed in order to keep them as simple as possible for the players.

#### Aims

* Create a list of controls for the game
* Create an in-level guide that helps players learn how to play the game

## Pseudocode for the Game

### Pseudocode for game

This is the basic layout of the object to store the details of the game. This will be what is rendered as it will inherit all important code for the scenes.

```
object Game
    type: Phaser
    parent: id of HTML element
    width: width
    height: height
    physics: set up for physics
    scenes: add all menus, levels and other scenes
end object

render Game to HTML web page
```

### Pseudocode for a level

This shows the basic layout of code for a Phaser scene. It shows where each task will be executed.

```
class Level extends Phaser Scene

    procedure preload
        load all sprites and music
    end procedure
    
    procedure create
        start music
        draw background
        create players
        create platforms
        create puzzle elements
        create enemies
        create obstacles
        create finishing position
        create key bindings
    end procedure
    
    procedure update
        handle key presses
        move player
        move interactable objects
        update animations
        check if player at exit
    end procedure
    
end class
```
