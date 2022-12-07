# mn_missilemania_idv2
Bugtracking for indev2 release of Monday Night Missilemania
# imported prerelease testing readme below
#

----------
MONDAY NIGHT MISSILEMANIA
 ©2022 DanDoesAThing (Daniel Newby)
[Indev Version 2]
___________________________________

README for indev2 private pre-release testing

This game was built in the open-source Godot Game Engine (v3.2.2.stable.official).

----------

Warning: this readme is pasted from a GDoc pasted from a notepad file,
the formatting may be all kinds of messed up

[README contents]

 i.	Thanks for Testing
 ii.	How To Report Bugs
 iii.	Known Bugs
 iv.	How To Play
 v.	Development
 v.	Suggestions
 vi.	Thanks for Reading

----------

Thanks For Testing!
----------

---
INTRO
--- 
                                                
Thanks for testing, and thanks for actually opening this README!
It is so easy to ignore these, but this is where I'll be writing notes on different release builds,
so between builds it'll be worth checking at least the 'known bugs' section to see if anything changes.

If you're not interested in reading the whole thing,
then the most important sections to read are:

	*) section i // thanks for testing (this section)
	*) section ii // how to report bugs
	*) section vi // known bugs

The private testing period for Indev2 will run from 6th December 2022, until the 19th December 2022.
Indev2 should release on the 20th December 2022 (soft release date).

Throughout the testing period there will be additional builds released. Don't feel obligated to
test every build. Any time you can spare, and any feedback you can give, is appreciated.

---
PERSONAL NOTES
---

Although it is the second release, Indev2 is the first 'MVP' release (Minimum Viable Product).
What I deemed 'Indev1' was a prototype thrown together relatively quickly, with little iteration.
Indev2 was a ground-up rebuild of that initial prototype.
I know the game is not terribly impressive right now. It is very lacking in actual content.
Indev2 has been a lot of framework/backend to support future content development.

(Please don't let first impressions influence your opinion of how much effort has gone into it,
For all the time I've put into it, I'm still just one person trying to do the jobs of many.)

Feedback, even criticism, is appreciated and welcomed. There's a lot more work to do.

---
THIS TESTING PERIOD
--- 

The main two goals of this two-week testing period are:

	1) determine performance on different specification PCs
	2) find any game-breaking bugs or crashes that aren't present on my desktop/laptop

Opinions on the game, criticism of the game, and suggestions on the game (see the section below), are
welcome. Feedback is really important and I've definitely not gotten enough outside feedback at this point.

Going forward into indev3 I'll be aiming to export frequent release builds with minor changes, rather
than waiting until the end of the development cycle. If you're interested in testing on an on-going basis
let me know and I'll invite you to the discord. Don't feel obligated to though, this is an unpaid volunteer
gig and you're all busy people!

---
YOUR COMPUTER SPECIFICATIONS
--- 

As a tester it is important for me to know how the game runs on your machine.

Towards the end of the testing period it is likely I'll follow-up on what
performance was like, and ask for your computer specs then, but if you
want to report this earlier that'd be a great help.

If you don't know how to get your relevant computer specifications, please follow these steps:
[These steps apply to Windows Operating Systems only]

1) Click in the task bar search bar (where it reads 'type here to search')
2) Type 'dxdiag'
3) Open the suggested program 'DirectX Diagnostic Tool'
4) On the default tab 'System', either take a screenshot of the system information or write it down.
 4b) The relevant information to grab is
	i) operating system
	ii) processor
	iii) memory
5) Navigate to the second tab on dxdiag, labelled 'Display 1'
 5b) As in step #4, record the system information by screenshot or writing it down
 5c) The relevant information to grab is
	i) Name

As an example of what I'm looking for:

Operating System:	Windows 10 Home 64-Bit
Processor:		Intel(R) Core(TM) i5-9600k CPU @ 3.70GHz (6 CPUs)
Memory:			16384MB RAM
Display 1 Name:		NVIDIA GeForce GTX 1060 3GB


----------

How to Report Bugs
_________________________________________ 

---
BUGS
---

