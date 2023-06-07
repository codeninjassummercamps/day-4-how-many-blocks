# Day 4 How Many Blocks

```template
let blocksPlaced = 0
player.onChat("5", function () {
    blocksPlaced = 0
    agent.teleport(world(7, 0, -5), WEST)
    while (!(agent.detect(AgentDetection.Block, UP))) {
        agent.place(FORWARD)
        agent.move(UP, 1)
        blocksPlaced += 1
        if (blocksPlaced >= 5) {
            break;
        }
    }
})
player.onChat("1", function () {
    agent.teleport(world(-9, 0, -5), WEST)
    for (let index = 0; index < 5; index++) {
        agent.place(FORWARD)
        agent.move(UP, 1)
    }
})
player.onChat("2", function () {
    for (let index = 0; index <= 7; index++) {
        agent.teleport(world(-5, index, -5), WEST)
        agent.place(FORWARD)
    }
})
player.onChat("3", function () {
    agent.teleport(world(-1, 0, -5), WEST)
    while (!(agent.detect(AgentDetection.Block, UP))) {
        agent.place(FORWARD)
        agent.move(UP, 1)
    }
})
player.onChat("4", function () {
    agent.teleport(world(3, 0, -5), WEST)
    for (let index = 0; index <= 3; index++) {
        agent.place(FORWARD)
        agent.move(UP, 1)
        if (index >= 1) {
            break;
        }
    }
})
loops.forever(function () {
    if (agent.getItemCount(1) <= 1) {
        agent.setItem(GRASS, 64, 1)
    }
})

```

## How Many Blocks

Learn about loops and more conditions by guessing how many blocks the agent will place for each chat command!

## How Many Blocks

Look at each of the chat commands and try to guess how tall of a stack the agent will build for each one. Write down your guesses in the in-game book! After you write your guesses, use the chat commands to test!

## Activity Complete!

You did it! Good work! 
