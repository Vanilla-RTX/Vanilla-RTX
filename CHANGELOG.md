# Vanilla RTX Changelog

Below you will find the complete changelog of every Vanilla RTX version, from the earliest changelogs still on record up to the latest release. Newest versions come first. Future versions will be added once an update is released.

Unless a note says otherwise, everything listed applies to all three packs: Vanilla RTX, Vanilla RTX Normals/Opus and is called out where it matters.

A few terms you'll run into:
- **Enhanced option:** an optional subpack that fixes ray tracing bugs in the base game through workarounds. It was called **Experimental** from 1.20.5 to 1.21.50, renamed to **Enhanced** in 1.21.60, and merged into the main pack in 1.21.206.
- **MER / MERS:** the material textures (metalness, emissive, roughness, and later subsurface scattering properties) of a block.
- **Normal maps / Heightmaps:** texture definitions that simulates surface details, like bumps or dents, Vanilla RTX uses Heightmaps and Vanilla RTX Normals/Opus normals, both packs utilize this to carve out the shape of each block to further elevate its character in their own unique way.
- **MCPE-{Bug ID}:** a bug report on Mojang's issue tracker, [Mojira](https://bugs.mojang.com/).

# Table of Contents

- [1.26.34](#12634) – Wilderness Bound
- [1.26.21](#12621) – Ocean atmospheric overhaul, end blocks and coral revamps
- [1.26.20](#12620) – Chaos Cubed game drop, POM, SSS and more...
- [1.26.16](#12616)
- [1.26.15](#12615) – Atmospheric Overhaul continued
- [1.26.13](#12613)
- [1.26.12](#12612) – Tiny Takeover
- [1.22.0](#1220) – Mounts of Mayhem
- [1.21.206](#121206) – Merge Enhanced option
- [1.21.190](#121190)
- [1.21.184](#121184)
- [1.21.180](#121180) – Copper Age game drop
- [1.21.175](#121175)
- [1.21.170](#121170) – Vanilla RTX Tuner preparation
- [1.21.160](#121160) – Chase the Skies
- [1.21.150](#121150) – Reformat
- [1.21.140](#121140) – Education Edition Revamp
- [1.21.130](#121130) – Atmospheric Overhaul continued
- [1.21.120](#121120) – Atmospheric Overhaul continued
- [1.21.110](#121110) – Spring to Life
- [1.21.100](#121100) – Atmospheric Overhaul
- [1.21.90](#12190)
- [1.21.80](#12180)
- [1.21.70](#12170) – Garden Awakens
- [1.21.60](#12160) – Transparency Overhaul
- [1.21.50](#12150) – Bugs, Begone!
- [1.21.40](#12140)
- [1.21.30](#12130)
- [1.21.20](#12120)
- [1.21.10](#12110)
- [1.21.0](#1210) – Tricky Trials
- [1.20.5](#1205) – Autumn's End
- [1.10](#110) – Trails and Tales
- [1.9.0](#190)
- [1.8.0](#180)
- [1.7.8](#178)
- [1.7.7](#177)
- [1.7.6](#176)
- [Pre-1.7.6](#Pre-176)  – Most 2020 to 2022 Changelogs are lost.

> Updates without a title generally comprised incremental improvements and revisions that gradually built up Vanilla RTX's many qualities over time, without focusing on any one central theme or major change.

---

## 1.26.34

*Wilderness Bound game drop, fire rework. Covers everything since the last CurseForge release (1.26.21), including 1.26.22.*

### Changes

- Added full support for all Wilderness Bound blocks, including the entire poplar wood set, straw bed, shelf mushrooms, and more
> Fully hand-made normal maps for Vanilla RTX Normals, heightmaps for Vanilla RTX, and, like always, consistent and well-designed materials throughout.

- Dappled Forest biome now has its very own unique atmosphere with RTX
> A darker atmosphere with mildly blue-shifted colors, to convey its status as a cold biome.

- Reworked Fire and Soul fire (and campfires) emissivity, both now emit significantly more light and produce less noise/firefly effect
> The overwhelming majority of the emissivity now comes from invisible static pixels around the fire texture, as opposed to the constantly shifting colors, which produced noise. At the same time, Soul fire is now significantly weaker compared to regular fire, to further emphasize their Fancy graphics light level differences.

- Updated all campfire/fire MERS with properly animated MERS
> Previously they used a MER based on the average of all stages. This was done in 2021 to work around the fact that animated MERs didn't work, but now they do. Almost every other item that was in the same boat was updated already, fire was left out until today.

- Improved End fog for a purpler, darker atmosphere that matches Fancy graphics brightness and colors as closely as possible
> Distant lights now get purple-shifted, since the fog now produces a strong purple color.

- Improved fog across all 5 Nether biomes, colors are now more accurate to vanilla game/Fancy graphics and each biome's intended theme
> For example, the crimson forest now appears more red, and soul sand valleys appear to scatter more blue light.

- Resolved disparities of MERS between Vanilla RTX Normals and Vanilla RTX
> While this was intentional all along, going forward, maintaining two different, consistent palettes of colors across two packs carried minimal benefit and was more of a thing done for correctness. This just means certain things in Vanilla RTX Normals, and consequently Opus, are going to appear a bit less rough/more glossy than usual. Things like planks, planks on a Crafter, lectern, etc... are impacted.

- Updated the Hay texture based on the most recent update, and updated PBR textures to match the new color texture
- Updated sulfur spike up tip merge texture and MERS to match it
> Mojang had updated a pixel on this texture, so the MERS were updated to match.

- Updated pale oak sapling subsurface scattering to match the style of other saplings, with only the leaves having SSS
- Adjusted Sulfur, Potent Sulfur, and Cinnabar block normal maps to be closer in style to blocks like Calcite
> In effect, you might notice the normal map is ever so slightly less blurry, and mildly stronger.

- Improved cherry shelf normal map and heightmap to better follow its texture (namely, which parts are considered carved-in on the shelf)
- Improved pale oak log side normal map
- Improved mangrove trapdoor heightmap
- Adjusted creaking heart heightmaps
- Adjusted ancient debris side normal map
- Minor revisions to numerous other normal maps/heightmaps, very little visual impact, mostly for the sake of correctness, so they aren't mentioned in the changelogs
- Updated blocks.json schema (1.26.22)
- Updated format version of client biomes to the latest
- Minimum required Minecraft version is now 1.26.50

### Enhancements

- Enhanced all 5 new particles from the Wilderness Bound game drop for ray tracing
- Updated several already-existing particle definitions to include their newer/changed properties from later game updates
- Added poplar door darkening issue workaround (MCPE-121412)

### Known Issues

- Red shrub renders incorrectly
> The MCPE-189266 fix for both red shrub and poplar sapling is applied, but only works for the sapling and not the red shrub at the moment. The reason is unknown, a future update might fix it.

---

## 1.26.21

*Continued atmospheric overhaul (oceans), End and coral revamps.*

### Changes

- Continued the atmospheric overhaul of every Minecraft biome, the following biomes received it in this release:
> Regular ocean biome: now features air similar to plains (default fog), but significantly deeper blue water colors, with the thermocline getting darker much faster as you descend. Lukewarm and warm oceans, and their deep variants, now feature a hotter atmosphere similar to desert (although a lot more mild and beach-like). Water colors have been updated using a more consistent mathematical formula/model for representing vanilla colors with ray tracing.

- Revamped PBR materials of End Stone, End Bricks, and End portal frame
> The green parts of the End portal frame are now considered to be made of Dark Prismarine, and End Stone parts are now consistent with End Stone, featuring more detailed materials.

- Revamped End Stone and End portal frame normal maps, End Stone parts are now consistent and feature detailed hand-drawn normal maps
- Revamped End Stone and End portal frame heightmaps, removed subtle noise on End Bricks (remnants of 2022 placeholder textures)
- Revised purpur block heightmaps, with slightly glossier MERS (purpur is slightly glossier by default now)
- Revamped bedrock block, improved normals and heightmaps
> The heightmap and normals are now in a similar style as stone. MERS now feature semi-ultra rough materials with extremely subtle metalness visible on the brightest parts of bedrock. This manifests itself mostly under the sun/strong lights, bedrock still poses itself as an ultra rough, tough material.

- Revamped all Coral blocks, coral fans, and coral plants (all colors), now consistent, with improved normal maps and heightmaps
> New MERS: alive coral plants now appear more wet than dead corals, in addition to all corals now featuring more detailed surface roughness.

- Blaze rods in brewing stands now blaze harder (appear brighter)
- Decreased campfire smoke and sulfur cave geyser particle opacities

---

## 1.26.20

*Chaos Cubed game drop, subsurface scattering, emissive entities.*

### Changes

- Added complete PBR support for all new Chaos Cubed game drop blocks, including all sulfur blocks, potent sulfur, the cinnabar block set, and sulfur spikes
- Sulfur Caves biome now features a uniquely sulfuric atmosphere, with water colors now closely matching the deep cyan-ish green seen in the vanilla game
- Revamped fog of Deep Dark, Lush Caves, and Dripstone Caves
> Now more appropriate for their 3D-biome status, with water colors now closely resembling that of the vanilla game. Since some of these biomes can generate exposed to the surface similar to sulfur caves, heights have been adjusted accordingly to play well with different terrains.

- Fixed an issue where the air atmosphere would appear exposed if the player/camera was inside a small body of water in caves (e.g. a water pillar)
> This happens because of a Minecraft issue where distance fog applies to air distance as well even if the camera is inside a body of water, in other words, Mojang didn't program it to be independent. This is a workaround that sacrifices faithfulness to the vanilla game in order to resolve a bug. In the End and Nether dimensions, this means standing in water no longer overrides the fixed air fog (which is intended to limit vision to a maximum of 96 blocks away from the player).

- Improved the End dimension sky to appear more purple instead of black
> Also fixed End dimension lighting and addressed unplayability with BetterRTX enabled.

- Added comprehensive subsurface scattering data to all MER files (now migrated to the MERS format)
> This is primarily intended for BetterRTX 1.5+ presets, however, it can show itself in Vibrant Visuals graphics mode as well. In general, thin surfaces such as leaves and foliage, or parts of objects that are supposed to let light through (like the paper parts on a birch trapdoor), now properly support subsurface scattering. A lot of time was dedicated to reviewing every block to ensure they support this new property properly, every block, down to the tiniest details like the thin pixels on a scaffolding, now has subsurface scattering.

- Added emissive texture data to all applicable entities (requires a BetterRTX preset with Emissive Entities enabled), you can download and install BetterRTX through the Vanilla RTX App
> This is separate from the existing glowing eyes enhancements, which are rasterized and do not require BetterRTX. Think of it as an expansion that only kicks in when BetterRTX is installed, with no impact otherwise. Glow squids now glow, and eye textures on ender chests, shooting ghast's mouth/eyes, drowned, blaze, and so many more entities now feature emissive textures.

- Corrected the bee nest front: a single pixel that was supposed to be honey now stands out as honey (PBR materials adjusted accordingly)
> Previously I misinterpreted it as a part of the nest texture.

- Candle wicks now burn brighter
- Sculk tendril changes: revised brightness of the inactive state and improved heightmap seams of the sculk tendril animation
- Added an animated normal map to the Nether portal texture, creating tiny distortions when viewing anything behind it (Vanilla RTX Normals and Opus)
- Baked POM (Parallax Occlusion Mapping) data into normal maps (Vanilla RTX Normals and Opus only)
> Used when an appropriate BetterRTX 1.5+ preset with POM is installed. The POM data is derived from Vanilla RTX's heightmaps at 1/5th of the intensity (this may change later). You may flatten the normal maps via the Vanilla RTX App, which retains the POM data. A future update of the Vanilla RTX App will allow you to adjust the POM intensity, though you could do the same now while building a BetterRTX 1.5+ custom preset.

### Enhancements

- Fixed rendering issues of the Sulfur Cube with ray tracing, for instance the top texture no longer renders as black, and flickering/potential Z-fighting issues are improved
- Improved particles of the sulfur cube and slime mobs' walking animations
- Added a workaround for the XP orb texture bug (MCPE-183629), XP orbs now also glow if using an appropriate BetterRTX preset
- Added a workaround for the hopper minecart texture appearing glitchy (MCPE-241124)
> The model isn't entirely accurate to the vanilla game, the hopper is larger and doesn't have the hopper details towards the bottom. The goal was to hide the glitched texture, and it is convincing enough as a temporary solution until Mojang addresses the issue upstream.

- Revamped particle enhancements for ray tracing, fixed with a new format version for the latest version of the game
> Newly added enhanced particles primarily concern the newer sulfur biome geyser particles, which have been tuned to look better with ray tracing. Older particles have also received a touch up with this release, with more consistent opacities throughout and more particles now appearing more transparent than before, to better blend in with the ray-traced world.

- Removed sun and moon related enhancements
> They had minimal benefit, but made the sun and moon look off, especially with the BetterRTX shader mod applied. Ultimately the tradeoff wasn't worth it.

### Known Issues

- Sulfur cube insides render black if the sulfur cube is submerged underwater while the player camera is not (or the opposite)

---

## 1.26.16

This version was never released publicly, only Opus 1.26.16 was released because it had POM ahead of the others.

---

## 1.26.15

*Biome atmosphere overhaul.*

### Changes

- Overhauled the fog and atmosphere of the following biomes, they no longer feature generic fog
> Every biome touched in this update now features its own unique water color, and underwater visibility now closely resembles Fancy graphics.
> - Meadow: now appears as a tiny bit colder variation of the plains biome
> - Beach: now appears similar to a significantly weakened desert
> - Stony Beach: a lot like the plains biome, temperate, but the water color now closely resembles the vanilla one
> - Birch Forest, Birch Forest Hills, Birch Forest Hills Mutated, Birch Forest Mutated: birch forests now generally tend to look cooler and brighter than regular forests
> - Roofed Forest, Roofed Forest Mutated: dark oak forests now generally tend to have a slightly greener and darker atmosphere
> - Mushroom Island, Mushroom Island Shore: mushroom islands now tend to have a purpler, more blue atmosphere, especially during rain

---

## 1.26.13

*Shelf blocks.*

### Changes

- Added full PBR support for Shelf blocks
> Fully consistent heightmaps and MERs with prior stripped wooden items. Comes with all new hand-drawn normal maps full of intricate details (drawing these took a lot of time). Initially, shelf blocks didn't support PBR, so support wasn't added in the update intended for the Copper Age game drop. Mojang enabled PBR on these blocks later.

### Enhancements

- Fixed baby villager geometry

---

## 1.26.12

*Tiny Takeover game drop and a huge quality update months in the making.*

This is a huge quality update, touching up on various blocks and items that were below the level of standard/craftsmanship Vanilla RTX strives for. It also brings full support for Minecraft's Tiny Takeover game drop, with various fixes to previous enhancements that stopped working in more recent Minecraft versions.

### Changes

- Revamped the appearance of glazed terracotta blocks
> New flavorful MERs and improved heightmaps. A normal map rework is planned for a future update.

- Revamped the appearance of Concrete blocks, now more consistent across different colors, with more interesting roughness properties
- Revamped the appearance of Concrete powder blocks, with a style that now matches up with other sand blocks
- New jigsaw and structure block normal maps, improved MERs, metal parts are now more metallic and less rough overall
- Improved coal block normal map and other coal materials
- Fully revamped cobblestone and mossy cobblestone
> This was done with a new layered approach to defining each pebble/rock (similar to how cobbled deepslate or rough ore blocks were previously reworked). Additionally, fixed a disparity of MERs between Vanilla RTX and Vanilla RTX Normals, this will be ongoing as previously intentional MER disparities will slowly be eliminated.

- Updated Stone, Stone Ores, as well as all stone parts on other textures (like on the stonecutter and grindstone) to have fully consistent MERs with finer details
- Revamped reinforced deepslate heightmaps, with more detailed hand-drawn normal maps
- Revamped heightmaps and normal maps of Deepslate and all deepslate parts on ores, as well as reinforced deepslate's deepslate parts
> Now with a style much more akin to the Stone heightmaps, which were reworked a few updates ago.

- Revamped chiseled deepslate materials to better match the style of other chiseled blocks
- Lapis block and lapis parts on lapis ores are now a bit less rough, to better convey their real world appearance
- Improved cracked deepslate tiles and bricks materials by more consistently defining which parts are considered cracks and part of the mortar
- Reworked all ore normals (stone and deepslate types), ore parts on ore textures no longer appear indented and instead appear to stick out!
> This is a new unique design where the idea is that towards the ore itself, the texture seems to bend down, but on the ore parts it appears to stick out instead.

- Added PBR support for the Golden Dandelion, consistent with gold, and fixed its cross-shape rendering error (MCPE-189266)
- Updated the stripped spruce log texture to match the 26.0+ texture (this was a color texture change, PBR texture updates were not needed)
- Minor adjustments to various other materials
> For example, stonebrick's mossy parts on its mortar are now consistent with how mosses on the mortar parts of mossy cobblestone are treated. There have been many similar minor changes throughout the materials to improve their appearance and consistency.

### Enhancements

- Updated the Golem eyes workaround, fixed the missing leash position in the model
- Updated the cat invisible shadow bug fix to properly include the new baby cats introduced with the latest game drop
- Updated the Mooshroom's missing mushroom workaround, no longer breaks baby Mooshrooms
- Fixed cloth rendering issues of baby villagers, the villager workaround no longer causes baby villagers to appear as adults (the same was done for zombie villagers)
- Enhanced the new mob growth, mob pause, and growth reset particles similar to other enhanced particles for RTX

### Opus Only

- The normal layer derived from Vanilla RTX's heightmaps has been significantly adjusted
> The resolution has been cut in half (192x to 96x), normal edge thickness remains the same, and a few new filters and passes were added to more closely recreate the pre-2021 appearance of heightmaps in Minecraft, resulting in a cleaner, more pronounced look with fewer chaotic areas.

---

## 1.22.0

*Mounts of Mayhem.*

Minor update targeting Minecraft's Mounts of Mayhem update. [View the commit](https://github.com/Cubeir/Vanilla-RTX/commit/4ef900790efaeff85c90411903d5067d1a890328).

---

## 1.21.206

*The end of the separate Enhanced option.*

### Changes

- Fixed size mismatch of the stonecutter saw MER compared to its color texture
- Fixed respawn anchor top active normal map size mismatch
- Fixed certain ocean biomes having a slightly bluer fog than usual
- Updated pack descriptions and removed localization, thanks to everyone who corrected the previous translations over the past two years
> The pack's version is also no longer listed in the description, you can still see it through the in-game UI's green checkmark where the gear icon previously was.

- Further adjusted torches to accommodate the state of a bug that caused point lights to go missing, improved heightmaps
- Adjusted redstone torch to accommodate an issue where transparent pixels on the texture appear opaque (MCPE-230978)
- Improved tuff and polished tuff heightmaps
- Improved carved pumpkin normal maps, the carved parts are now correctly indented
- Improved calcite and polished basalt normal maps (similar styles), improved calcite materials and heightmap
- Improved basalt materials with better consistency, improved some basalt heightmaps
- Adjusted grass top and side heightmaps
- Minor improvements to grass, podzol, mycelium, and grass path side normal maps, further revised blackstone normal maps
- Brought over the latest 1.21.130.28 client biome data, as a result the pack's unofficial minimum engine version is now 1.21.120
> Due to a Minecraft issue it will artificially remain at 1.21.100. This is critical, as without it many biomes' music and other properties will go missing, due to individual packs not inheriting the missing properties.

### Enhanced Option

- This is the end of the road for the Enhanced option as a separate feature in Vanilla RTX
> Going forward, it will be fully integrated into the main pack on release packages, as well as the version installed by the Vanilla RTX App. The Enhanced option will remain separate in the GitHub development folders, so you can continue to access the pure, widely compatible version of Vanilla RTX and Vanilla RTX Normals. The decision was made after it became abundantly clear Mojang is not going to fix Minecraft Bedrock Edition, let alone ray tracing. For years these vanilla resource fixes were separate as the glimmer of hope remained. This way the development files will remain clean, and the fixes and enhancements for vanilla Minecraft RTX become enabled by default.

- Updated several outdated JSON data based on the latest 1.21.120 vanilla resources

---

## 1.21.190

*A giant heap of quality upgrades, the result of a 2-week marathon through the backlog.*

### Changes

- Lava's brightest spots now radiate ever brighter!
- Increased shroomlight's emissivity and improved its normal map
> Shroomlight parts on crimson and warped fungi now appear brighter to more closely match shroomlight.

- Improved Glowstone block normal map
- Improved smooth basalt heightmap
- Sandstone updates:
> - Adjusted smooth and chiseled sandstone and their red variants' heightmaps
> - Updated all sandstone and red sandstone normal maps
> - Updated all materials for consistency between variations of the block, with adherence to the newest heightmaps/normal maps
> - Smooth sandstone is now closer to other smooth blocks (e.g. smooth basalt, smooth stone), as well as the sides of carved sandstones
> - Red sand and its products are now overall more rough than the non-red ones

- Improved gravel materials and heightmap
> Gravel is now closer to dirt pebbles in terms of roughness, representing small smooth stones near a real life river.

- Slightly increased sand and suspicious sand normal map intensity for more visibility
- Minor adjustments to suspicious sand MERs
- Updated sand and red sand heightmaps with an improved, subtle, layered approach
- Reworked blackstone heightmaps and normal maps
- Revised rough prismarine heightmap
- Revised chiseled blackstone heightmap and normal map to match the style of chiseled stonebrick
- Revamped the appearance of the pitcher crop pod to better match the materials of wet farmland and other dirt-like blocks
- Fixed most inconsistencies of the exposed copper block set
> The vanilla textures themselves use a highly inconsistent color palette, which resulted in inconsistencies in the PBR textures. They've been reviewed and resolved as much as possible, but a broader copper update is planned for some time in the future.

- Updated mangrove propagule PBR textures to match the style of other foliage
- Adjusted redstone block normal map, removed potential seams around the edges
- Adjusted wet farmland materials
- Reworked mud blocks (Mud, packed mud, mud bricks, muddy mangrove roots)
> All non-dried muds just got wetter and muddier! Corrected the mud bricks normal map, previously the upper bricks had a missing line. All heightmaps and normal maps were reworked.

- Increased accuracy of raw copper and copper ore materials to better match other copper blocks
- Updated ancient debris top heightmap to better complement its side
- Revamped raw iron, gold, and copper ore heightmaps and normal maps, now with more artistic complexity and a layered approach
- Revamped the materials of raw irons (ores and the raw ore block) to more closely resemble the properties of real life rough iron ore
- Updated mangrove log and mangrove root MERs for consistency with other wood
- Revamped the appearance of jigsaw and structure blocks, now consistent together with several corrections and improved heightmaps
- Improved redstone block heightmap
- Revamped stone heightmaps as well as wherever else the stone texture appears (e.g. grindstone, stonecutter) and all non-deepslate ore blocks
> The heightmaps are now much more well-defined.

- Daylight and nightlight detectors are now slightly emissive
> This is hinted at in default Vibrant Visuals.

- Updated all amethyst clusters to be more emissive, to more closely match their vanilla light level without affecting the appearance of their texture
- Sea pickles are now brighter to more closely match their vanilla light level, this doesn't impact the appearance of the texture

### Enhanced Option

- Removed the brighter lava which was previously isolated to the Enhanced option, as lava is now brighter by default
> For further tuning of emissivity (like getting the old lava back) you can use the Vanilla RTX Tuner App.

- Shortened file path names of bookshelf workaround textures to avoid potential errors
- Updated lit redstone ore heightmap to match the new redstone ore heightmap

### Known Issues

- The redstone torch texture renders with its alpha channel colors even at 0 opacity, causing it to appear a little strange in the latest previews, this is a game issue

---

## 1.21.184

*Copper Age parity.*

This revision brings over the latest changes from the vanilla game release and prepares for some of the issues introduced in the upcoming Minecraft 1.21.120 release.

### Changes

- Adapted textures based on the changes in the final previews and release of the Copper Age game drop
> Copper lanterns, copper bars, and copper torch have all been updated to match their latest textures.

### Enhanced Option

- Updated point light workarounds to adapt to the latest bugs introduced in Minecraft, including brighter lanterns in the Enhanced option to make up for their lack of a point light
> Once Minecraft 1.21.120 arrives, it is highly recommended to turn on the Enhanced option to keep these light sources functional.

---

## 1.21.180

*Copper Age game drop.*

Vanilla RTX once again covers the latest Minecraft update. Since Mojang has never tested new feature additions with ray tracing, it is up to Vanilla RTX to make sure it all works.

### Changes

- Added full support for all Copper Age game drop blocks
> Copper chests are block entities and do not support PBR. The remaining copper additions (copper bars, chains, lanterns, and the new lightning rod oxidation stages) are now supported. Additionally, when a lightning rod is struck by lightning, it now emits an intense flash of light with ray tracing!

- Improved iron bars normal map
- Updated the pack icon for the new update
> This update was developed during the Previews. As the Copper Age got closer to its release some textures were slightly altered, a future Vanilla RTX update will ensure parity.

### Enhanced Option

- Fixed the missing green flame texture
- New copper golem enhancements:
> - Fixed copper golem eyes not appearing with ray tracing (MCPE-227676)
> - Copper golem eyes now glow with ray tracing with a bloom effect, slowly dim out with oxidation levels, and match the appearance of their respective copper bulb

- Added super strong torch tips for soul torch and copper torch to keep them functional with ray tracing, a workaround for several items missing a point light on the Windows platform (MCPE-227624)
> There may be another minor update which addresses this issue in case it spreads to other items.

### Notes

> If you have trouble enabling ray tracing (MCPE-152158, MCPE-191513), simply use the Launch Minecraft RTX button inside the Vanilla RTX Tuner App (or follow the manual workaround guides found on most official download pages of Vanilla RTX).
> Updates may become a once-per-game-drop thing for a while, with the next big update planned for the fourth game drop. If development continues, atmospheric overhaul of biomes (the thing that gave each biome vanilla-accurate water colors and a unique atmosphere) will be picked back up.

---

## 1.21.175

*Prelude to Copper Age game drop support.*

The minimum required Minecraft version is 1.21.100, however, this version is intended only for 1.21.111 and higher.

### Changes

- Revamped water distance fog parameters of all biomes to closely follow vanilla behavior
- Fixed an issue that caused textures to get randomly swapped if Vanilla RTX Tuner was run while the game was open
- Fixed an issue that caused some textures to appear slightly stretched (quadrupled padding from 2 to 8)
> This was usually only noticeable when a block changed its texture based on its state, e.g. when placing or removing books from a chiseled bookshelf while using the Enhanced option, or when interacting with redstone ore, sometimes the texture would move slightly.

- Performed a parity check up to Minecraft 1.21.110.26 Preview and updated resources and client biomes wherever necessary to match the latest vanilla definitions
> For example, this fixes missing music in some biomes. Even though this is an RTX pack and should have nothing to do with music, the new client biome system is flawed and requires occasional updates to keep up with the vanilla game's client biome definitions.

### Enhanced Option

- Removed the soul torch lighting workaround (not necessary for this release)

---

## 1.21.170

*Tuner-friendly adjustments.*

### Changes

- Revamped the appearance of item frame and glow item frame
- Adjusted torches to allow Vanilla RTX Tuner's Emissivity Multiplier to leave a greater impact with high multipliers
- Updated rough prismarine normal map and heightmap
> The heightmap is now more detailed, with individual stone pieces no longer blending together, along with a corrected normal map. All PBR texture sizes now correctly match the base texture (previously this prevented Tuner from tuning this block).

- Revised andesite heightmap
- Beacons are now brighter
- Adjusted sea lantern so the edges are better impacted by the Vanilla RTX Tuner app
- Revised smooth stone slab heightmap
- Revised basalt top heightmap
- Adjusted leaf litter to be more dirt-like
- Minor adjustments to several blocks

### Notes

> This update is smaller than usual, and updates will be smaller and more frequent from here on. Development time is being split between Vanilla RTX, Tuner, and several other projects, and with modding platforms increasingly flooded with spam/fake updates, smaller and more frequent updates help genuine releases stay visible. Vanilla RTX Tuner automates updating the pack for you.

---

## 1.21.160

*Ghastly Update.*

### Changes

- Added full support for the dried ghast block
- Reworked the appearance of redstone lamp, now packing much more detail
- Updated the appearance of wool, improved details with slight variations per wool color, now diffuses more light, improved heightmaps and normal maps
- Updated all terracotta materials, details now vary between different colors, improved heightmaps and normal maps
> Regular terracotta no longer uses the wrong materials for its texture.

- Improved the appearance of tripwire hook Normals
- Tripwire wire now appears similar to web
- Increased spawner eye emissivity
- Updated icon and main cover

### Enhanced Option

- Updated Mooshroom textures based on the 1.21.90 release
- Tuned down the brightness of lava in the Enhanced option
- Updated several entity models to 1.21.90 with the new format version leash positions, for parity
- Disabled offscreen culling of ghasts

---

## 1.21.150

*Reformat update: TARGA files, Education Edition content decoupled into Chemistry packs.*

This update is unconventional. While a few areas got touched up, its core purpose is internal: reorganizing, reformatting, and optimizing Vanilla RTX for future development. This isn't about in-game performance, but about making workflows cleaner and tools more efficient to work with the upcoming Tuner app. **Tuner will only support Vanilla RTX 1.21.150 and above.** Moving forward, all previous Vanilla RTX Add-ons/Extensions are planned to be updated with the same changes.

### New Packs

- The Education Edition content revamped in 1.21.140 has been decoupled into standalone packs:
> - Chemistry RTX
> - Chemistry RTX Normals
> - Chemistry RTX Opus
>
> These are only available via the world resource pack settings menu. These packages are final and further updates won't be necessary.

### Changes

- All files within the pack now use the TARGA format (where applicable), which comes with a few benefits:
> - Less unnecessary data
> - More efficient batch processing of files (benefits the upcoming Tuner app)
> - Distributable package sizes reduced by up to 50% (also great for Tuner, which comes with the ability to auto-update Vanilla RTX)
> - Unpacked package size is up to 600% larger, which in turn leads to snappier load times in game (raw data, no decoding overhead)

- Unified colorspaces of all images to 8-bit per-channel RGBA
> Heightmaps are no longer 8-bit single-channel greyscale (this hasn't been a requirement for over six months).

- Removed the Fogless option
> Fog will be tunable in the future via the Vanilla RTX Tuner app, you will soon be able to thicken, lighten, or completely disable fog permanently.

- Removed all Education Edition content from the pack (decoupled into standalone packs)
- Updated fog format versions to 1.21.90
- Fixed missing MER animation of respawn anchor top, made consistent with nether portals through being uniformly brighter, this inconsistency is intentional
- The pack now uses textures_list.json and contents.json (built-in Minecraft features for caching)
- Minimum engine version is now 1.21.90
- Re-added a subtle emissivity to the dragon egg, as it became clear in Vibrant Visuals that this is the intended look of the dragon egg
- Increased Education Edition related blocks' normal intensities (carried over to the now-decoupled Chemistry RTX Normals and Chemistry RTX Opus packs)
- Updated various MERs for consistency
- Quality adjustments to a variety of textures (sunflower, torches, allium flower), alongside various other normal map adjustments
- Revamped cobweb, with a new silky touch!
- Revamped lever, now consistent with cobblestone and wood

### Enhanced Option

- Once again reverted the spyglass workaround to the 1.21.20 version, the previous workaround's file size was unreasonable
- Lava now appears brighter in the Enhanced option
- Soul torch emissivity workaround is now stronger in the Enhanced option

### Opus Only

- Fixed some textures losing transparent colors, causing some workarounds to stop working

### Notes

> One more revision is planned before returning to the biome atmospheric overhaul, 1.21.160 will bring support for the new dried ghast, with some potential enhancements for the happy ghast also planned. The Vanilla RTX Tuner app is imminent, and will initially be released to Vanilla RTX supporters, as it only supports Vanilla RTX 1.21.150+. A public release is planned after the release of Minecraft 1.21.90. The Chemistry packages and update files are available on Discord if you wish to try them out early.

---

## 1.21.140

*Education Edition elements.*

This revision is almost entirely dedicated to Minecraft: Education Edition. It targets the upcoming Minecraft 1.21.90 update, so minor issues (like missing block particles in the Enhanced option) will occur when using it with older game versions such as 1.21.80. The minimum engine version will be bumped to 1.21.90 in the next update.

### Changes

- All 118 Element blocks (plus the Unknown Element) have been revamped, with each elemental category now exhibiting features that reflect the real-world appearance of its group
> - Alkali metals appear somewhat rough and heavily oxidized, while alkaline earth metals are a bit less so
> - Transition metals exhibit the highest metallicity, while other metals and metalloids appear significantly less metallic
> - Noble gases and halogens now feature an icy/crystalline look, indicating how they'd likely appear in solid form
> - Biologically essential nonmetals like hydrogen, oxygen, and carbon now have a plastic-like finish
> - Actinides use a rough, corroded surface with a subtle glow to suggest radioactivity, visually similar to alkaline earth metals but with that added effect
> - Other groups follow similar material logic to reflect their physical nature
>
> Each category also includes distinct heightmap and normal map designs to add an additional layer to its visual identity.

- Other Minecraft: Education Edition blocks have also been overhauled
> Lab Table, Element Constructor, Material Reducer, and Compound Creator now feature fully fledged designs. Chemical Heat Block PBR textures now use the correct size.

- Revamped the appearance of TNT and Underwater TNT
- Updated the Lava texture to 1.21.90
> The texture was changed to include 32 stages instead of 20, normal maps and MERs were updated to match the new size. Lava now appears more vibrant than before, and has a revamped normal map.

- Improved emissivity of soul torch and underwater torch in the absence of hardcoded point lights, with minor improvements to other torch types
- Updated various color texture formats for consistency
- Minor texture tweaks and visual improvements across various blocks
- Fixed anomalies on the stone normal map

### Enhanced Option

- Updated block destruct and slide particle configs to match recent vanilla game changes
- Updated entity geometry format versions in the Enhanced option to align with the latest vanilla changes

### Notes

> This update was released as a checkpoint before some drastic changes to Vanilla RTX and its workflow. With the next update, Education Edition content will be stripped out of Vanilla RTX and put into individual packages.

---

## 1.21.130

*Atmospheric Overhaul continued. The fog overhaul is now 43% through.*

The last few updates revamped swamps, plains, and taiga biomes. In this release, nearly every warm biome has received a makeover, which is a major chunk of the full 87 biome list.

### Changes

- Atmospheric Overhaul: arid-land biomes (Desert, Desert Hills, Desert Mutated, all 6 Mesa variants, and all 4 Savanna variants), alongside all Jungle variants
> **Desert, Mesa & Savanna:**
> - Skies and clouds in dry biomes now feel drier and thinner compared to temperate biomes and forests
> - Air fog is brighter and tends to clear out faster at higher altitudes than in other biomes
> - Water colors were reworked to match their vanilla surface tones, this applies to every biome that receives the fog overhaul. For example, Eroded Mesa water, in comparison to desert, features a dark, pale blue surface color in vanilla graphics, which is now brought over to ray tracing
> - Shattered Savanna's appearance is a hybrid between savannas and jungles
>
> **Jungles:**
> - Jungles now have heavier clouds and deeper blue skies when compared to plains or other forest biomes. This unique trait is strongest in Jungle, Jungle Hills, and Jungle Mutated, and weaker in transition biomes like Sparse Jungles
> - Water colors also closely match vanilla colors
>
> **Other changes:**
> - Rebalanced Pale Garden fog
> - Swamp tweaks: slightly darker skies, denser clouds, and smoother biome transitions, with murkier waters (Mangrove Swamp waters in particular appear murkier than before)

- Fixed single-stage heightmaps on lanterns, which caused the glowing-chain issue to occur more frequently, particularly when lanterns are placed near chains
> Special thanks to Davis8483 for reporting and investigating this issue at [Vanilla-RTX/issues/44](https://github.com/Cubeir/Vanilla-RTX/issues/44).

- All flipbook PBR textures now use vanilla texture dimensions, even if only one frame was needed
> Adjusted many animated heightmaps to reduce final normal shifts throughout the animation (e.g. lanterns, smoker).

- Dirt-related heightmaps adjusted to be subtler
> Similar adjustments will follow for other abundant nature/terrain blocks.

- Campfire heightmaps updated for consistency with oak log

### Enhanced Option

- Further decreased the opacity of the falling leaves particle for all leaf types
> With ray tracing, the area beneath trees tends to be well lit while leaf particles remain quite dark, making them stand out. The change makes falling leaves less distracting, the frequency and other properties of particles remain vanilla.

### Opus Only

- In this iteration, Opus sees a bug fix to the rendering of torches and cocoa beans
> If you see any other texture that looks off, stretched, or otherwise distorted, you can report it via direct messages or on Discord.

### Notes

> The next atmosphere update will likely focus on oceans, the Nether, and the End, redefining their properties and tuning distant fogs to better match vanilla behavior. The Nether and End being too dark has been a long-standing complaint, and an upcoming update will aim to address it.
> This update began right after 1.21.120 as a direct continuation of the fog overhaul. During development a few more tools were built to ensure Vanilla RTX maintains perfect parity with vanilla resources, with zero unintended disparities found this time. Until recently, every RTX resource pack, including Vanilla RTX, leaned on a few shared fog configs across all biomes. For the first time, fog is being treated with the same precision as the blocks.

---

## 1.21.120

*Atmospheric Overhaul: taiga, plains, forests, and more.*

This version targets the upcoming Minecraft 1.21.80 update, but you can still use it on the Minecraft 1.21.73 hotfix. Just note a few things listed here will be missing in the current non-preview version of the game, but will take effect once 1.21.80 is out.

### Changes

- Atmospheric Overhaul for the following biomes: Taiga, Taiga Hills, Taiga Mutated, Mega Taiga, Mega Taiga Hills, Redwood Taiga, Redwood Taiga Hills, Plains, Sunflower Plains, River (non-cold), Forest, Flower Forest, and Wooded Hills
> **General breakdown** (the same can be expected from future atmospheric overhauls):
> - Atmosphere tends to be dimmer in dense forests, and rain now darkens the atmosphere more significantly in non-plain/wooded biomes. In contrast, the sun shines brightest in flat, non-hilly biomes
> - Cloud intensity now varies by biome. Biomes you'd expect to be clearer appear that way, and those that should have thicker clouds now look heavier and denser. They remain hollow enough to avoid being tinted by terrain light bounces
> - Water's surface color, as well as the color from the inside, now closely matches vanilla game colors
> - Underwater visibility is more restricted, similar to the vanilla game. You can no longer see across the ocean in the absence of direct sunlight, and water now properly absorbs light as you descend, the deeper you go, the darker it gets
> - Air and atmospheric color now vary per biome to match each one's intended theme, with smooth, non-jarring transitions, so biomes feel distinct instead of just being terrain transitions

- Pale Garden and Cherry Grove fogs have also been readjusted
- Minecraft 1.21.80.27 fixed PBR textures on candles, candles are now fully revamped with better lighting and a new waxy material
> Due to the lack of hardcoded point lights, candles are still somewhat dysfunctional, this is addressed in the Enhanced option.

- Adjusted the Ender Eye appearance, it now subtly glows in the dark (this reflects its intended design as seen in Vibrant Visuals)
- Improved the sea pickle's appearance
- Revamped the turtle egg's appearance
- Improved torchflower heightmaps
- Flattened Flower Pots
> This block has strange overlapping UVs, normals or heightmaps are best avoided entirely.

### Enhanced Option

- Reverted the Spyglass texture to the workaround seen in 1.21.10
- Added an enhancement for Candles
> Now more viable as a light source, with a fading glow effect on the wax towards the bottom. A lit candle's wick now glows a bright yellow instead of black.

- Removed the Dried Kelp Block workaround, no longer needed in 1.21.80.27+
- Moved the Chiseled Bookshelf workaround to a dedicated folder, purely for tidiness, there's functionally no impact

---

## 1.21.110

*Spring to Life game drop.*

This release introduces full support for all Spring to Life drop content, brings fixes for a few issues, and polishes several items.

### Changes

- Added complete support for the Spring to Life drop content
> Added PBR materials for the following blocks: Bush, cactus flower, firefly bush, leaf litter, short and tall dry grass, and wildflowers. The firefly bush was implemented in a way that didn't account for ray tracing, so the blinking texture animation is missing from default Minecraft RTX, a workaround restoring the blinking lights is included in the Enhanced option. The firefly bush emits a small amount of light similar to the vanilla game, with or without the Enhanced option.

- Fixed the sky turning cyan instead of grey during rain in the Cherry Grove biome
- Adjusted the Ender dragon egg's appearance and removed its emissivity
- Minor adjustments to the appearance of Lapis block, Lapis Ores, and Amethyst Cluster
- Adjusted pink petals for consistency with wildflowers
- Performed parity checks and updated resources where needed
- Detected and fixed a few unintended MER disparities between Vanilla RTX and Vanilla RTX Normals
- Updated the format version of all client biomes to 1.21.70 and carried over missing dry foliage data
> Vanilla RTX should not have to include these changes, but it is forced to because client biomes do not inherit their vanilla defaults. You can vote for the issue [here](https://bugs.mojang.com/browse/MCPE/issues/MCPE-190718).

- Updated pack icons
- Minimum required Minecraft version is now 1.21.70

### Enhanced Option

- Phantom entity improvements:
> - Eyes are now significantly brighter with a new bloom effect, allowing them to stay visible in the night sky
> - Fixed the eyes being misaligned with the head model
> - Phantom eyes continue to be visible when the phantom itself is invisible

- Updated the workaround for missing mooshroom mushrooms to use the new model from 1.21.70 alongside the newer textures
> The mushrooms were remodeled with more accuracy, brown mooshroom mushrooms are now taller, and baby Mooshrooms no longer have any mushrooms on their body.

- Added particle adjustments for falling leaves and magic critical hit
- Added a workaround for the firefly bush firefly texture animation missing
- Adjusted the sun texture for ray tracing, the texture is now more visible through the air's volumetric fog instead of appearing white
- Removed workarounds for item texture issues, spawn eggs now have individual item textures in Minecraft which no longer have coloring issues in ray tracing
- Re-enabled offscreen culling for most entities that previously had it disabled
> It generally remains enabled for large floating mobs and similar, and remains disabled for the rest.

### Notes

> This is the first update shared on Ko-Fi. Minecraft has added three critical ray tracing bugs recently: one with the RT toggle and foliage rendering issues in 1.21.60, then severe flickering issues in 1.21.70, and another introduced in the 1.21.80 Previews that turns all entities black.

---

## 1.21.100

*Swamp fog overhaul, parity check, and maintenance.*

This is mainly a maintenance update to get things back in order for the latest Minecraft releases.

### Changes

- Added support for the Dormant Creaking Heart block state introduced in Minecraft 1.21.60
- Fog overhaul: Swamp, Swamp Hills, Mangrove Swamp, and Pale Garden
> - Pale Garden water has been adjusted to be reminiscent of vanilla game colors, with a natural transition between water and air. Previously the bright blue colors clashed with the dark, dead atmosphere of the pale garden
> - Water in all swamps is no longer crystal clear, it now appears darker and murky, with colors matching vanilla game colors
> - Air fog has been revamped to uniquely fit each of the three swamp biomes, giving them a fresh atmosphere
> - Vision underwater in these biomes is now limited, depths now significantly affect darkness similar to the vanilla game. This will apply to more biomes going forward

- Performed a full parity check with the vanilla resources (Feb 2025), which brings over some missing features and fixes others to work with the latest available versions of the game
> - Fixed the missing Nether dimension ambient sounds
> - Updated all client biomes for data parity with the vanilla game. Unfortunately missing properties are not inherited from vanilla resources, which can cause issues without notice. This will be ongoing and will require constant updates until Mojang improves the client biome solution

- Adjusted command block normal maps to avoid seams when command blocks are placed near each other in different orientations
- Updated seagrass and kelp heightmaps, the new ones have no height variation near the edges of each stage, which previously caused seams in blocks like tall seagrass
- Minor improvements to various textures, such as withered rose, barrel heightmaps, and more
- Removed the unnecessary Eyeblossom texture
> Inventory-only textures should not be included in Vanilla RTX unless necessary.

- Vanilla RTX's new minimum supported version is Minecraft 1.21.60

### Enhanced Option

- Fixed tropical fish patterns not being composited properly if the fish's base layer is transparent (this was causing fish fins to go invisible with ray tracing)
- Adjusted various particles: added six of the missing particle adjustments for ray tracing, updated some outdated particle definitions, and fixed a typo in one of the particle file names
- Fixed an issue where cats' collars would always appear grey without ray tracing
- Reverted the frogspawn inventory texture to the vanilla one
- Added a universal workaround for rendering errors of cross-shaped blocks, foliage, and crops (MCPE-189266)
> This applies to almost every block of these kinds: all sapling types and the mangrove propagule; all flowers and flower types, mushrooms, fungi, and similar; all grass types and shapes, bushes, ferns, and similar; hanging roots, pale moss, and similar; sugarcane; all corals and dead corals; wheat, potatoes, carrot crops, nether warts, and similar; all amethyst bud sizes and amethyst cluster. Previous workarounds for dripstone and cave vines were removed until a better solution is found.
>
> This issue will persist for the following blocks: Glowberry vines, Pitcher plant, Kelp, Pointed dripstone, Weeping vines, Twisting vines, Seagrass, Sweet berry bush.
>
> This bug doesn't affect some items in 1.21.60, but with the changes Mojang is making in 1.21.70 and later updates, it unfortunately will. This is as future-proof as it can get. See [MCPE-189266](https://bugs.mojang.com/browse/MCPE-189266).

---

## 1.21.90

*Resin parity, a new Pale Garden atmosphere, and a full resource parity check.*

### Changes

- Redefined all materials of the Resin block family for a more coherent look
> Creaking heart and Eyeblossom now glow brighter. Resin clumps heightmap and normal map were inverted, since the plane/model was unintentionally flipped in the vanilla game.

- Revised anvil heightmaps and normal maps
- Revamped all command block heightmaps and normal maps for a new refined appearance
- Performed a full resource parity check (Dec 2024)
> - Updated all PBR textures according to the 1.21.50.29 and 1.21.60 texture changes, the following blocks are affected: Brick, chiseled nether bricks, chiseled resin bricks, cracked nether bricks, nether brick, red nether brick, resin bricks, lit powered exposed copper bulb
> - Updated some leaves textures that were silently updated in recent previews (likely done for consistency with other leaves, mostly affects alpha channels, this is a parity change and PBR textures remain unaffected)
> - Included PBR support for the opaque mangrove leaves variant introduced in a recent preview

- New unique Pale Garden atmosphere and fog to match the vanilla game
> The sky atmosphere now appears much darker upon entering the pale garden, with sky color and fog color matching the vanilla game or promotional renders.

- Resolved some disparities between leaves textures and their opaque variants
- Updated some heightmaps and normal maps for blocks with flipbook textures to be only a single stage
> This is for consistency, and to prevent sudden height changes when a texture heightmap reaches the end of the flipbook, which has a slightly different normal map generated based on it.

- Minimum required Minecraft version is now 1.21.51
- Updated description translations for better accuracy across all languages
- New pack icon and cover image

### Enhanced Option

- Updated the Magma Cube glowing enhancement based on a recent model change from the vanilla game
- Updated the workaround for the Creaking, invisible creaking eyes now remain visible, similar to Endermen and Spiders
> This behavior, although absent from Garden Awakens at launch, was included later in Minecraft 1.21.60 Preview for parity with Java Edition.

- Added a texture fix for the Creaking spawn egg in ray tracing
- Added a color-corrected pale oak door texture for ray tracing
> Because the door texture already uses very bright colors, it is not possible to offset it too much, so this particular workaround remains pretty tame for this door.

- Revised some particles for ray tracing
- Increased vibrancy of glowing parts on some entities which previously had the glowing enhancement
- Updated various other Enhanced resources based on the latest Minecraft release for parity

---

## 1.21.80

*Resin Clumps, Resin blocks, and Eyeblossom support.*

This update brings full RTX support for all the latest additions in Minecraft Preview.

### Changes

- Added complete support for Resin Clumps, Resin Block, Resin Bricks, Chiseled Resin Bricks, and Eyeblossom
> Newer previews reveal that the creaking heart is made of Resin. In this update, the creaking heart has been revamped entirely to reflect this fact, and also packs much more detail while staying consistent with other resin or wood blocks.

- Improved all log top and side heightmaps, as well as their stripped variants
- Fully revamped all log top and side normal maps and their stripped variants
> While the new textures are a significant improvement, this was largely done to open room for establishing a consistent logic between the new pale wood blocks, the creaking heart, and older wooden blocks. As such, the creaking heart normal maps and heightmaps have also been revamped to stay consistent with other wooden logs.

- Revamped vines and waterlily
> New MERs to stay consistent with other leafy materials. Vine normal maps now tile properly with an improved heightmap. Waterlily normal map and heightmap now follow the texture's intended shape. Improved weeping vines normal maps and heightmaps.

- Improved water textures with an updated formula, with slightly more vivid water that is more accurate to vanilla Minecraft
- Updated Cauldron and Hopper
> Gave cauldron and hopper distinct characters with new normal maps and heightmaps. Adjusted Hopper MERs based on Cauldron for consistency.

- Improved all log side normal maps
- Performed a full texture parity check (November 2024)
> - Several textures were found with variations in game files, with only one being used in game, unused files were removed
> - The Brick texture was found to be altered, PBR textures were updated accordingly
> - Corrected Weeping Vines texture names (two sets of textures are present in vanilla files but only one set is used in game)
> - Updated the creaking heart texture

- Fixed active ominous vault front states emitting the same color of light as the inactive state
- Adjusted bamboo mosaic heightmap
- Improved clay heightmap and normal map
- Updated the pale garden client biome
- Many other micro-adjustments to various textures

### Enhanced Option

- Added particle enhancements for new Pale Garden particles (falling leaves, creaking particles, etc...)
- Improved rendering of the Creaking with ray tracing, added a workaround for the black texture issue of the Creaking mob, as well as an enhancement to make its eyes appear bright with ray tracing
- Added a workaround for non-colored states of cauldron water appearing rough and not using the proper texture set in the vanilla game
- Fixed the End Portal's pitch black material
> The Normal/height pixel has been moved to the 3rd, and the MER pixel's location repositioned to the 5th pixel of the End Portal image. This is hardcoded and has been continually changed by Mojang in previous versions, so it may break again if Mojang changes the position of hardcoded values again.

- Fireworks rocket no longer appears invisible without ray tracing
> This was previously a side effect of the black firework texture bug workaround. The fireworks rocket model has also been minified so it overrides less of the rasterized areas.

- Updated the Black Enchanted Trident workaround
> Eliminated all unintended side effects at the cost of a black tint over the enchanted trident. This workaround is now worse than before visually, but comes with no unintended bugs while making enchanted tridents more visually correct.

- Due to an issue with enderman-held blocks appearing too bright, Enderman eyes no longer ignore light and react to vanilla light levels instead
> Even now Enderman eyes still stand out slightly brighter, even at light levels of zero to four (fully dark or moonlight).

---

## 1.21.70

*Early Pale Garden support and the groundwork for the fog overhaul.*

Minecraft 1.21.40 comes with significant changes to how fog works. This update lays the foundation for the new fog schema, new fog features, and future fog updates, and also completes the glass update from 1.21.60.

### Changes

- Added early support for the Pale Garden
> - Added support for the Pale Oak wood set, including the doors, tree, and saplings
> - Added support for the Creaking Heart, which features a subtle glow, a wood imbued with magical properties
> - Added support for the Pale Moss
> - Added a placeholder default fog for the pale garden, a more complete fog with unique properties will be added with a future update
> - Adjusted Moss textures
>
> Textures are subject to change with future previews, as such some of them are placeholders and not the finished version.

- Updated the appearance of Obsidian-related blocks (enchanting table, respawn anchor, obsidian, crying obsidian, and glowing obsidian)
> - Revamped heightmaps with a more well-defined look
> - New hand-painted normal maps that pack significantly more detail and follow the texture's intended shape
> - Updated the portal MER animation to be an average of all stages, due to PBR animation being broken for this particular block (previously only the first stage was used)
> - Respawn anchor has been revamped entirely with more logical heightmaps and normal maps, the enchanting table has also been improved, and the textures now properly tile with obsidian and crying obsidian from the sides and bottom
> - Revamped MERs for a more life-like appearance that fits better with the new normals and heightmaps

- Revamped purpur blocks: more well-thought-out heightmaps, revamped normal maps, and redefined MERs that represent their connection to chorus fruit
- Fog overhaul groundwork
> This update lays the foundation for the future fog overhaul. To start:
> - Migrated to the new client_biome system instead of biomes_client
> - Updated the fog format version to 1.21.0, and starting from now applicable biomes use the new weather volumetric fog
> - Updated all fog names and identifiers to follow a naming pattern similar to vanilla Minecraft
> - Improved clouds, which remain mostly the same across all biomes
> - Split fog configurations into tens of different instances, with each biome having its own fog configuration
> - Cleared outdated biomes and identifiers based on the latest Minecraft version
> - Adjusted all fog to have vanilla values, RTX fog will no longer grant players extremely increased visibility underwater, and the player's vision is now limited in exactly the same way as vanilla Minecraft
>
> Visually, fog remains largely the same in this update, this was just the necessary groundwork. Future updates will slowly revamp fog for all biomes with unique, varying atmospheres and configurations per biome that more faithfully preserve the vanilla theme.

- Updated the grass top normal map to account for its isometric property
> Grass normal map no longer appears to be more intense with direct light from certain angles. In game, this eliminates the weird random darker grass squares during sunset by having a similar average vector intensity in all directions.

- Revised end rod, notably brighter to more closely match its vanilla light level of 14
- Improved overly dark spots on the gravel normal map
- Updated all texture set format versions to 1.21.30
> This seemingly results in faster loading and fixes some loading issues.

- Improved Glowstone normal map
- Adjusted sniffer egg heightmaps
- Nerfed glow lichen emissivity
- Vanilla RTX and Vanilla RTX Normals' new minimum engine version is 1.21.30, make sure you're using the latest Minecraft release

### Enhanced Option

- Improved some of the door color correction workarounds by using a new method to maximize the brightness of their textures
> Added color correction for all variants of copper doors. The new door color corrections are mathematically accurate and made as bright as possible by the distance of the brightest pixel to maximum brightness. This preserves the color composition of the image while making it brighter, solely to counter the darkened doors bug (MCPE-121412).

- Wither Armor and several other rasterized parts on mobs now appear brighter

### Notes

> This is a transition period: for the past four years, Vanilla RTX has supported all game versions since the Nether Update.

---

## 1.21.60

*Glass Overhaul.*

This update completely overhauls all glass, a delicate process that took a long time to complete. Perfecting a truly vanilla glass has been a goal since 2022.

### Changes

- Grand Glass Overhaul
> This rework applies to all glass in game, including all colors of different glass variants and hard glass. Blocks with varying opacity levels or uniformly transparent blocks such as ice variants, slime, honey, etc. are also affected. The goal was to finally bring together a direct and mathematically consistent conversion for all glass, allowing all glass to retain near-vanilla color and transparency with ray tracing. This means glass is no longer overly vibrant, it changes the color of light that passes through it in a similar way to the vanilla game, and other transparent blocks such as ice or hard glass are no longer overly opaque and preserve their vanilla appearance.
>
> - Reworked all glass, glass pane, and hard glass MERs, all textures now come with much more detail and full consistency, glass pane top MERs now properly match their non-pane variants' frames and scratches
> - Added normal map edges for glass and glass panes in Vanilla RTX Normals
> - New reworked tinted glass with an amethyst touch
> - Glass frames and glass pane tops now boast more detail
> - Added heightmaps to glass pane tops, improved all existing glass heightmaps
> - Converted all glass pane top colors to remain fully consistent with glass
> - Modified all hard glass textures for ray tracing
> - Similar to glass, readjusted ice, slime, and honey

- Properly converted the portal texture for ray tracing, the texture now has maximized translucency while preserving its vanilla color composition and appearance
- Revamped pumpkin and watermelon normal maps, improved heightmaps
- Revamped redstone repeater and redstone comparator normal maps, improved heightmaps, improved stone parts on MERs
- Reworked the camera block, much more detailed, with corrected normal maps and fixed heightmap noise
- Revamped Emerald Block normal map and adjusted iron block normal map to be in line with the style of similar blocks (such as gold, Netherite, etc.)
- Revamped bee nest and bee hive
> New hand-painted normal maps and heightmaps. Improved MERs, now consistent with honey and packing more detail.

- Improved honeycomb normal map and heightmap
- Revamped soul sand and soul soil normal maps and heightmaps
- Updated glow berries to emit a significant amount of light while preserving texture saturation
- Redefined the honey material across all block textures with honey
- Updated acacia trapdoor heightmap
- Fixed noise on the polished deepslate brick heightmap
- Resolved any file name disparities between Vanilla RTX and Vanilla RTX Normals and removed unused files (deepslate gold was extra in Normals, and rail turned was named differently)
- Rebranded the Experimental subpack option to Enhanced
- Greatly reduced the brightness of Chemical Heat block to remain faithful to its vanilla properties (0 light level), adjusted transparency
- Corrected normal values of smooth stones
- Readjusted slime and honey textures for ray tracing, made heightmaps more subtle
- Adjusted pointed dripstone heightmaps, updated pointed dripstone block normal map and heightmap
- Fixed a critical issue that prevented resources from being properly loaded in world settings, often with half the files missing
> This would happen at random on certain devices with both Vanilla RTX and Vanilla RTX Normals. This issue might still happen with future Minecraft versions, so it is highly recommended to stick to Global resources, since loading packs in your world makes the game try to copy the pack files, which can sometimes cause issues. Changing subpacks may also sometimes not work, and require you to do it multiple times. Loading the pack in a world is necessary only when using Education Edition to load education related files.

### Enhanced Option

- Fixed the End Portal texture adjustments
> Mojang changed the hardcoded pixel locations from the 10th and 5th pixel for Normal and MER respectively, to the 6th and 3rd pixels from the top left corner of the image.

- Disabled entity culling for a number of mobs and entities
> This often applies to large entities, block/immovable entities, and flying entities, as well as entities that don't often spawn in bulk and flying thrown entities such as all player-thrown items. A total of 31 entities are affected. Culling preserves a good chunk of performance in some scenarios and shouldn't be disabled on all entities.

- Replaced the 3D model of villager levels with a simpler plane to more closely match the vanilla game
> This was done because it was impossible to make the 3D appearance go well with other layers, and it ended up looking weird on some villager clothing variations.

- Fixed thrown enchanted tridents appearing black
> Known issue: the hand-held model appears invisible in first person view mode, and appears invisible in all view modes if ray tracing is turned off. This is temporary and may be improved with future updates.

- Fixed the in-world fireworks rocket texture appearing black
> Known issue: fireworks appear invisible if ray tracing is turned off.

- Added a new Jack O' Lantern enhancement that allows it to glow much more closely to its vanilla light level by emitting light from all sides
> This was created to emulate a kind of subsurface scattering effect, as though a torch is placed inside the carved pumpkin.

- Made Enderman and Magma Cube eyes, and the lava core of the Magma Cube, appear brighter
- Removed the Sun Path modifiers from the Enhanced pack, as Mojang has decided to remove the capability from default and RTX graphics modes and limit the feature to Deferred Lighting
> You can help it return by voting for [MCPE-180094](https://bugs.mojang.com/browse/MCPE-180094) or [here](https://feedback.minecraft.net/hc/en-us/community/posts/4406892103565-Ability-to-change-Sun-Azimuth). Personal note: Mojang putting effort into making sure we don't *accidentally* use capabilities not intended for ray tracing, instead of adding features, is not funny.

- Adjusted pointed dripstone and cave vine (glow berry) textures to counter Z-fighting issues present in the vanilla game (MCPE-121746)
- Further reduced spore blossom ambient particle opacity
- Added carried textures for some transparent blocks: Ice, tinted glass, slime, honey, as well as dripstone and glow berries due to adjustments in this update
> This allows the vanilla texture to display in the player's inventory without the ray tracing specific adjustments meant for in-world textures.

### Notes

> The new glass appears much more desaturated compared to 1.21.50 and older versions, and this might not be to everyone's taste. The previous glass belonged to the earliest versions of Vanilla RTX, when not much thought went into it beyond making something that looked nice. The new glass is meant to much more accurately represent how textures are in vanilla Minecraft, and the degree to which it affects light is now consistent across all glass, just like the vanilla game. If you prefer a saturated glass that turns light into a very saturated color when it passes through, a Clear Glass add-on update is on its way with an option for saturated glass, suitable for playing with color (e.g. saturated colored godrays). The glass update is completed in 1.21.70.

---

## 1.21.50

*Fifth major revision for 1.21. Mostly bug fixes, a vastly expanded Experimental option.*

This update is largely about fixing a huge number of bugs and enhancing vanilla resources for ray tracing. It vastly expands the Experimental option and adjusts assets beyond blocks to improve their compatibility and appearance with ray tracing.

### Changes

- Revamped blast furnace normal maps, a new style that aligns with similar items
- Improved chiseled bookshelf normal maps
- Improved cauldron top heightmap with better edges
- Adjusted slime and honey opacity, now per-pixel
- Decreased End dimension fog density, the sky now appears more purple
- Updated Chinese and Taiwanese translations for better accuracy, courtesy of "hermitisla"

### Experimental Option

To use Experimental features, you must switch to the Experimental option from the settings of Vanilla RTX.

- Ender Dragon's mouth, Magma Cube's inside lava and eyes, and Enderman, Spider, and Phantom eyes now glow with RTX
> This doesn't come with ray-traced emissivity, there may be unintended effects when ray tracing is off. In general it's worth remembering that changes in the Experimental option are primarily aimed at RTX mode, with game resources modified for proper functioning in ray tracing only.

- Fixed the invisibility effect not properly hiding the models of the following entities when ray tracing is enabled: Spider, Cave Spider, Phantom, and Enderman
- Fixed villager texture issues (biome clothing, professions, and levels), they now display correctly with ray tracing
> This is the same issue as the one listed in the known ray tracing issues list on the Minecraft website. Models for villagers have been adjusted to allow textures to display correctly with RTX while maintaining the vanilla game appearance, minor disparities or issues may be present.

- Fixed missing clothing and profession gear on Zombie villagers with ray tracing
- The glasses of Cartographers, Librarians, and their Zombie counterparts are now rendered as glass
- Improved the chiseled bookshelf book front texture workaround, you may now place books in all possible combinations
> Textures have been manually defined for all remaining states in all directions (North, West, South, East) to allow for PBR texture assignment. Prior to this update, this bug was fixed in the Experimental option, but textures were static (only empty and occupied states with PBR textures). In vanilla Minecraft this is handled internally, and Mojang did not account for ray tracing, leading to Z-fighting and the impossibility of PBR textures. This fix could break in future Minecraft updates if the handling of chiseled bookshelves changes, since the current one has its own issues.

- Restored the Warden's bioluminescent layer with ray tracing, the Warden heart now glows and beats, and spots display properly
> This workaround may be improved in the future, some transitions are currently sudden.

- Adjusted Nether Update biomes' ambience particles for ray tracing
- Fixed the snow golem head remaining unaffected by ray tracing, the pumpkin head is no longer rendered similar to particles
- Improved breeze wind animation
- Fixed an issue where tamed cats would not cast full shadows
> Known issue: tamed cats' collar color no longer displays without ray tracing. Vanilla RTX, and especially the Experimental subpack, is intensely focused on the ray tracing mode of vanilla Minecraft only, meaning there can be side effects without ray tracing. These will be addressed as time goes on, however they are lower priority.

- Improved the fix for the dried kelp bottom texture, in-world and inventory textures now better match vanilla Minecraft
- Reverted all flame/lava and soul flame particles to be fully opaque (smokes remain semi-transparent)
- Adjusted the beacon beam texture for ray tracing
- Fixed an issue in Vanilla RTX Normals where the world would appear warped and bent when viewed from certain angles in End Portals
- Fixed an issue where Slime and Magma Cube mobs would flicker and pixelate their surroundings with ray tracing
- Updated the fix for TNT Minecart and Command Block Minecart blocks rendering as particles
> - Updated models to better match vanilla Minecraft, eliminated lines due to slightly disjointed models
> - Fixed a Z-fighting issue when blocks in minecarts were viewed from afar, removed rasterized parts
> - Fixed an issue where the Minecart's geometry would shift around briefly after being placed on a turned rail

- Cleared unnecessary files and references

### Known Issues

- Villagers and zombie villagers: the performance impact may be larger when too many villagers are present, texture Z-fighting occurs at high distances without ray tracing, and villager heads may occasionally flicker with ray tracing

### Notes

> This was a unique update that took a while to deliver, as it focused on fixing almost every remaining major Minecraft bug that could potentially be fixed. These bugs were fixable due to being data-driven and could be edited to work with ray tracing. Conversely, items handled mostly internally cannot be modified or fixed (unless you have access to Minecraft's source code), which means issues with banners, maps, and similar bugs can not be fixed. More fixes will come for both existing and new Minecraft additions, as Mojang is unlikely to account for RTX while adding new items.
>
> **Why are all these bug fixes limited to the Experimental option?** A fix moves out of the Experimental option into the default Vanilla RTX when it meets the following criteria:
> - It must remain visually the same as vanilla Minecraft and not alter it
> - It must not cause other bugs or issues, whether ray tracing is on or off
> - It must not cause a significant performance dip
> - It must remain stable across many Minecraft updates (i.e., avoid undocumented features that could change and break)
> - It must ideally remain compatible with other texture packs that modify folders other than `root/textures/blocks`, or Minecraft's featured server resources
>
> So far only a few fixes fit these criteria, and even then there's reluctance to move them to the default Vanilla RTX. Maybe one day, when all bugs are fixed and everything is as stable as it can get, this option will be renamed to "Enhanced" to sound less scary and encourage more people to use it. One of the ideas of Vanilla RTX is to keep it pure, changing things only out of absolute necessity. This ensures maximized compatibility and makes Vanilla RTX integrate seamlessly as part of the game's own resources stacked on top of each other, which is what allows you to use a great variety of resource packs and add-ons with Vanilla RTX without seeing errors.
>
> **Should you use the Experimental option?** If you're using only Vanilla RTX (with its add-ons), using it all the time is highly recommended. In cases where you're using other add-ons/mods, resource packs, or forced server resource files, things have a chance to break, so turn it on and see if everything works fine. If it does, keep using it, if something breaks, turn it off. These fixes are directed only at the RTX mode of vanilla Minecraft, and the Experimental option is expected to work without issues only with the vanilla ray-traced game, and without third-party texture packs, add-ons, or mods. Optimally, make sure Vanilla RTX is stacked on top of the vanilla game, without any other third-party packages or mods. Meanwhile, Vanilla RTX's default mode can be used alongside anything you wish.
>
> Recent Betas and Previews have brought updates to Deferred Lighting which caused some parts of Vanilla PBR to break, a new update is coming soon.

---

## 1.21.40

*Texture parity check, grindstone, cobbled deepslate, and bamboo.*

### Changes

- Performed a full texture parity check with vanilla Minecraft for 1.21 (May 2024)
> - Trial Spawner and Ominous Trial Spawner textures were found to be changed, PBR textures have been updated accordingly
> - The Missing tile (UPD-ATE!) block was found to be changed in the latest resources, PBR textures have been updated accordingly
> - Regular vault textures were found to be slightly updated, PBR textures have been updated accordingly
> - Various other textures were also updated that were slightly off (usually not by more than a single RGB digit on some pixels)

- Decreased the overall roughness of ice variants
- Revamped all amethyst block and crystal normal maps, also improved heightmaps, less noisy and more logical than before
- Revamped Grindstone
> Now consistent with smooth stone and stone (edges are considered to be made of smooth stone while the rest is regular stone), with revamped normal maps and heightmaps.

- Revamped cobbled deepslate with better defined heightmaps and normal maps
> Now follows a similar style and logic to ancient debris, where no part of the texture is considered mortar, and it instead appears as though there are layers of stone laid on top of each other, which is much more faithful to what the artist intended with the vanilla texture. The new handcrafted normal map is brought to you through blood and tears.

- Bamboo updates
> - Improved bamboo mosaic heightmap, there is now more elevation between different parts
> - Improved bamboo stem normal map, now slightly curved
> - Updated all new 1.20 bamboo blocks with perfected normal angles similar to planks, and aligned them with the new appearance of the bamboo stem's nodes
> - Updated scaffolding normal maps and heightmaps to match other bamboo normal maps
> - Improved bamboo leaf heightmaps

- Other adjustments
> - Fixed more jarringly dark pixels from certain angles on cobblestone normal maps
> - Removed unused torchflower files
> - Readjusted all log top normal maps, the curve now more strongly applies to non-mortar parts
> - Removed the cached textures and file lists, as they caused unexpected errors instead of preventing them, and came without any significant effect on load times
> - Improved iron block normal map
> - Increased cake normal map intensities and adjusted the top
> - Updated various normal maps that had plank texture in them to match the intensity of planks (e.g. crafting table, cartography table, etc.), along with other general corrections to wooden table blocks
> - Minor overworld fog adjustments, dialed back on the red tone
> - Minor corrections to lightning rod

### Experimental Option

- Added 1.21 particle adjustments for ray tracing
> All new in-game particles now blend in with the world, such as breeze and wind charge explosions, mace particles, as well as trial chambers related particles.

- Fixed more issues with redstone ore reactivity in the Experimental option (seemingly caused by content jsons)
- Further decreased the brightness of Breeze wind

---

## 1.21.30

*Animated materials, Ominous Trial Spawner and Vault support.*

### Changes

- Added full support for the Ominous Trial Spawner and Ominous Vault block of Trial Chambers in Minecraft Preview
- Reworked and updated the non-ominous vault block and trial spawners according to texture updates in Minecraft Preview 1.21.23.0
> This also fixes the trial spawner active state being unsupported in the latest Minecraft Preview.

- Quartz normal map revamp
> Improvements and corrections to quartz bricks and chiseled quartz normal maps. Quartz and smooth quartz will no longer appear curved/round, this allows smooth quartz to form seamless tiles similar to the vanilla game.

- Reworked Netherite and Ancient Debris, with new hand-made normal maps, improved heightmaps, and completely redefined materials
- Updated Iron block and Lapis block normal maps to be in line with the appearance of similar blocks (i.e. gold block, copper block, etc.)
- Added a cached texture and files list, this could potentially improve load times or help prevent an issue where textures aren't fully loaded
- Fixed dropper top horizontal incorrectly using the dropper top vertical MER (and vice versa)
- Animated material updates
> Not long ago animated textures were fixed in Minecraft. Prior to this, Vanilla RTX used an average of all stages of a texture to have a PBR texture that approximately looks good throughout all stages of an animated texture. This update comes with proper animated materials for many animated blocks, which usually results in improved vibrancy and allows true texture colors to be preserved throughout the animation, or in other words, less "washed-out" colors. Known issue: this bug persists with the sculk catalyst blooming state and sculk shrieker.
>
> - Magma block
> - Blast Furnace
> - Sea Lantern (also updated materials to better match other prismarine blocks)
> - Portal and Respawn Anchor Top Portal
> - Lantern and Soul Lantern (also nerfed the overall emissivity of soul lantern)
> - Cauldron water, also changed to a new material that closely matches regular water (known issue: non-colored water in the cauldron does not have a material)
> - Sculk Tendrils, also updated normal maps and heightmap animations
> - Sculk Veins, materials now appear most consistent
> - Sculk (I'm aware of some inconsistencies in sculk, a future overhaul will universally refine and unify all sculk blocks)
> - Sculk Catalyst Blooming and Sculk Shrieker Top (these two in particular do not have proper animations, however they have been improved in other ways to make up for the lack of animated PBR materials)
> - Rough Prismarine
> - Crimson and Warped log, also improved heightmaps
> - All variations of Command blocks
> - Campfire and Soul Campfire base (this only affects their base/burning coal parts, not the fires themselves, the animation update for fire and soul fire is set to arrive with a future update). Also removed the unnecessary campfire fire normal and adjusted campfire log heightmaps
> - Chemical Heat block in Education Edition

- Updated smoker
> Revamped normal maps, improved heightmaps, added proper burning emissivity animations, and updated materials for consistency with other wood and stone.

- Reworked mossy stonebrick and stonebrick normal maps with better defined cracks and mossy parts
- Adjusted default fog settings to be closer to default Minecraft RTX sky colors (i.e. reduced the subtle green/cyan color of the sky horizon in some biomes), removed the blue tint
> I'm aware of other issues like water appearing inappropriately discolored in certain biomes such as some rivers, all similar problems will be addressed in a future update with the yet-to-arrive grand fog overhaul. These changes are only meant to get things in a better state for the time being.

- Other adjustments
> - Overall dimmer comparator and repeater active states, so they may no longer be functional as a light source (vanilla light level is 0)
> - Decreased intensity of all plank-type normal maps and corrected angles
> - Uniformly increased lava emissive intensity, increased lava normal map intensity
> - Adjusted redstone, regular, and soul torch texture brightness (redstone and soul nerfed, regular torch slight buff)
> - Nerfed all passive redstone materials' emissivities, with less contrasting colors
> - Decreased heightmap intensity of foliage such as grass and ferns to more closely match grass top
> - Maximized portal transparency (further reduction of opacity will result in issues with the screen overlay animation of the portal)
> - Decreased cauldron water opacity
> - Adjusted all white irons and all gold blocks, now possessing slightly more metallic characteristics (i.e. iron doors, block, gold parts on rails, gold block, gold parts on chiseled bookshelf, all gold ores, etc.). This also makes white irons more distinct from grey irons, where grey irons now appear slightly less metallic and more rough overall, while retaining the same detail and style

- Updated pack icon

### Experimental Option

- Fixed blocks in Command Block Minecarts and TNT Minecarts not being affected by ray tracing
> Minecart entities have been faithfully remodelled.

- Moved the Slime mob texture and End Portal adjustments under the Experimental option (undocumented feature)
- Fixed Iron Golem cracked stages not displaying with ray tracing
> Removed cracks being overlays, and instead each cracked stage now has its own complete texture, which eliminates the issue and should remain visually the same as vanilla Minecraft.

- Improved the workaround fix for Breeze wind, inner layers can now be visible (previously only the outermost wind layer was displayed)
> Breeze wind now appears more transparent with ray tracing to better match the vanilla game. Known issue: inner layers are only visible when looked at from the top and bottom.

- Swapped sun and moon paths, the maximum offset is now 30 degrees, and the sun's path was modified to follow a much smoother curve without disruptions

---

## 1.21.20

*Dirt, Heavy Core, and a big batch of mob fixes in the Experimental option.*

### Changes

- Perfected all dirt! (dirt textures on grass, mycelium, podzol sides, all dirt variants, even the dirt parts on hanging roots or missing tile, etc.)
> - Dirt materials have been updated with a more ample dirty appearance
> - Pebbles now appear consistent and overall more rough
> - New heightmaps that remain consistent across all dirt blocks
> - Updated normal maps with seamless tiling, this is especially important now that with the updated sun azimuth, players get to see from different angles
> - As a result of all the changes above, there is no more unintended noise in heightmaps, and every pixel with a wrong height and material value is now corrected

- Added support for the "Heavy Core" in Minecraft Preview
- Adjusted Trial Spawner and Vault block emissivity
> Lower parts on the vault block and upper parts on the trial spawner now emit more light for a more natural look. Off states now glow more strongly (however only the vault block emits an aura of light to match the vanilla game). On states' emissive parts are now much stronger.

- Adjusted all brick-type blocks' normal maps (e.g. stonebricks, deepslate tiles and bricks, mud bricks, etc.) to look better during sunrise, fixed all netherbricks' normal maps
- Updated sandstone and carved sandstone normal maps to have a consistent logic with similar blocks
- Revamped mycelium, with new materials, new smoother seamless normal maps, and better heightmaps
- Revamped spore blossom
> New heightmaps and normal maps. The base texture is now consistent with Azalea leaves, with nerfed emissivity.

- Revamped Stone diorite, granite, and andesite
> Improved diorite details and increased the overall roughness of all 3. New smoother normal maps with better tiling and improved heightmaps.

- Fixed jarringly dark pixels on Cobblestone and Mossy Cobblestone normal maps that would appear during sunset and sunrise
- Improved all wooden logs' and stripped variants' top normal maps with better details
- Reworked the warped door heightmap, fixed incorrect height of some pixels on the crimson door heightmap
- Revamped grass path to have a similar style to grass block, now much more detailed with improved normal maps and heightmaps
- Updated chiseled stonebrick normal map to match the style of other stonebrick types
- Updated cracked stonebrick heightmap with better defined cracks
- Updated prismarine bricks, top and left sides are no longer considered a part of the mortar
- Updated hanging roots and root parts on rooted dirt with new detailed materials
- Updated French translations for better accuracy (thanks MazeWave)
- Other changes and fixes
> - Nerfed redstone block emissivity so it may no longer be viable as a light source in large chunks (it still passively emits a small amount of light to accommodate consistency between redstone components)
> - Updated redstone dust heightmaps, no more distorted edges
> - Improved tuff bricks and chiseled tuff bricks heightmaps
> - Fixed an incorrect pixel angle on the grass side normal map
> - Updated mossy stonebrick heightmap, fixed noise and established a consistent logic between every stonebrick variant

### Experimental Option

- Fixed Mooshroom mushrooms being invisible with ray tracing
> The missing mushrooms have been remodelled on top of the mooshroom for ray tracing in this workaround, as such they may not perfectly line up with the original mushrooms, which results in duplicate mushrooms appearing without ray tracing. It is worth noting that in vanilla Minecraft mushrooms float over the cow's body, this workaround fixes that too.

- Changed the Breeze's material that caused the glass-like appearance of its wind body, Breeze wind animations are now functional
- Updated the fix for the Warden's black ears and chest with ray tracing, now fully fixed without the glass-like ears (MCPE-157438)
- Fixed the glass-like wind charge projectile with ray tracing, they now appear solid with working animations
- Fixed Wither Boss armor animation with ray tracing (MCPE-141530)
- Fixed in-world item textures appearing red/yellow for Sniffer, Breeze, Armadillo, Bogged, Allay, Axolotl, Camel, Ender Dragon, Frog, Glow Squid, Goat, Hoglin, Iron Golem, Piglin and Piglin Brute, Polar Bear, Snow Golem, Strider, Tadpole, Trader Llama, The Warden, Wither Boss, and Zoglin, by manually defining the item textures for them
- Added particle modifiers for all particles in game, all particles have been adjusted and now appear less opaque where needed
> For instance, while particles like lava will remain fully opaque, other particles like rain or block destruction now blend in with their background. Particles are not ray traced, and this can lead to drastically improved visuals while using ray tracing.

- Fixed the chiseled bookshelf front appearing glossy (MCPE-166159)
> Book textures are not yet dynamic, right now the on or off state is displayed only depending on the direction the block is facing, this is still an improvement over a glossy texture without any PBR textures at all.

- Fixed kelp bottom not using a PBR texture (now uses the kelp top texture instead)
- Brightened all doors by varying degrees, as a counter to MCPE-121412
- Added decorated pot fixes for all 3 new pottery sherds in Minecraft Preview (MCPE-167161)
- Fixed the Experimental option causing redstone ore reactivity to break, moved the reactivity functionality of redstone ores exclusively to the Experimental option
> This was previously part of default Vanilla RTX, however it has shown to cause missing textures in some servers and with some add-ons and their resource packs. Redstone ores' textures will now permanently remain in a non-lit state, which passively emits a tiny amount of light like all other redstone components. It is now required to switch to the Experimental option if you wish redstone ores to light up when interacted with or walked on.

- Updated the spyglass overlay bug workaround, removed the fix for the texture being too zoomed in, and instead modified only the problematic parts of the texture that caused two darker squares to appear on screen
> Spyglass zoom now functions more similarly to Java mods like OptiFine zoom, without an overlay texture, with ray tracing. Unlike the previous workaround, this one no longer causes the texture to be too zoomed out without ray tracing.

### Notes

> Some of the features here were previously included in Minecraft RTX Fix Pack. For this update, Minecraft RTX Fix Pack has been updated for the latest Minecraft versions and merged into the Experimental option of Vanilla RTX. Minecraft RTX Fix Pack is now discontinued.

---

## 1.21.10

*Trial Chambers quality update, 29 languages, animated lava.*

This is a huge quality update for Vanilla RTX 1.21, numerous blocks have been reworked and tweaked for better quality and improved consistency. Support for the 1.21 Vault block has also been added.

### Changes

- Added complete support for the Vault block of the Trial Chambers
> To accommodate consistency between Trial spawners and the vault block, inactive states now emit a tiny amount of light.

- Added multi-language support for all available languages (29)
> Pack menu texts were also improved. Translations might not be perfect, if you are a native speaker and find the translation for your language to have a problem or sound odd, please open an issue on GitHub suggesting a better translation.

- Revamped composter, now consistent with podzol and other wood blocks, with reworked heightmaps and normal maps
- Updated Lectern, now fully consistent with other wood blocks, books are now consistent with the bookshelf, golden parts now match gold
> Revamped heightmaps with improved edges, and revamped normals.

- Updated bookshelf heightmap, the height differences of books are now based on the average pixel brightness of each book for a more natural look, with added missing details
- Revamped Lava, now with proper animations!
> Previously, emissivity was based on the average of all stages of lava to make up for the lack of animated MER support. Now that animated MERs are once again functional in Minecraft after years, the new emissivity follows lava's texture animation. The new lava appears more vibrant and more faithful to vanilla Minecraft. Also added a subtle normal map to Lava in Vanilla RTX Normals.

- Updated Barrel
> Revamped normal maps, improved heightmaps, and updated wooden parts material to be consistent with other wooden blocks.

- Updated podzol on dirt podzol
> Revamped heightmaps, improved normal maps with better tiling, and new redefined materials.

- Revamped Lodestone, with all new normal maps, improved heightmaps, and new materials
- Flattened smooth stone slab normals to match smooth stone
- Updated old stonecutter top and side normal maps
- Revamped new stonecutter
> New saw material animation that follows the saw texture. Freshly designed normal maps and improved heightmaps. Updated materials, iron, wooden, and stone parts are now fully consistent with other blocks.

- Updated all hardened clay materials, now much more rough with less contrast for a less distracting and subtle look
- Revamped Brewing stand
> New materials, iron parts are now consistent with other iron of the same class/type, and rod emissivity has been tweaked. New normals and improved heightmaps.

- Snowy grass side now connects more seamlessly with the snow block above it, also improved its heightmap to fully match the snow heightmap
- Improved cobblestone and mossy cobblestone normal maps
- Added more details to the Netherrack mortar MER
- Reworked crimson and warped Nylium
> New materials, crimson nylium top is now consistent with netherrack. Reworked heightmaps and new subtle normal maps with better tiling.

- Revamped all crimson and warped foliage (vines, roots, and sprouts)
> Now fully consistent with crimson and warped nyliums, with improved heightmaps and normal maps.

### Experimental Option

- Improved sun azimuth in experimentals
> Fixed the bug of the sun texture and the directional light of the sky appearing to come from opposite angles during sunrise and sunset, and improved the sun path with smoother and more natural transitions. The moon now rises and sets from the opposite azimuth angle than the sun. This newer version has smoother transitions, and the offsets are less extreme compared to vanilla Minecraft, helping retain the vanilla feeling and avoiding making it feel like the north pole.

- Fixed the spyglass overlay texture
> Previously too zoomed in with ray tracing enabled, the texture was converted for ray tracing mode. This fix comes with a drawback: the spyglass overlay texture now appears too zoomed out without ray tracing. The fix is only meant for the ray tracing graphics mode, and disabling ray tracing will break the spyglass overlay texture.

- Added an incomplete fix for dark areas on The Breeze, Wind Charge, and The Warden mobs
> These fixes are not yet complete, however for the time being they are an improvement over the issues posed by the game. More of the game's issues will be addressed through various workarounds in upcoming updates, keep an eye out in the Experimental section of the changelogs.

---

## 1.21.0

*Crafter, Trial Spawner, and the new copper family.*

### Changes

- Added complete support for the Crafter block, with all-new hand-made normal maps and fully consistent materials with iron, redstone, and wood blocks
- Added support for the new family of Copper blocks
> Fully consistent with older copper blocks, with new hand-painted normal maps for all new copper blocks.

- Added full support for the Trial Spawner
> Consistent with the new Mob Spawner.

- Revamped Mob Spawner
> Now in line with other dark metals, with a completely reworked heightmap and normal map.

- Updated all copper and cut copper blocks' heightmaps, to allow a consistent logic between old and new copper blocks
> Updated some of their normal maps as well for the same reason.

- Updated the iron parts on all door hinges, handles, and all trapdoors
> All metal parts on doors now match other dark metal materials (such as Hoppers and Cauldrons), now with more details and fully consistent. The golden handle on the dark oak door now matches gold block and other gold materials.

- Updated all door heightmaps to be in line with one another, with improved logic
- Updated Blast Furnace, improved iron parts to better match the crafter and other iron materials, improved heightmaps
- Updated Glowing Obsidian
> Now fully consistent with other Obsidian blocks. Now emits more light to better match the vanilla Minecraft light level of glowing obsidian. Improved normal map and heightmap.

- Improved the appearance of Frogspawn
- Enchanting Table now gives off a small amount of light
- Adjusted Lantern emissivity
- Improved Glow Lichen emissivity
- Improved mossy cobblestone normal map (fixed some pixels appearing too dark from certain angles)
- Improved rough prismarine normal map (mortar parts)
- Performed a texture update check
> 4 blocks were found to have different file sizes (likely minor differences, with some pixel color values being off by no more than 1 RGB value). The Snow block side was found to be based on an older texture, PBR textures were changed accordingly in this update to reflect the new texture and correct many pixels.

---

## 1.20.5

*Autumn's End. The launch of the Experimental option and dynamic sun azimuth.*

### Experimental Option

- Launch of the Experimental option
> This is a new subpack which will be used for anything experimental from here on out. Future features in the Experimental subpack might not be intended for everyday gameplay, so they may or may not be added to Vanilla RTX. Think of it as a playground for testing and exploration, keep an eye out on the changelogs for information on what's new in Experimental. You can enable this option through the updated resource pack settings menu.

- Implemented dynamic sun azimuth, for the first time ever in Minecraft RTX! This allows diagonal shadows and a more dynamic day-night cycle, bringing more realistic outdoor lighting
> The previous sun angle was at 0°, which led to shadows lining up with blocks, resulting in far less than ideal visuals. The new sun azimuth makes diagonal godrays/shadows possible, and sunlight now passes in various directions instead of being parallel with the entire Minecraft world, making the environment much more dynamic.
>
> Vanilla RTX is the first resource pack ever to introduce this feature without external modifications to the game's files or memory. Unlike older methods, which involved modifying the game's files or memory with each restart or Minecraft update, all you have to do is enable the Experimental option of Vanilla RTX through the resource pack's settings. No extra world experimental option or preview version is required either.
>
> Known issue: at certain times of day, the sun's directional light may momentarily appear to come from the opposite direction, this will be addressed in a future update.

- Implemented a workaround fix for decorated pot texture glitches

### Changes

- Default materials for unsupported textures will now appear fully rough
- Prismarine has undergone a major overhaul with significant improvements
> - Materials for all prismarine blocks (Sea lantern, rough prismarine, prismarine bricks, and dark prismarine) have been revamped
> - Rough prismarine now boasts more details
> - Consistency issues between prismarine blocks have been resolved, all prismarine blocks now share a unified appearance
> - Incorrect height values on the rough prismarine heightmap have been corrected
> - Prismarine bricks and Dark Prismarine normal maps have been revamped, angles on dark prismarine have been fixed and perfected, and prismarine bricks now sport a completely new look

- End Portal material no longer appears glossy, it is now pitch black instead
> It is not possible to faithfully recreate the green moving dots of default graphics, however a void black replacement can still be thought of as a suitable alternative to the (likely unintentional) default oily material.

- Updated the manifest and metadata, and restructured Vanilla RTX
> Added the URL and License of the official repository, and new PBR capabilities required for the new experimental features.

- Added a new short, comprehensive description of each subpack in the resource pack settings menu, which can be viewed underneath the slider while changing subpacks
- Modified all texture set jsons within the package to be in a correct and human-readable json format
- Updated mushroom blocks (stem, red, brown, inside, and red/brown fungi)
> Normal maps have been overhauled for better natural aesthetics and improved tiling. Decreased all heightmap contrast with more subtle details. Updated MERs and filled in missing details, all mushroom blocks now appear consistent.

- Revamped Observer
> Different types of stone parts and redstone parts now match their respective materials. Remade all heightmaps along with new hand-made normal maps to be up to standard.

- Updated the mortar texture parts on cobblestone related blocks (such as Pistons, Dropper, Dispenser, Furnaces, etc.) for enhanced detail and consistency
- Fixed an issue with tall seagrass top and bottom normal maps appearing disconnected, similar issues with Kelp top were also addressed, and missing information for some normal maps has been filled in
- Adjusted regular bricks and pots roughness to more closely match other types of bricks
- Updated Cobblestone and Mossy Cobblestone MERs, added in missing details
- Corrected a wrong emissive pixel on the sculk catalyst side
- New icons

---

## 1.10

*Cherry Grove.*

### New

- Added full support for the cherry wood set (planks, doors, logs, etc.)
- Added support for cherry leaves and petals
- Added unique fog for the Cherry Grove biome: water colors match vanilla Minecraft, and the air color is similar to the Vanilla RTX default with a subtle pink tint
- Added support for Suspicious Sand
- Added support for Suspicious Gravel
- Added support for Torchflower

### Changes

- Updated sand and red sand to better match their texture (MERs), improved normal maps
- Revamped waterlily
- Revamped Dripleaf and Small Dripleaf
> Improved normal maps and heightmaps, and updated materials to better match other foliage.

- Adjusted cactus MERs
- Updated gravel
> Updated MERs to match the stone block, improved normal maps with better tiling, and better heightmaps to allow consistency between gravel and suspicious gravel.

- Adjusted all wooden plank heightmaps (less intense)
- Changed the concrete normal maps' color format to RGB from index

### Known Issues

- The big dripleaf top normals are inverted depending on the direction the big dripleaf top is placed

---

## 1.9.0

*Redstone overhaul, polished and smooth blocks.*

The latest update brings the final refinements to bamboo blocks, revamps redstone, and improves all polished/smooth blocks by making them more consistent and better looking, along with numerous improvements to other blocks.

### Changes

- Full redstone overhaul (e.g. redstone block, redstone parts on comparator, repeater, rails, redstone dust, redstone torch, observer, etc. are all affected), every block/item with redstone has been revamped
> - The light that rails and other redstone components emit now better matches the vanilla game (e.g. light emitted by non-light-emitting blocks in vanilla Minecraft is no longer considerable/is significantly weaker)
> - All non-active redstone blocks and items now passively emit a tiny amount of light, to make up for consistency between redstone dust and other components, which have to emit light at all times
> - Reworked and unified all redstone MERs with new and improved materials (redstone is made of Uranium and Carbon, the new materials reflect this fact to some extent)
> - Adjustments to lit redstone ore emissivity

- Bamboo updates
> - Improved bamboo planks, bamboo block, stripped bamboo block, bamboo fence, and fence gate heightmaps
> - Fixed edges on bamboo fence, fence gate, and stem heightmaps
> - Updated the bamboo block and stripped bamboo block top textures to match the latest betas, and made necessary adjustments

- Polished and smooth block changes
> - Updated all polished blackstone blocks to fully match each other (polished blackstone bricks, cracked variant, polished blackstone, and chiseled blackstone), all now use consistent materials
> - Improved cracked polished blackstone bricks heightmap
> - Adjusted chiseled deepslate and polished deepslate MERs, with better detail
> - Updated smooth stone MERs (now the same between Vanilla RTX and Vanilla RTX Normals), much more detailed and more consistent with deepslate smooth stone
> - Improved the detail of smooth granite, andesite, and diorite

- Updated Rails
> - Redstone parts are now fully consistent with redstone
> - The stone part on the detector rail now matches stone
> - Updated golden parts to fully match gold block
> - Updated iron parts to fully match other iron blocks
> - Wooden parts now match other woods

- Updated iron bars to better match other iron blocks
- Adjusted Netherbrick blocks' MERs (Netherbrick, Cracked Netherbrick, Red Netherbrick, and Chiseled Netherbrick), smoother MERs and less contrast
- Updated all blackstone and gilded blackstone PBR maps to match their newer texture, improved MERs to better fit in with the rest of the blackstone blocks
- Revamped fletcher table, with new MERs to fully match birch planks, and new heightmaps and normal maps
- Revamped cartography table, with more detailed and consistent MERs (for instance, iron parts on the compass and gold parts are now consistent with their respective materials), new normal maps, and improved heightmaps
- Revamped Loom, with new detailed MERs, new hand-painted normal maps, and new heightmaps
- Updated wooden parts on the smithing table to better match mangrove planks, and corrected the smithing table bottom, metal parts now appear metallic
- Revamped Seagrass and Kelp (foliage)
- Updated beacon emissivity, now much more subtle
- Updated target block MERs
- Updated chiseled bookshelf texture names to match the latest beta
> Known issue: book textures do not display correctly, this is half-fixed in an upcoming Minecraft RTX Fix Pack update.

- Fog changes
> New water fog in the mangrove biome which is much closer to vanilla water colors, and other adjustments to mangrove air fog.

- Minor adjustments to glazed terracotta
- Basalt updates
> Smooth Basalt, Polished Basalt, and regular basalt now use consistent and improved MERs. Reworked normal maps and improved heightmaps for all basalt blocks.

- Updated icons (the Vanilla RTX Normals icon is now made using Vanilla RTX Normals)

### Notes

> This update touches many things that desperately needed an update for a long time to be up to Vanilla RTX standard. Future updates will likely focus more on bringing support for new content rather than improvements.

---

## 1.8.0

*Water, ice, snow, and fire revamp.*

### Changes

- Revamped water
> The new water texture is as faithful to vanilla water as it can possibly be, which also results in slightly clearer water reflections.

- Decreased the default End fog density
> This results in slightly better vision and a brighter environment.

- Added support for bamboo block and stripped bamboo block
- Updated scaffolding MERs to fully match other bamboo blocks (also updated to its newer texture)
- Updated bamboo plant stem MER to better match the non-stripped bamboo block
- Made necessary adjustments to bamboo planks to match its newer texture
- Ice rework
> New and improved smooth normal maps, better and logically consistent heightmaps, and reworked MERs with more detail, slightly glossier, resulting in better reflections. Blue ice no longer emits light with ray tracing (since 1.17.10 blue ice no longer emits light in the vanilla game).

- Snow rework (Snow, Powder snow, Snowy grass)
> Revamped MERs, now fully consistent with each other and slightly rougher. Smoother normal maps, and new and much more subtle heightmaps. Snowy grass PBR textures now properly match snowy grass.

- Netherrack rework
> Crimson/Warped Nylium side, nether gold, and quartz ores normal maps are now much smoother, with minor adjustments to heightmaps (netherrack parts only).

- Adjusted magma block emissivity, now more detailed per pixel
- Revamped all fire and campfire fire MERs
> New MERs are based on the averaged RGB value of all animation phases combined. Soul fire now appears significantly dimmer than regular fire.

- Reworked quartz pillar normal maps
- Reworked redstone block top normal map
- Improved jukebox and noteblocks
> The disk insertion spot on the texture now absorbs more light, making it appear darker. Fixed noise on their heightmaps and reworked normal maps.

- Redefined materials for certain black irons, now fully consistent and more detailed
> Reworked iron parts on Smithing Table MERs. Reworked Chains and iron parts on Lanterns.

- Reworked smithing table normal maps and heightmap
- Improved lantern and soul lantern emissivity (overall dimmer), updated heightmaps and normal maps
- Reworked the normal maps of all ore parts on all ores (e.g. the gold or emerald parts on emerald or gold ore)
> Every ore now has a concave-shaped normal map on its ore parts, making them appear smoother (this will be followed up by a glowing ores update).

- Updated chains normal maps and heightmaps
- Berry revamp
> Updated Glow Berries emissivity, overall dimmer to retain vanilla colors. Updated every texture with berries in it (Glow berries, Sweet Berries, Berries on cake top), now fully consistent. Updated glow berries and sweet berry bush MERs to better match leaves/other foliage, now much more detailed. Revamped all of their normal maps and heightmaps.

- Revamped crimson/warped log side and crimson/warped stripped log side normal maps
> Now better matches other log variants and is much smoother.

- Improved all dripstone normal maps, reworked dripstone block normal map
- Fixed 2 pixels with wrong height on the crying obsidian and respawn anchor bottom heightmap
- Increased pebble roughness on all textures with dirt (e.g. farmland, dirt, grass side, etc.)

---

## 1.7.8

*Copper, command blocks, and a texture parity pass.*

### Changes

- Added full support for "Next Major Update" blocks in Minecraft Preview
- Revamped copper and cut copper (stage 0) MERs
- Updated non-oxidized parts on copper ores and raw copper to fully match the copper material, the lightning rod is now more detailed and matches copper, adjusted lightning rod heightmap and normal map
- Oxidized parts on the raw copper block now match other copper oxidization stages
- Improved all 16 colors of glazed terracotta MERs, now much more detailed, with fully reworked normal maps
- Improved bamboo and bamboo leaves normal maps and heightmaps, now much softer, with other corrections/fixes
- Revamped all command block normal maps, improved heightmaps, reworked MERs, now much more detailed
- Reworked hopper outside normal map
- Updated 16 base textures with different file sizes compared to vanilla resources
> This eliminates any possible unintended disparity (e.g. the inside of the cauldron, which had been flipped, or weeping vines, which now have a blue tint). PBR maps were updated where needed to match the new textures.

- Added support for structure air, improved structure void
- Decreased cave vine emissive intensity (glow berries)
- Revamped structure block and jigsaw block, with improved normals and heightmaps, new and detailed MERs, jigsaw and structure blocks are now fully consistent
- Improved iron parts on the smoker front on and off, now matches other iron blocks
- Adjusted lava emissivity, pixels that are overall darker during the animation now emit slightly less light
- Revamped Kelp block, now much more detailed
> I am aware of the reflective bottom texture issue, a fix will be included in an upcoming patch.

- Optimized pack file size
- Adjusted scaffolding top normal
- Updated flowerpot to fully match the brick block's roughness values
- Updated bookshelf to match chiseled bookshelf

---

## 1.7.7

*Respawn anchor, glowstone, logs, sculk, and foliage.*

### Changes

- Fully revamped respawn anchor, now much more detailed and fully consistent with crying obsidian/obsidian
> Fixed the off/on stages of the side and top not matching, and darkened the holes on the side/top. The glowstone charge indicator on the respawn anchor is now fully consistent with Glowstone.

- Fixed 2 pixels that shouldn't be emitting light on crying obsidian, and decreased the overall emissive intensity
- Updated glowstone, it is now more metallic (as it is made of Boron), with a reworked normal map and vastly improved emissivity
- Reworked shroomlight, with a better heightmap, smoother normal map, and vastly improved emissivity (also closer to the emissivity of glowstone)
- The entire sculk tendril now lights up when activated, new PBR maps for the sculk tendril are based on the average of 16 stages of its animation
- Fixed consistency issues of the sculk sensor, now fully matches other sculk blocks, with adjustments to other sculk blocks' emissivity
- Inverted the sculk shrieker top normal map/heightmap (they used to display incorrectly in game), darkened the top and side
- Adjustments to mountains fog, fog used to be unnoticeable at high heights in certain mountain biomes, and is now overall denser
- Revamped crafting table MERs, now much more detailed and consistent with wooden planks, with a revamped normal map and heightmap
- Redefined all white/bright iron block materials (e.g. iron block, door, trapdoor, iron parts on crafting table)
- Fixed the sandstone top normal map (had an issue exposed during sunset and sunrise), improved heightmap (now more subtle)
- Increased planks roughness (Vanilla RTX is affected more by this change)
- Updated compound creator, element constructor, lab table, and material reducer normal maps
> 21 new hand-painted normal maps replacing the placeholder ones added in v1.7.4. Fixed a wrong pixel on the material reducer top. Now fully consistent and much more detailed.

- Improved grass top/side roughness
- Updated all remaining land foliage blocks/flowers (29 textures) MERs to match the roughness of grass (the tops of flowers and the flowers themselves now have detailed, consistent roughnesses across all flowers)
- Updated flowers heightmap/normal map, now more subtle, and inverted the sunflower normal and heightmap to display correctly in game
- Adjustments to Diamond block MER (also applies to diamond parts on the enchanting table)
- Updated all log/stripped log top roughness to fully match planks in Vanilla RTX and Vanilla RTX Normals
- Updated all non-stripped log sides and edges of log tops to fully match each other, and increased overall roughness
> This also eliminated any wrong pixel that was due to different variations of logs using the same MER (e.g. dark oak and oak log). It turns out the shading of some of these blocks is slightly different, now no two logs share the same MER. Edges of log tops are now fully consistent with their side textures, and log roughness is now fully consistent across different log types.

- Updated all stripped log sides and tops, edges and sides are now consistent and fully match their wooden planks, and the stripped dark oak log MER and heightmap are no longer mismatched
> The new stripped log MERs are the same between Vanilla RTX and Vanilla RTX Normals, despite planks having different roughness between packs, but are based on the average of planks from both packs. The reason behind the stripped log changes is notable: log tops use the same colors as planks, and edges of stripped log tops have colors close to log tops, which means stripped logs should be closer to planks and more consistent with the top of logs.

- Improved glow lichen roughness, adjusted its normal map, and improved and inverted its heightmap to display correctly in game (it used to be inverted)
- Adjustments to calcite roughness, with a new and smoother normal map
- Minor detail improvements to all wool MERs
- Removed 22 unused files
- Updated hopper inner to better match the hopper side
- Adjustments to portal emissivity, the new MER is based on the average of all 32 phases of the animation, which means pixels that are darker during the full animation cycle will emit slightly less light
- Reworked crimson and warped fungi, they now match wart blocks, and emissive pixels are now much dimmer
- Updated Vanilla RTX and Vanilla RTX Normals pack icons

---

## 1.7.6

*Vanilla RTX Normals split into two packs.*

This release separates Vanilla RTX Normals into two packs:
- **Vanilla RTX Normals**: the original look of the pack, using 16x normal maps
- **Vanilla RTX**: bumpy pixelated textures using 16x heightmaps

### Changes

- Both packs (previously subpacks) now feature a fogless resource pack option, which allows you to remove all of the air fog through resource pack settings, distance and water fog are untouched
- Added unique fog for Mushroom Islands, water color now matches the vanilla game with ray tracing
- Adjustments to density values across most of the fog configurations
- Revamped all dirt normal maps, now subtle and consistent across all blocks which have dirt in them
- Revamped campfire logs: coal parts now match coal block, wooden parts now match oak log, along with better emissive on the fire parts
- Updated stonebrick, cracked stonebrick, and mossy stonebrick MERs
> Cracked stonebrick and stonebrick used to use a similar MER, even though their textures aren't the same (cracks), they are now fully consistent and match their own respective textures.

- Updated mossy stonebrick, mossy cobblestone, and moss block to be consistent
- Updated cracked stonebrick heightmap, fixed a few wrong pixels
- Updated dirt podzol: better side and top heightmap, updated top normal map
- Revamped reeds
- Updated end rod, the end rod base is now metallic
- Revamped fern and large fern, now consistent with grass
- Inverted the sculk vein normal map and heightmap (they used to display incorrectly in game)
- Updated cobbled deepslate MER: better mortar MER
- Fixed the lapis ore heightmap (its texture was updated in one of the newer Minecraft textures)
- Updated grass snowed side heightmap and MER to match its newer texture
- Fixed a pixel which appeared too bright on the chemical heat block
- Decreased all concrete blocks' roughness contrast and decreased overall roughness

## Pre 1.7.6
> Prior to `1.7.6` there were tens of updates, notably
`1.7.5`
`1.7.4`
`1.7.3`
`1.7.2`
`1.7.1`
`1.7.0`
`1.6.X`
`1.5.X`
`1.4.X`
`1.3.X`
`1.2.X`
`1.1.X`
`1.0.0 (Initial relesae)`
> Eeverything before 1.7.6, and a few other versions along the way are missing from this history. They'll be added if they turn up. Modern direction of Vanilla RTX was settled starting with `1.6.0`, some parts to this day use assets from that time.

