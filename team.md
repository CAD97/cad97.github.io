---
title: "Team Game Projects"
description: null
---

## Conjury Revell

<video controls muted width="100%" poster="{{ '/assets/img/conjuryrevell.png' | relative_url }}">
    <source src="{{ '/assets/vid/conjuryrevell.webm' | relative_url }}" type="video/webm">
</video>

<iframe src="https://store.steampowered.com/widget/2142850/" frameborder="0" width="646" height="190"></iframe>

This game was developed by a 27-person student team from SMU Guildhall over the course
of six months, as part of the program's capstone Team Game Project (TGP) curriculum.
The soundtrack was composed by a team from SMU Meadows School of the Arts.

During the development of *Conjury Revell*, I was in charge of the build process,
including automated daily upload of development builds to Steam, as well as several
core systems of the game, including the save persistence system as well as all of
the menu and 2D HUD elements' implementation. Taking on these duties freed up the
rest of the programming team to focus on iterating the other areas of development.

The devlopment of this game was a bit troubled, taking a bit longer than originally
hoped to find its identity and undergoing some large cuts of content due to that.
Navigating this was an insightful experience, as a meaningful portion of effort was
invested into systems and content which never got to see the light of day because
it was more important to invest in improving what was working and make a smaller
well-put-together game than to continue developing the underutilized systems.

If I were to pick one thing to point at and say "I made that," it would be a close
race between the animated indicator when the game is saving, and when the game is
loading between scenes. Both had interesting implementation constraints due to the
asynchrony required to get a good user experience instead of just freezing the game
while IO is done, and both were an instance where I got to put a little bit of extra
polish into the game via a bit of animation nuance not in the initial draft.

## Kibbi Keeper

<video controls muted width="100%" poster="{{ '/assets/img/kibbikeeper.png' | relative_url }}">
    <source src="{{ '/assets/vid/kibbikeeper.webm' | relative_url }}" type="video/webm">
</video>

<iframe src="https://store.steampowered.com/widget/1702970/" frameborder="0" width="646" height="190"></iframe>

This game was developed by a 15-person student team from SMU Guildhall over the course
of six months, as part of the program's capstone Team Game Project (TGP) curriculum.
The soundtrack was composed by a team from SMU Meadows School of the Arts.

During the development of *Kibbi Keeper*, I was primarily focused on maintaining the
performance of the game, especially with respect to the VR playground expansion, as
well as handling the menus and save persistence system. Early on in development, I
approached Kam, our Game Design lead, with a concept for the main title screen and
menus. With his greenlight, I blocked out the environment and camera movement on the
title screen, and that initial vision shipped in the final game nearly unchanged.

One fun issue we ran into during development and I ended up having to debug was a
crash that occurred only in shipping builds of the game, and as such provided very
little insight as to what caused the crash. After going through the process of making
a version of the game with a debuging compilation of the engine itself, I was able
to track it down to that in the version of Unreal Engine we were using, setting a
Niagara particle system to `None` in Blueprint was improperly only checked for being
`nullptr` on the C++ side in editor builds, and in shipping builds just chucked the
null pointer where it didn't belong, leading to the crash. We worked around it on
the Blueprint side by setting a do-nothing system instead (what the C++ was supposed
to be doing), and everything worked again.

If I were to pick one thing to point at and say "I made that," it would have to be
the musical egg. It's a small and easily overlooked detail in the game, but thanks
to my pushing for and implementing, the music box notes that the egg plays actually
match the chord changes of the playing background music. It's these small details of
coherency in design and execution which always make me smile when possible to pull off.

## Snowpainters

<video controls muted width="100%" poster="{{ '/assets/img/snowpainters.png' | relative_url }}">
    <source src="{{ '/assets/vid/snowpainters.webm' | relative_url }}" type="video/webm">
</video>

<iframe src="https://store.steampowered.com/widget/1545710/" frameborder="0" width="646" height="190"></iframe>

This game was developed by a 40-person student team from SMU Guildhall over the course
of three months, as part of the program's capstone Team Game Project (TGP) curriculum.

During the development of *Snowpainters*, my primary responsibility was to maintain
and extend the 3rd party tool we used for laying out track, called Modular Road Tool.
In addition to that, I was in charge of build automation including uploading daily
development builds to Steam, and assisted with the camera behavior and tracking
performance. Towards the end of development, I was able to develop some small bits of
telemetry for development builds to track the relative performance of each of the
classes of racing penguin, as well as if/where on the tracks that the CPU racres tended
to get hung up.

Working with the Modular Road Tool was certainly a learning experience. The initial
version of the tool worked well enough for simple use cases, but the entire development
process was the cycle of the level designers trying to do something vaguely interesting,
the tool breaking, and my needing to extend the tool to handle it. A good half of the
tool, if not more, ended up refactored and essentially rewritten to support the extra
things our team wanted to do with it that weren't anticipated by the original dev.

I certainly have capital-O Opinions on how to do a spline-based road tool, coming from
this project. I'm honestly unsure if they're all even achievable at the same time, and
I've not had the opportunity to take my shot at making the ideal spline road tool. But
the game managed to turn out well for all of the effort put into wrangling MRT both
from myself and from the designers using it, and that's all that matters in the end.