It is inevitable at some point you'll encounter a bug.
This is a considerably early build still.

 To quote the preloader-splash text ingame:
	"There may be bugs, unbalanced gameplay elements, and placeholders.
	Content is likely to change markedly between versions,
	and the current state of the game does not reflect the intended end project.
	Thank you for understanding."

---
GETTING THE LOG FILE
---

The best way to report bugs, is to provide the log.txt file to me.

On Windows you can find the 'log.txt' file by following these steps:

 1) Open a folder/windows explorer,
 2) right click in the address bar,
 3) click 'edit address'
 4) copy and paste the following line into the address bar, then press enter:
%AppData%\mn_missilemania\logs

If you are on macOS, you will find the log folder at: ~/Library/Application Support/mn_missilemania/logs
If you are on Linux, you will find the log folder at: ~/.local/share/mn_missilemania/logs

---
ADDITIONAL INFORMATION

It helps when you're reporting bugs if you can comprehensively report the circumstances in which the bug occured.

Try answering these questions:

	1) How would I reproduce the bug to test it?
	2) What were you doing in-game when the bug occured?
	3) What were you expecting to happen instead of the bug?

---
IMPORTANT NOTES
---
 1) you will not be able to find the user data/log folder if you haven't at least run and loaded the game once
 2) if you run the game before getting the log file, the log file will instead be relevant to the most recent run*

* up to 5 additional log files are stored in the mn_misslemania logs folder,
	so if it is a recent game instance that featured the bug,
	you can still get the relevant log file
                                                   

----------

KNOWN BUGS
----------                                                    

These have been moved to the issues section of the repository.

----------

How To Play
---------- 

---
GAMEPLAY DESCRIPTION
---

Monday Night Misslemania is a top-down arena survival or 'bullet heaven' game.

