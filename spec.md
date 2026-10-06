# Foraging to Factories

This is an incremental / semi-idle survival game, somewhat inspired by Minecraft, and specifically, hardcore/tech modpacks for Minecraft.
The main game loop revolves around the action button. This is one button.
However, you can change what it does by going to a different area (called "Chunk").

There are, besides the explore button: a world view, an inventory, a craft screen, and an action selector.

# The World View
Shows you the world, top-down. You can see the chunks you have explored. Chunks not yet explored, but adjacent (horizontal/vertical, not diagonal) to explored chunks are greyed-out but the biome is visible. The rest of the world is black.
THe world consists of a square grid.
Each chunk has attributes:
- a biome
- buildings/features
- resources
(It might be smart to code the buildings and resources in a similar class, or in separate, im not sure. Since they are both removable/regenerable)

The chunk the player spawns on at the start is ALWAYS an oak forest biome, with as features, an oak forest. Theres always a known adjacent tile which is a plains biome, with as a feature, a wheat field and a river, and an adjacent tile which is a hills biome, with as a feature a coal deposit. 
! However, you don't have to implement this yet. For the prototype, just implement 1 chunk, which is the oak forest, there's no exploring or other chunks yet.

---

You have an action selector, the actions available are dependent on the biome and features of the chunk your in. Actions are always performed on the chunk your in. On a forest biome, for example, at the start, you can simple "forage". This can only give you, at the start, pebbles, flint, and sticks. However, once you have, for example, a sharp flint (crafted from 2 flint), you can also collect wet fiber. A drying rack, made of sticks, (this becomes a building/feature of the chunk) can turn the wet fiber into dry fiber which can be turned into string. Then you can make a flint axe. Now, a new action opens up in the forest: chop wood. This will give you sticks, leaves, thin logs and saplings, etc.

Once you have some thin logs, you can craft a hut (a building). And with some dried fiber, you can craft a straw bed (modifies the hut)  This is where the prototype for now ends.

Pressing the action button (which changes its label based on the selected action) normally takes time. Let's say, exploring usually takes 2 seconds. However, if you have the hut and the straw bed, you can do a sleep action. For the next 5 actions, this gives you "well rested", which boosts your action speed by 20%.