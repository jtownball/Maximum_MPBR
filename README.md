# Maximum_MPBR

Source for ballistics calculator
https://www.jbmballistics.com/ballistics/calculators/calculators.shtml

So the Army wants to train and equip soldiers to be effective in combat. Through years of experience they've come up with some very good approaches small arms combat.
In particular, how they setup the M4 rifleman rifle.
The M4 is is fairly close to the AR platform that is generally hated as a weapon of war that "doesn't belong on our streets" or whatever (not here for the gun debate).
It fires a 5.56mm cartridge from a 14.5 inch barrel that's gas operated using NATO m855 ball ammo (they might have changed it recently).
The key here is that for that ammo and that barrel the bullet has a specific ballistic coefficient and velocity such that it is effective out to about 600m.
The more interesting aspect is there way the rifle is setup.
The soldier first zeros the rifle at 25 meters with the optic.

Once the zero is established, the soldier goes to the range where they will engage popup targets at ranges from 25 meters to 300 meters.
That point of aim at 25 meters and 300 meters is dead on. At ~150 meters, you bullet is near the top of the parabolic arch (this is just an approximation) and so you need to aim about 5-6 inches high.
For a human sized target, you can effectively engage any target from 25 to 300 meters if you aim dead on center of mass.
The Army standard for the M4 is 4 moa (which is an extremely sloppy rifle) and even then if you're a good shot you can hit those targets.
There are (or were when writing this) 40 targets and 40 shots. In order to make all 40 shots you have to shoot from prone, kneeling, and the new system includes a barricade. You will also have to do a magazine change while engaging targets.
I have, over the years, hit 40 out of 40 multiple times and im not the best shot.
It does take some luck at the cheap army magazines are apt to jamming the rifle.

Having said all of that, the key take away is that the system is designed and built around making it as easy as possible for a soldier to train and use the M4 weapon system. There's no ballistics calculations, there's minimal adjustments needed to be able to use that system.
That brings me to the point here, and that is setting an effective hunting rifle and the strategy behind it.
Maximum Point Blank Range (MPBR), for the M4 is 300 meters.
The entire system is built to be able to use effectively from 25 to 300 meters without having to think about it.
When hunting game, you can't predict when you'll see a deer (or whatever you're hunting).
It might be on the way to your spot, or the way back to your truck or at anytime.
If you are setup to only make shots from a tree stand with a range finder and a ballistic reticle, you're missing a lot of hunting opportunities.
So my plan is to setup my hunting rifles with a MPBR that matches the game and my realistic expectations about hunting.

For example, my 45/70 shoots big 325 grain bowling balls at 1886 fps and so it's unrealistic to expect that rifle to shoot much past 150 yards.
My 300 win mag, shoots 189 grain, high BC (ballistic coefficient) bullets at 3000 fps so my MPBR is probably closer to 300 yards (or more).
But the process for setting the rifle in this isn't super efficient.
You pick a cartridge, shoot it for your gun to get the muzzle velocity.
Take that bullets BC and that muzzle velocity and the scopes height above bore and the zero and then the calculator will spit out a range chart.
Pick a different zero and you have to re-run the calculator.
This is horribly inefficient.
So, I found an open source library for a ballistic calculator.
With that I can easily make a whole series of calculations that iterate over different zeros so i can easily pinpoint the zero needed for my maximum MPBR.

So I am going to take that open source library, write it in either R or Python and then make a webpage that lets anyone quickly find the maximum MPBR for their rifle and ammo combination.
Then you just buy a scope with just cross hairs, aim center mass out to you MPBR and fire. No holding over the target and making kentucky windage guesses.
So that's my project.
Hunting season is in December, and I need this done by mid-october for it to be useful before this year's hunting season kicks off. 
I need it done by then to give me time to verify it, and get ground truth data.
A potential next year enhancement would be to make tables that let's the user modify the bullets and velocity separately from factory cartridges. 

So, for example, I can throw in different .30 caliber bullets and powder loads (which changes velocity) and quickly see what gives me a maximum MPBR for my rifle barrel length.
(the dwell time is how long the bullet is in the barrel being accelerated by the gas pressure. A longer barrel will give you a longer dwell time, and faster burning powders will increase pressure and more powder, etc...)
