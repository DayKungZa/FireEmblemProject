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
  - If it does not CRIT, it deals regular amount of damage.
- If the attack did not hit, it misses and deals 0 damage.

The other character does their attack the same way only if their HP is not at 0 yet.

If the SPEED one character is higher than the other more than 4, they can deal the second attack

## Methodology
- In the class set, we gathered average data of every class, divided them into 3 class levels from the game, and gave them the class weapon accordingly.
- In the character set, we gathered data of every character at their max level and gave them their according class weapon.
- Then we match up all the characters in each set, calculate the pre-battle stats, then simulate the battle mechanics 100 times.
- Each win counts as a point, then we take the sum of all points from every match-up to determine the best character/class.

## Results
These are the best characters and classes.
![Fire Emblem Project](https://github.com/user-attachments/assets/bbc25ff2-d8ef-4621-8072-e65d0afcc860)
![Fire Emblem Project (1)](https://github.com/user-attachments/assets/1f2fef68-4472-4c21-8332-fe008088f441)

