---
layout: default
title: My Hunter
parent: Projects
nav_order: 1
---
[![GitHub Repo](https://img.shields.io/badge/GitHub-Check_the_repository-blue?style=for-the-badge&logo=github)](https://github.com/mathematisse/My_Hunter)
[![Itch.io Page](https://img.shields.io/badge/Itch.io-Download_the_game-red?style=for-the-badge&logo=itch.io)](https://mathematisse.itch.io/My_Hunter)

# My Hunter

My Hunter is an Epitech project made with [CSFML](https://www.sfml-dev.org/download/csfml/).
This project was created with the goal of getting to know that graphical library, while reproducing (with some creative freedom) the [Duck Hunt game](https://fr.wikipedia.org/wiki/Duck_Hunt).

## Installation

**Linux Operating systems ONLY**

You can **[download the game](https://mathematisse.itch.io/My_Hunter)** from itch.io to just get the binary and ressources.

Follow the instructions and launch the game with the following command in the downloaded folder :

``
./my_hunter
``

To build it yourself, you will need to **[download the repository](https://github.com/mathematisse/My_Hunter)** from github.

You'll also need [CSFML](https://www.sfml-dev.org/download/csfml/) installed.

Once this is done, run the following command in the unpacked folder :

``
make && ./my_hunter
``

## Usage

> Ducks are animal, and like us, they poop.
> 
> For some mysterious reasons thousands of ducks started flying just above you.
> 
> You will not be a toilet for ducks.
> 
> Good you have this huge laser-gun.

In this game, your goal is to shoot flying ducks with a laser-gun.

As time pass by, more and more ducks will take-off and start fly around.

When the red bar is filled, it's over, you died intoxicated with guam!

The Orange and Green bars represents the reload and energy storage state of your laser gun.

Move the mouse arround to visualize your target range, and click to shoot a laser beam.

Everytime you kill a duck, you win a credit !

Buy upgrades to survive :
- Plant trees to lower intoxication levels over time
- Construct solar panels to harvest electricity faster
- Lower your laser reload time
- Enlarge your laser range

## Technical Details

Built with CSFML on emacs only. The code is not meant to be re-used, neither maintained. See my csfml lib if you're looking for usable tools.

The ducks are represented by simple structs with minimum amout of informations linked to them.

On each update, the system iterate through all active ducks and use an "image bank" to avoid duplicating data.

Trigonometric functions are used to fastly determine which duck is in range of the laser.

The "Hard" mode spawns more ducks that you can ever kill, but it is a nice showcase of the performances of the game.
