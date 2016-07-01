# Rock Paper Scissors

## Overview

Write some "bots" that can play Rock Paper Scissors.

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Fork the [rock-paper-scissors](https://github.com/wcci-summer-2016/rock-paper-scissors) repository
  - [ ] Create a README.md file explaining what this project will involve
- [ ] `RandomAI` (we will write this in class)
- [ ] `StubbornAI` class
  - [ ] Implement `IPlayer`
  - [ ] Make a constructor that takes one parameter: `favoriteMove`
  - [ ] `NextMove()` always plays favoriteMove
- [ ] `ShortAttentionSpanAI` class
  - [ ] Implement `IPlayer`
  - [ ] `NextMove()` plays the move that would win against the opponent's previous move
  - [ ] `SaveResult()` does something with the passed-in values to make `NextMove` work

### Stretch Tasks

- [ ] Develop a more sophisticated AI
- [ ] Fancier UI

## Details

In this project, you'll be focusing on the logic involved in making "artificial intelligence" as it applies to the game [Rock Paper Scissors](https://en.wikipedia.org/wiki/Rock-paper-scissors). Initially, you'll make some very simple bots, and then you'll scale up to more complex ones.

The starter code is set up to give you a framework for playing games against AI classes that implement the `IPlayer` interface. This interface requires two methods: `NextMove` and `SaveResult`.

`NextMove` is used to get the next move for a new round of Rock-Paper-Scissors. This interface uses numbers to represent the various choices: `0` for rock, `1` for paper, and `2` for scissors.

`SaveResult` is called after each round, and can be used to have your AI classes "learn" from previous matches. It's also possible to simply ignore the result - in this case, you still need to implement `SaveResult`, but you can just have an empty method.

We will develop the `RandomAI` class as a group to discuss how to implement the `IPlayer` interface.

The `StubbornAI` class is meant to pick a favorite move, and always play that move. You will need to write a constructor for it to specify which move it should always play, then the `NextMove` method should always return that move. `SaveResult` can be blank for this class.

The `ShortAttentionSpanAI` class will need to do something in `SaveResult` to keep track of moves as it sees them. Once it has seen a move, it assumes that a player will play the same move again, and for its next move picks the move that will beat that move. For example, if it sees **Rock**, it picks **Paper** as its next move (because **Paper** beats **Rock**).

The `ShortAttentionSpanAI` should very quickly win against the `StubbornAI`. You can test this for yourself by adding the AI classes into the `AIPlayers` dictionary in the `Program` class, running the program, and choosing the `AI vs AI` menu option.


### Stretch Tasks

Develop a more sophisticated AI class (or classes). Pit them against each other to see who's victorious!

The UI could also use some work - right now it's very barebones.

## Hints

If you're tackling the stretch tasks, you may want to check out this New York Times article for some inspiration about how you could make a better AI:
http://www.nytimes.com/interactive/science/rock-paper-scissors.html?_r=0

A slightly simpler idea might be to assume that your opponent will do the equivalent of the `ShortAttentionSpanAI` (as in, they might expect you to play the same thing twice), and pick the thing that would beat them. This starts to remind me of the [Battle of Wits](https://www.youtube.com/watch?v=i6TQ7ljcsjk) scene from _The Princess Bride_, though.
