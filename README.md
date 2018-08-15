﻿# Kerbal Health

This mod introduces many aspects of astronauts' health management to KSP. It makes the game more challenging but also more realistic, encourages smarter mission planning, and adds to the fun. It works well alongside most popular mods.

**Features**

- Every kerbal has Health Points (HP).
- Maximum HP increases with kerbals' level. A newbie has 100 HP while a 5-level kerbal has 150.
- Kerbals' HP change, including in the background and in timewarp, based on a range of factors such as living space, presence of crewmates, gravity, and specific ship parts. E.g., a level 1 kerbal will typically survive 11 days in a 1-man pod before becoming exhausted and turning into a Tourist.
- Kerbals need time to recuperate at the KSC between flights to restore full health.
- If a kerbal's health goes under 20%, he/she is exhausted and becomes a Tourist. They will go back to work when health grows back to 25%.
- If a kerbal's health falls to 0, he/she dies!
- Kerbals experience radiation, both cosmic and artificial, which permanently affects their maximum health.
- You can protect from radiation by using shielding and choosing safer mission profiles. Planets and moons can reduce radiation with their magnetic fields, atmospheres and occlusion, to various degrees.
- When kerbals level up, they can acquire quirks that affect their health reactions, to the better or to the worse.
- Kerbals may fall sick, have health accidents or panic attacks: prepare for contingences!
- Health Monitor lets you check on all your kerbals in KSC and in flight.
- Health Report in Editor helps design comfy and healthy craft.
- A configurable low health alert will warn you when you are about to lose a kerbal.
- Compatibility patches support a range of parts mods (see below).
- All of these settings are easily changed or disabled in-game and with ModuleManager patches.

**Health factors**

The following factors may affect kerbal's health:
- Assigned (kerbal is on a mission): -0.5 HP/day
- Crowded (scaled effect): -3 x <Crew> / <Living Space> HP/day (Living Space is provided by most crewed parts, depending on their size, capacity, function etc.)
- Loneliness (only 1 kerbal in the vessel, badass kerbals are immune): -1 HP/day
- Microgravity (orbital or suborbital flight or under 0.1 g conditions, e.g. Minmus): -0.5 HP/day
- EVA: -10 HP/day
- Sickness (the kerbal is marked as Sick, cures after some time): -5 HP/day
- Connected (having a working CommNet connection to home): +0.5 HP/day
- Home (on Kerbin below 18 km altitude): +2 HP/day
- KSC (kerbal is recuperating in KSC, i.e. available): +5 HP/day

These values, like most others in the mod, are adjustable in Difficulty Settings. They also depend on quirks of a particular kerbal. You can check current values for a specific crew member in Health Monitor.

Certain parts (Hitchhiker, crew cabins, and the Cupola + many provided by mods) can additionally reduce the effect of a health factor (Crowded in this case) allowing for much longer and healthier flights. It often requires EC though. Hab rings in some mods can help overcome Microgravity issues for long-term stations and interplanetary missions. All these features can be changed using ModuleManager patches.

**Health Recuperation and Health Decay**

Certain parts (such as the Cupola) provide Recuperation bonuses. If a kerbal receives, say, a 1% recuperation bonus, he/she will recover 1% of their lacking health (i.e. of the difference between their current HP and the maximum HP) every day. This change works in parallel with the normal health factors above.

*Example: A 5-star kerbal (maximum HP = 150) currently has 40 Health Points and is in a vessel that gives him 1% recuperation. The vessel has 10 units of living space and he has connection and he has a crewmate. Therefore he recovers (150 - 40) x 1% = 1.1 HP per day and loses also (0.5 + 3 x 2 / 10 + 0.5 - 0.5) = 1.15 HP per day. It means that the marginal change balances out the "normal" change and his health will stay around 40 HP (27%) until the situation changes.*

As you see, this mechanics may allow some kerbals to stay relatively healthy indefinitely. It may look cheaty, but the point is that: (1) there should be a way to design long-term missions without spamming crew space, (2) it requires a lot of heavy parts and therefore still difficult, (3) the balanced health level is usually far from 100% and may fall lower if circumstances change (e.g., new crew arrives and fills the station), (4) these bonuses require a lot of EC, (5) radiation still keeps mounting (see below).

