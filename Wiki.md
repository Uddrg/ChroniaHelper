Woo hoo, guys, here's UnderDragon.

Here's the documentation for ChroniaHelper entity parameters.

Thanks to [Yocto](https://gamebanana.com/members/3170382), the helper is fully expanded with some brand new stuffs!

# Entities

## Advanced Spikes

**Trigger**

If enabled, the spike will turn into a Triggered Spikes.

**Sprite Color**

The color tint to add on the original spike, can be useful to pure color spikes.

**Sprite Rotation**

The rotation to apply on the sprite so that the sprite can be customized directional.

Notice: The hitbox won't rotate with the sprite.

unit: rad. 

*PI rad = 180 degrees*

**Sprite Origin**

The beginning distance the sprite is from the position you placed in Lonn, if "Triggered" option is enabled.

Default value is -4.

Notice: The hitbox won't be affected.

**Single Size**

The distance between each spike sprite. To explain it simpler, in vanilla you can see the spikes being next to each other, that's because the distance between each sprite is 8 px.

**Lerp Move Time**

This option defines how fast and far the spikes move when triggered under "Trigger" mode.

**Touch Delay**

How long it takes to enter "Trigger Delay" when player touches the spikes under "Trigger" mode.

**Trigger Delay**

How long it takes for the spikes to come out when triggered.

**Retract Delay**

How long it takes for the spikes to retract.

**Trigger Flag**

The flag it requires for the player to trigger this spikes.
Which means, you need the flag enabled and touch this spikes to trigger them, otherwise it would remain safe.

**Trigger Lerp Move**

This defines how fast the sprite moves when triggered, and the distance is defined by "Lerp Move Time"

**Retract Flag**

The flag it requires for the spikes to retract.

**Random Texture**

As you may know the texture image can contain variants, if this option is enabled, the entity will pick a random variant of the same texture.

Let's say you have textureA00.png, textureA01.png, textureA02.png.

Then enabling this option will make them appear in game randomly, if disabled, then only TextureA00 would appear.

## Animated Spikes

**Tentacle Sprite**

The sprite of the 'fur'-like thingy in 3a (when the spikes are not triggered)

**Texture Sprite**

The sprite of the 'dust ball'-like thingy in 3a (when the spikes are triggered)

**Tentacle Frame**

The Animation Speed

**Tentacle Mode**

Only Tentacles - When the spikes is triggered, the texture would move up like a normal triggered spike.

TenteaclesAndTexture - When the spikes are triggered, the spikes would change with a texture, like how the dust fur turn into the dust ball in 3a.

**Texture Exteriors**

An array that defines how the texture is distant from the original position.

The format would be *1, 2, 5*

**TextureFrame**

Similar to TentacleFrame.

**textureRotationSpeed**

How fast the sprite rotates.

## Cornerboost Block

## DecreaseRefill

## Seamless Spinner

## Player Indicator Zone

## Player Indicator Zone (Custom)

## Killer Block

## Grouped Killer Block

## Killer Wall

## Omni Zipmover

## Spikes

## No Coyote Time Block

## Refill

## Refill Wall

# Triggers

## Ambience Fade

## Ambience

## Axis Camera Offset

## Bloom Fade

## Bloom

## Fastfall Collider

## Flag Management

### Flag Add

### Flag Carousel Manage

### Flag Carousel

### Flag Choose
To adjust new flags according to the flags you have or don’t have, works like multiple flag-if-flags.
Given format is {[if flags]: [add flags]}, ...
For example {a1: b1}, {a2: b2}, {a3: c1, c2}, {a4, a5: d1}

### Flag Clear

### Flag If

### Flag List

### Flag Random

### Flag Remove

### Flag Replace

### Flag State

### Flag Switch

## Lighting Fade

## Lighting

## Music

## SmoothToOffset Camera

## Sub Pixel

## Teleportation

### Target ID

### Teleport Position

### Teleport Target

# WiP: Migration from [TeraHelper](https://gamebanana.com/mods/481388)
[TeraHelper ](https://gamebanana.com/mods/481388)is an excellent helper that gives some entities their tera types so players can interact with them as if they're in an RPG game, and the tera types are strictly based on Pokemon setups, which is pretty well-known.
However, not everyone gets familiar with the 18 tera types from Pokemon, and personally speaking I don't see a way a mapper can use most of the 18 tera types in one map unless it's a huge puzzle map. So that's why I made a duplicate and changed the tera type settings to make it more... I guess, generally simpler.

The entities are all from TeraHelper, very grateful to the source code the author provided, and they have a [wiki about the mechanics](https://github.com/Higashiii/TeraHelper) they included in the helper.
The mechanics of the attacker and the defenser are not changed, but the tera type system is re-written as follows:

Instead of the original 18 tera types, I only kept 5 of them, which is Fire, Water, Grass, Normal and Ghost.

These attacks will be greatly effective:
Fire to Grass,
Water to Fire,
Grass to Water,

These attacks will be normal:
Any to Normal, vice versa
Fire to Fire,
Water to Water,
Grass to Grass,

These attacks will be not so effective:
Fire to Water,
Water to Grass,
Grass to Fire,

These attacks won't work:
Any to Ghost, vice versa