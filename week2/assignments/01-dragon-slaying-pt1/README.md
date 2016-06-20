# Dragon Slaying (Part 1)

## Overview

Heroes need to slay dragons. It's what they do.

Coders need to write code so that heroes can slay dragons. It's what you'll do!

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Create a fork of the [dragon-slaying](https://github.com/wcci-summer-2016/dragon-slaying) repository and clone the fork onto your machine.
  - [ ] Create a README.md file explaining what this project will involve and how someone could run it.
- [ ] The `Die` class
  - [ ] `public Die(int NumberOfSides)`
  - [ ] `public int Roll()`
- [ ] The `Dragon` class
  - [ ] `public bool IsAlive()`
- [ ] The `Hero` class
  - [ ] Add any necessary field(s)
  - [ ] `public int HitPoints` `get` and `set` methods
  - [ ] `public override string ToString()`
  - [ ] `public bool IsAlive()`
  - [ ] `public void Attack(Dragon opponent, int diceRoll)`
  - [ ] `public void Defend(Dragon opponent, int diceRoll)`


### Stretch Tasks

- [ ] UI enhancements
  - [ ] Give better feedback to the user during the `Battle`
  - [ ] Use colors to improve the console interface
  - [ ] Put the stats of the Hero and the Dragon side by side as the `Battle` rages on
- [ ] Multiple enemies (_!!!_)
  - [ ] Modify the `Battle` method to take a `List` of enemies and fight multiple dragons
  - [ ] Give the user a choice of which enemy to attack each turn

### Stretch Armstrong Tasks

- [ ] Give the user the ability to decide what to do on each turn (e.g., attack/defend). Decide on some logic to determine the results of each decision.

## Details

Dragons must be slain on every [hero's journey](https://en.wikipedia.org/wiki/Monomyth), whether they are literal dragons or metaphorical ones. In this assignment, you're going to write parts of the code that will allow a battle of epic proportions to take place.

As it is right now, though, a lot of important pieces are missing. You must fill in the missing sections (noted above and marked `TODO` in the provided code) so that the battle can take place as planned.

For part 1 of this assignment, you will be focusing on the battle process.

Battles in this program will take place by alternating between a hero attacking and a dragon attacking. There is some simple math that determines how much an attack damages an opponent, with a little randomness factored in from a virtual [20-sided die](https://en.wikipedia.org/wiki/Dice#Polyhedral_dice). Once either the hero or the dragon has 0 HitPoints, the battle is over and the winner is the one still standing.

You will need to write parts of the `Die` class, which will use a `Random` number generator to generate a number used in the battle.

You will need to write parts of the `Dragon` and `Hero` classes. Most of the battle logic is handled in the `Hero` class. Check the [XML doc](https://msdn.microsoft.com/en-us/library/b2s063f7.aspx) tags for more info about how the logic is supposed to work.

`Program.cs` is set up to run a battle between a hero and a dragon - you may feel free to change any of the stats in this file, but it is not necessary to change anything.


## Hints

You should start by implementing the Die and the methods that throw `NotImplementedException`, as these will prevent your program from running. Next you may want to work on the ToString() method of the Hero class, so you can see how your hero is doing.

I believe it is technically possible to win a battle with the stats as they are set, but it requires a lot of luck or a broken random number generator. To test things out, you may want to modify the stats of the `Hero` or the `Dragon`.

For the secondary task involving displaying the stats side by side, you'll need to do something a little special instead of the usual `Console.WriteLine`. `Console.SetCursorPosition` isn't a bad starting place... Or, you could use a series of `Console.WriteLine` and substitution to get each individual stat. There's more than one way to approach this problem!
