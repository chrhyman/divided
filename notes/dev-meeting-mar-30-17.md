# Meeting information

__Date__: March 30, 2017
__Attendees__: Chris, Corey, Ryan
__Secretary__: Chris
__Summary__:
- [x] Visualizing the game board
- [x] Tile flipping (Resource depletion)
- [ ] Movement cost
- [ ] Multiple houses on one resource tile
- [x] Buildings contributing to incidents
- [ ] a
- [ ] a

# Topics

These sections flesh out topics discussed in meetings and notes.

## Game board

We talked more about how we visualize the game board. Our playing area is a certain region of the full map. This is important so that the game board doesn't "wrap" from row A to row B, or column 1 to column 6. In playtesting, we mostly felt like this came across as unintuitive. Additionally, it feels like the other side of the board is now actually "far away", improving that aspect of game feel.

## Tile flipping (Resource depletion)

As in the v2.0 rules, a resource tile flips when its resource difficulty exceeds 12 (the highest possible resource roll). "Flipping" should now correspond metaphorically to a resource being depleted, not destroyed. Movement is still allowed to and from this tile. Units and buildings on a tile are not destroyed by the tile flipping. Cost does not change on a flip, but can be further altered by other effects (such as being adjacent to a spawn or depleted resource). Spawns leave a depleted tile.

## Movement cost

We have an open discussion on movement cost. Currently there is no hard-coded maximum movement cost. The theoretical maximum is 18, as that is a perfect roll of three 6s. Should we allow inaccessible tiles? (Think about movement thematically as well.) Keep in mind that there is currently no mechanic to lower movement cost in the game.

## Multiple houses on one resource

We have an open discussion on multiple houses on one resource. From one perspective, games like Catan might make players feel like they _should_ get two resources if they have two houses on a tile. On the other hand, incident rolls represent a player's effect on the planet, and if they get two resources, the tile should count twice, etc.

## Buildings contributing to incidents

Chris raised a question about Barracks contributing to the incident roll. It was clarified that only the building that collects resources, i.e. Houses, will count towards calculating the incident roll. When incident cards target tiles you touch, only count buildings that gather resources (i.e., Houses).

## Other considerations

For brevity, smaller topics are grouped under this heading. These may need further discussion or playtesting in order to resolve.

* Resource gathering in the late game may become tedious, or be more work than its worth. This may depend on the token used to represent the resources, however.
* How is the pacing in resource acquisition?
* How much RNG should there be in tile and cost distribution? There was a thought to include a "beginner" mode that was more balanced than pure randomness.
* Still need to analyze and balance the cost of various structures and units.
* Design issue: it's unfun to update movement and resource counters on each tile. May come down to components.

# Reference: Raw notes

These are my raw notes from during the play session.

- Dinosaur on turn 1 sucks
  - pressure > motivation
- changing movement/resource tiles isn't fun
- start with house -> can you build 4 inf. + the starting builder?
- collapsed tiles - can you walk on them?
- can you move from row A to row D (map wrapping)
  - do tiles affect across the board like that?
- 2 houses on one tile: 2 resources? think Catan (counter: think incident roll)
- barracks contributing to incident roll
  - what about incident card for tiles you touch
- does a building die if all connected tiles flip?
- what happen on a tile flip?
- simplify late-game resource gathering
- analyze resource acquisition (pacing)
- how much RNG should there be in tile distribution and cost distribution?
- number of resources necessary to build various things

# Reference: Dev notes

These are my raw notes from during the dev meeting

- Difficulty ramps with cards building on top of one another, but you can still get fucked
- tile flipping
  - how do we visualize this?
  - what gets destroyed?
    - not buildings
    - doesn't kill units
  - movement effects
    - can still move through depleted resources
    - movement cost stays the same
- movement cost - no cap?
- 2 houses = 2 resources?
- clock for playtesting to eliminate dev time (so we know how long a game is)
- incident cards target tiles you get resources from
- off-board arrows don't affect us, can't warp/move across map (game board is a subset of planet surface)
- resource gathering late-game
- movement and resource costs aren't fun to update
- suggested "beginner" preset with "balanced" tile and cost distribution
