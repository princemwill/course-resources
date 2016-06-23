# Dragon Slaying (Part 2)

## Overview

![its_dangerous](its_dangerous.png)

Your hero probably had some trouble defeating the dragon from [part 1](../01-dragon-slaying-pt1). It's time to suit up your hero.

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Create a new branch off of your `master` branch called `item-shop`
  - [ ] Merge any updates from the `day-2` branch into your `item-shop` branch
- [ ] The `Hero` class
  - [ ] `public void Attack(Dragon opponent, int diceRoll)`
  - [ ] `public void Defend(Dragon opponent, int diceRoll)`
- [ ] The `ShopKeeper` class
  - [ ] `public void Trade(Hero hero)`
  - [ ] `public void BuyMenu(Hero hero)`
  - [ ] `public void SellMenu(Hero hero)`
  - [ ] `public void Buy(Hero hero, int itemIndex)`
  - [ ] `public void Sell(Hero hero, int itemIndex)`


### Stretch Tasks

- [ ] Stock the shop
  - [ ] Add additional items to the ShopKeeper's list of `Wares`
- [ ] UI enhancements
  - [ ] Give better feedback to the user, e.g., how much more gold they need to buy an item
  - [ ] Use colors to improve the console interface
  - [ ] Put the stats of the Hero and the Dragon side by side as the `Battle` rages on
- [ ] Multiple enemies (_!!!_)
  - [ ] Modify the `Battle` method to take a `List` of enemies and fight multiple dragons
  - [ ] Give the user a choice of which enemy to attack each turn

## Details

Well, we found yesterday our hero was not ready to fight a dragon. We skipped an important step: getting ready!

A hero must equip him/herself. In the case of this program, this will involve stopping at a shop and buying/selling items, all of which have various impacts on the battle.

First, you should bring in some changes from the `day-2` branch. Git has a helpful command `git merge` that lets us combine edits from multiple branches of code.

Perform the merge with the following command in your git shell:

```
git merge origin/day-2
```

If it's successful, you'll see something like this:

```
Auto-merging DragonSlaying/Hero.cs
Merge made by the 'recursive' strategy.
 DragonSlaying/DragonSlaying.csproj |  2 +
 DragonSlaying/Hero.cs              |  9 ++++-
 DragonSlaying/Item.cs              | 33 +++++++++++++++
 DragonSlaying/Program.cs           | 61 +++++++++++++++++++++++++++-
 DragonSlaying/ShopKeeper.cs        | 82 ++++++++++++++++++++++++++++++++++++++
 5 files changed, 184 insertions(+), 3 deletions(-)
 create mode 100644 DragonSlaying/Item.cs
 create mode 100644 DragonSlaying/ShopKeeper.cs
```

If it failed, you'll see an error message.

After the merge, `Program.cs` will now use the `ShopKeeper` class to handle some trading before the battle begins.

You will need to write the bulk of the `ShopKeeper` class. You should be able to run your program without it, but you will likely find that the hero simply cannot win without getting some new items in the inventory (or some rearrangement of the starting stats).

The `Inventory` is a list of `Item` objects, all of which have some effects that may or may not impact the battle. If an `Item` has a `Defense` effect, for instance, then it will impact the Hero's ability to defend. If it has an `Offense` effect, then it will impact the Hero's ability to attack. Any other effects are ignored at this point.

The `Effects` object is stored as a `Dictionary`. You will need to determine if each item is applicable to the action taking place, and apply its effect if so.

You will need to make updates to the `Hero` class to take into account the contents of the `Inventory` for both the `Attack` and `Defend` phases. The specific calculations are described in the comments preceding each method.


## Hints

As usual, focus on just one part of the project at a time. Start by making sure you understand the concept of the inventory and an `Item` object and what parts you'll need to interact with. Then think about how you would solve one particular task. Trust that other tasks will be figured out.
