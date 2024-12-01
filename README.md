# This is the Fire Emblem Project
Made by Day, Ryu, Noah, Jaimai from class ESC776: Into the complex world

## Introduction
If you have played one of the Fire Emblem games, you might know that the battle mechanic relies not only on strategy but on luck too.

With each battle initiated, HIT, CRIT, and DMG are displayed for you. Even if your character is strong, they might miss an attack--or even get hit by a critical too.

So with the school project task of making Monte-Carlo simulation, a method using a lot of random numbers to simulate, and turn that into statistics, I decided that Fire Emblem is the game I want to use.

This project uses the Monte-Carlo method to simulate battles with characters from Fire Emblem Echoes to find the best class and character.

## Mechanics
![Fire Emblem Project](https://github.com/user-attachments/assets/67c7a00f-cd32-4268-b1c6-6845e735c3e1)

There are many stats in each character (HP, Atk, skill, speed, luck, def, res) combined with their weapons, that are calculated with the opponent's and then turned into the "Battle Stats" that you see when you initiate battle.

With these stats (DMG, HIT, CRIT, SPD) we then simulate these using the battle mechanics from the game.
- A character attacks first
- Roll a number from 1 to 100
- If the number is lower than HIT, then the attack hits
  - Then roll another number, if it is lower than CRIT, then the damage dealt is **three times the DMG**.
  - If it does not CRIT, deal regular amount of damage.
- If the attack did not hit, then it misses and deal 0 damage.

The other character does their attack the same way only if their HP is not at 0 yet.

If the SPEED one character is higher than the other more than 4, they can deal the second attack