You control a drone spaceship (no pilots, don't feel guilty about inevitably getting blown up)
against the backdrop of space, whilst missiles attempt to chase you down and destroy you.

Your ship is equipped with a series of weapons that will automatically target enemies and
fire at them. You do not have to worry about manually targeting enemies, just dodging them!
Your weapons however do have independent ammo counts and reload times, so sometimes you
may have to rely on different weapons whilst another isn't active.

The game as of indev2 has no end goal. You just play until you die.

---
GAMEPLAY NOTES
---

Movement is remembered! You're in space.
If you go forward, and then stop going forward, you will keep going forward.
For gameplay reasons this *is* capped. Early tests showed the game was absolutely uncontrollable the
closer to realistic movement it got, so a balance between space physics and 'actually playable' was needed.
You need to cancel out previous movement before you can go in the other direction.
Try and account for this when dodging enemies.

When you activate the main engine your rotational thrusters are capped.
Effectively, if you press the 'go forward' action, you will turn slower.
Let go off 'forward' before you try and turn. You'll keep going forward anyway.

In Indev2 the available weapons for your ship are:
 - The Light Machine Gun or Personal Defence Cannon 'PDC'
 - The Medium Broadside Burster
 - The Heavy High-Velocity Railgun

Each behaves in a diferent way.

 -	The LMG/PDC has a high ammo count, fires quickly, and reloads slowly.
	It tracks enemies, rotating to face them as it fires, but has a limited rotation arc of 90 degrees.
	Heavily inspired by the Rocinante's cannons on the Expanse.
	Your ship can support up to 10 of this weapon, 4 on each side and 2 on the nose of the ship.

 -	The Broadside Burster fires a spread of higher damage projectiles.
	Bursters fire in an alternating pattern. The bursters on one side of your ship fire,
	then the bursters on the other side of your ship fire. This then repeats.
	They're pirate ship cannons.
	Your ship can support up to 6 of this weapon, with 3 on each side.

 -	The High-Velocity Railgun fires a single projectile.
	This projectile pierces all enemies, and always destroys any enemy it touches.
	The railgun itself has a maximum ammo count of 1, and is slow to reload.
	Your ship can support only 1 of this weapon, mounted on the top of the ship.
	

---
GAMEPLAY LOOP
---

Missiles will spawn and attempt to chase you down. Your weapons will attempt to fire at the missiles,
or fire in a direct line based on where they are facing (some weapons track enemies, some do not).

When all missiles are defeated the 'perk option selection' screen will pop up.
On this screen you can choose a perk (a boon/benefit) that will affect your gaemplay.
Each perk is also attached to a set of enemies; these are the enemies that will spawn next!
Sometimes it may be worth skipping a desirable perk if it has a scary set of enemies attached.

NOTE:	As of indev2 perks are not yet functioning.
	Some temporary perks might make it into indev2, but they're unfinished.

After you select a perk, the gameplay begins again.

---
CONTROL SCHEME
---

These are the default controls.
The game has basic joypad support but input remapping had to be disabled for this build.

[Keyboard]	[PS Joypad & Xbox Joypad]		[Action]
W Key		X Button or A Button		Active main engine/add forward thrust
A Key		Left Joystick, Left Axis		Rotate the ship left
D Key		Left Joystick, Right Axis		Rotate the ship right
F1		{currently unsupported}		Show/Hide Debugger Info
ESC		{currently unsupported}		Pause Game

----------

Development
----------                                                         


---
DEVELOPMENT HISTORY
---
I first started working on MNMM in February 2022 (though back then it was called 'Missile Survivors').
The initial pitch was 'the scenes from 'the Expanse' where the Rocinante blows up missiles' meets 'Vampire Survivors'.

By May 2022 I'd put together a very simple prototype (which I now refer to as 'indev 1').
It's actually probably more accurate to say I spent a couple of weeks building a game prototype,
and then 3 months building the framework around the game to actually be able to release it publicly.
I spent those first few months of development working one evening a week, maybe a weekend day or two.

You can still find this prototype on my itch.io page, if you're interested in comparing
indev1 and indev2. Find it at: https://dandoesathing.itch.io/star-survivors

After I released the prototype on reddit, in the Godot community subbreddit, where it got a surprisingly positive
reception (it's a very encouraging community), I gained enough confidence in the concept to keep at it.

I rebranded the game to 'Star Survivors' and spent the next 2 month working slowly at it, frequently distracted
by life. Then the thing I'd been fearing since I first went 'I can't believe none of these other
sci-fi vampire-survivor-likes are using this name' happened;
someone beat me to market with a similar named game in an almost identical genre.

So July 2022 I had to drop everything Star Survivors related, and stopped working for a week whilst I collected my
thoughts. This is actually where development begins in earnest. Up until this point I'd been working on other projects,
job hunting, and treating game development more like a dedicated hobby. As of July 2022 I've considered this my
job, and have been working on this game every day (now roughly 6 months without missing a day).

After the name debacle, more than my attitude to development shifted. My goals for the game did.
I decided that just being a Vampire Survivors clone wasn't enough; I'd noticed a growing trend that
the gaming community was sick of the deluge of vampire-survivor-likes, and it was something that had been concerning
me for a few weeks at this point anyway.

So I went back to the drawing board and pulled out one of the weirder ideas that I'd ignored early on.

---
FUTURE DEVELOPMENT OVERVIEW
---

As the 'Monday Night Football' spoofing title suggests, Monday Night Misslemania is going to be a sports* game.

*Sort of

The plot of the game will be in a near-future scifi in which the most popular worldwide sport is 'Missile Dodging',
a sport in which solo drone operators remotely pilot actual (albeit disposable) military spaceships and
attempt to avoid missiles that their 'viewers' are attempting to hit them with. Sort of a 'TwitchChatPlaysTagInSpace' thing.

The main game/story gameplay loop will be akin to Fifa/other football games, with the player cast as a drone pilot who
has just been promoted up to the major leagues. Aside from managing their rank in the Misslemania leagues, the player
will have to garner fans, manage relationships with the sponsors who provide the in-game perks and parts for their ship,
and tinker with/build drones to fly for matches.

If you can't picture that, but you're intrigued, let me know. I've got some draft ui designed I can show off.

---
DEVELOPMENT GOALS AND NEXT RELEASE VERSION (INDEV 3)
---

Indev3 (the next release version) is going to be targeting some of these goals, particularly moddability since I've
already got a great April 1st demonstration of the modding feature planned. Indev3's primary goals (aside from refactoring
the ship resource framework to support moddability) will be to nail down the game loop and add more content to
expand on the current perk/spawn/tag system that I built for Indev2. After that it'll be time to move off Indev and into Alpha.

Alpha 1 will follow Indev3, and that will be the beginning of the early access period on Steam.
Early Access will be where I start selling the game (albeit at a significant discount) but rest assured,
if you're a tester at any stage the game will remain free for you forever.
If I don't remember to send you a full copy when it goes on sale just message me and I'll sort that out for you.

I'm tentativelyTentatively aiming for late Summer/early Autumn of 2023, but it's way too early to set a release date for that. I'd
like to hit the 

As to the future development goals for the game; ultimately I am looking for this game to be an tactically-leaning bullet heaven,
where (due to the conserved momentum and detailed flight plans) you must make decisions ahead of time to succeed.
Since my favourite games involve customisation at their core, I'll be aiming for a high potential of in-game build complexity,
and enabling player experimentation/building wherever possible.

--
Here's some of the specific design goals I've got:
--

# WEIGHTED ENEMY AND PERK SPAWNING
 Every perk you choose has 'tags' associated with it.
 Every enemy has 'tags' associated with it as well.
 As you choose perks, you build up tags in your game.
 The enemies you'll see spawn each game wave, will be influenced by these tags.
 The perks you get offered each game wave, will be influenced by these tags.
 Do you want to fight fewer high-explosive enemies? Stop picking the high-explosive tagged perks!
 Do you want to pick laser-affecting perks? The more laser perks you pick, the more you'll see.
 The best bit is this system is actually already present in the game! Sort of.
 It's there, but there are just not enough content to properly demonstrate it,
 so it'll be Indev3 before you can see it in it's full glory.

# UNIQUE ENEMY BEHAVIOURS
 I've already drawn and prototyped 13 enemy types. Many that were initially planned
 as part of Indev2 got delayed by a pending shader rewrite and enemy controller refactor.
 As the game develops I'll be looking to split enemies into archetypes that can be
 mixed and matched to provide a great deal of procedural content at a fraction of the dev-effort.

# UNIQUE WEAPONS
 Mini-drones that follow your ship and turn the game into Snake.
 Lasers that lower the maximum HP of enemies rapidly (until they lose focus), setting up kills by other weapons.
 Anti-missiles missiles! Yo dawg I heard you wanted missile mania so I put missiles in your missiles!
 And so much more. If you're interested in hearing about content plans, shoot me a message. There are docs I can share.

# SHIP CUSTOMISATION
 Players can build their own drones from unlocked ship parts (see below).
 The parts you choose influence the perks available you in gameplay.
 In this way players can determine their own gameplay experiences.

# METAPROGRESSION
 Players unlock ship parts and potential in-game perks through sponsorships from ingame NPCs.
 Some ingame NPCs dislike each other, so you have to balance which teams you play for and
 what offers you take during gameplay.

# MODDABILITY
 The feature I'm potentially most excited about, and something I'm already working on (best to get the
 groundwork laid early); I want the content/resources in the game to be entirely moddable by players.
 Perks, Weapons, Ship Pieces, Engines, Enemies, Projectiles <- all of this will be easily moddable.


----------

Suggestions
----------                                                      


Indev 2 (MNMM release version 0.2, the upcoming game release) is feature locked.
What this means is any suggestions you've got, no matter how cool or fitting I think they are,
will definitely not be part of the game in this upcoming release. There's not enough time left to
implement and test anything else before December 20th (current target release for Indev 2).

Not to mention the game is still in an early state and I've got large refactors/revisions planned already.
I know there's a lot that could be done, a lot that is missing; trust me, I spend 90% of my day thinking
about what I could change or add to make it better. Adding stuff is the most fun part!

Despite how that sounds I'm actually really eager to hear what you think the game needs.
This is the best time to make suggestions as it's still so early in development I can easily pivot to make
larger (within reason/scope) changes. I just want to be up-front that I won't even begin to look at
implementing anything new until the next development cycle begins in January.


----------

Thank you for reading!
----------       
                                                

If you made it this far, I'm impressed!

Please let me know what you think of the game. Monday Night Missilemania has a lot
more development to come, and feedback from testers is going to be key for that.

----------       

MONDAY NIGHT MISSILEMANIA
©2022 DanDoesAThing (Daniel Newby)