Note that, since v1.1, Recuperation is not stacked and has crew cap. It means that one Cupola provides 1% Recup for 2 kerbals, 2 Cupolas give 1% for 4 kerbals (not 2%!), etc. If you have more kerbals than the crew cap, Recuperation will be split among them evenly (e.g. 4 kerbals with 1 Cupola will get 0.5% Recup).

Decay is the opposite to Recuperation: for every percentage point of Decay, your kerbal will lose 1% of their remaining health per day. Fortunately, it is very rare.

**Radiation**

All kerbals on missions are affected by radiation, which slowly but permanently reduces their maximum HP. Radiation is measured in banana equivalent doses (about 1e-7 Sv), or simply bananas. 1e7 (10,000,000) bananas reduce max HP by 25%; 4e7 bananas kill a kerbal. Currently, there is no way to reduce the dose.

The amount of Radiation a kerbal receives depends on many factors. Most importantly, it is determined by their location. Many planets and some moons have magnetic fields that stop some radiation; atmospheres are also very effective in shielding it (see [wiki](https://github.com/GarwelGarwel/KerbalHealth/wiki/Radiation) for more). Being close to a celestial body helps screen some rays too. E.g., radiation level at Kerbin's sea level is 1,000 times lower than in interplanetary space just outside Kerbin's SOI. Cosmic radiation is also greater closer to the Sun. Being on EVA takes away all the protection your ship provides and dramatically increases radiation level. Artificial radiation is created by certain parts like atomic engines and nuclear reactors.

You can protect kerbals from radiation (both cosmic and artificial) by adding shielding to the vessel. It is provided by some parts, like structural panels, heat shields and mk3 cargo bays. These parts and most crew pods can be improved by adding Radiation Shielding to them in the Editor. You can never eliminate all radiation, but you can reduce it to non-dangerous levels.

**Quirks**

Whenever a kerbal levels up, there is a 25% chance that he or she will acquire a health quirk (unless he/she already has two). Discovering an anomaly can also grant a free quirk. These can be positive or negative and usually affect kerbals' vulnerability to various health factors and dangers. Chances of getting some quirks depend on courage and stupidity of a particular kerbal. The [full list](https://github.com/GarwelGarwel/KerbalHealth/wiki/Quirks) can be found in the Kerbal Health Wiki.

**Random events**

Kerbals' organisms, like ours own, are not always predictable. Sometimes, quite rarely, you may see random events that can impact your whole mission. Now you need to prepare for contingencies like real space programs do. You may completely disable or fine-tune the event system in settings.

- Sickness/Curing: a kerbal can become sick and start losing health quickly. This condition heals itself after some time, but you may have to evacuate the kerbal to KSC (or bar him/her from flights) before their health falls too low. On average, kerbals catch flu once every 200 days and cure after 20 days or so. Note that these diseases have incubation periods, so it may be wise to quarantine kerbals for several weeks before sending them on an interplanetary trip.

- Panic Attack: when your kerbal's is on a mission, he/she may epxerience a panic attack and become uncontrollable for up to 3 hours. This event's probability depends on the kerbal's health (the lower, the more likely) and courage (the lower, again, the more likely) of the kerbal, the maximum average frequency is once per 100 days.

- Accident: your kerbals loses a random percentage of their current health (20 to 50%). This event's chance depends on kerbal's stupidity, but generally happens very rarely (every 1,000 days on average with 50% stupidity). However, it can become an important factor for very long missions.

**Requirements**

- [Module Manager](https://forum.kerbalspaceprogram.com/threads/55219)

**Supported mods**

Kerbal Health should work well alongside most other mods and will try to adapt to them with smart MM patches. Some have better, manually balanced support though:

- [B9 Aerospace](https://github.com/blowfishpro/B9-Aerospace)
- [Blizzy's Toolbar](http://forum.kerbalspaceprogram.com/index.php?/topic/55420-120-toolbar-1713-common-api-for-draggableresizable-buttons-toolbar/)
- [Bluedog Design Bureau](https://forum.kerbalspaceprogram.com/index.php?/topic/122020-131-bluedog-design-bureau-stockalike-saturn-apollo-and-more-v141-атлас-1jan2018)
- [Deadly Reentry Continued](https://forum.kerbalspaceprogram.com/index.php?/topic/50296-122-deadly-reentry-v760-june-9-2017-the-ariel-edition/)
- [DeepFreeze Continued](http://forum.kerbalspaceprogram.com/index.php?/topic/112328-11-deepfreeze-continued)
- [Deep Space Exploration Vehicles](https://forum.kerbalspaceprogram.com/index.php?/topic/122162-14x-deep-space-exploration-vessels-build-nasa-inspired-ships-in-ksp/)
- [FASA](http://forum.kerbalspaceprogram.com/index.php?/topic/22888-105-fasa-544/)
- [Kerbal Atomics](http://forum.kerbalspaceprogram.com/index.php?/topic/130503-10511-kerbal-atomics-fancy-nuclear-engines-initial-11-test/)
- [KPBS](http://forum.kerbalspaceprogram.com/index.php?/topic/133606-130-kerbal-planetary-base-systems-v144-6-june-2017/)
- [KSP-AVC](http://ksp-avc.cybutek.net)
- [KSP Interstellar Extended](https://forum.kerbalspaceprogram.com/index.php?/topic/155255-12213-kspi-extended)
- [Malemute](https://forum.kerbalspaceprogram.com/index.php?/topic/139668-13-the-malemute-rover-020/)
- [Outer Planets Mod](https://forum.kerbalspaceprogram.com/index.php?/topic/165854-ksp-142-outer-planets-mod221-15-april-2018/)
- [RLA Reborn](https://forum.kerbalspaceprogram.com/index.php?/topic/175512-14-rla-reborn/)
- [Spacetux Recycled Parts](https://forum.kerbalspaceprogram.com/index.php?/topic/164829-131-spacetux-industries-recycled-parts/) (Atomic Age, FTmN, FTmN-New, RSCapsuledyne)
- [SpaceY Heavy Lifters](https://forum.kerbalspaceprogram.com/index.php?/topic/90545-12213-spacey-heavy-lifter-parts-pack-v116-2017-01-30/)
- [SSTU](https://github.com/shadowmage45/SSTULabs)
- [Tundra Exploration](https://forum.kerbalspaceprogram.com/index.php?/topic/166915-143-tundra-exploration-v113-may-31st-stockalike-spacex-falcon-9-dragon-v2-and-bfr/)
- [USI Kolonization Systems (MKS/OKS)](https://github.com/BobPalmer/MKS)
- [USI-LS](https://github.com/BobPalmer/USI-LS)

If you would like to include special support for your (or your favorite) mod, let me know. Or, better yet, provide a PR.

Making History expansion is fully supported, but not required.

**Conflicts & Incompatibilities**

- Any mod, which can temporarily make kerbals Tourists, can conflict with Kerbal Health if both mods change kerbals' status and then turn it back. In some situations it may mean that your kerbals will remain Tourists indefinitely or become active too soon. Kerbal Health tries to fix some of these situations, but cannot prevent all of them.
- It is recommended to disable habitation mechanics of USI-LS' (and other mods') as these largely have the same goal as Kerbal Health.
- RemoteTech's connection state is not supported for the purpose of the Connected Factor status. This issue will be resolved once RemoteTech 2.0 is released. Meanwhile, you may disable both Connected and Assigned factors to keep balance.
- Compatibility with Kerbalism hasn't been tested. This mod changes much of game's internal mechanics, so it can be incompatible.

**Future features**

- New mechanics: more various diseases, radioactive planets, injuries, medical supplies, quarantine, and whatnot...
- Solar weather and/or radiation events
- UI improvement
- API for collaboration with other mods

**Copyright and License**

This mod has been created by [Garwel](https://forum.kerbalspaceprogram.com/index.php?/profile/141813-garwel/) and is distributed under MIT license.
