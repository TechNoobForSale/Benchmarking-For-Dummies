# THE EXYNOS 9810 UNDERVOLT GUIDE by Nightshot V1

**ONLY FOR PEOPLE RUNNING THE LATEST VERSION OF XXTR KERNEL BY https://github.com/xxmustafacooTR**

**This is a Github Port of the Original Guide, which was written on a PDF File**

## DISCLAIMER:
**YOU ARE ABOUT TO MESS WITH SYSTEM PARAMETERS. ME AND THE XXTR TEAM, AS WELL AS ANYBODY ELSE WHO BRINGS THIS DOCUMENT TO YOUR ATTENTION ARE NOT LIABLE FOR ANY DAMAGE THAT OCCURS TO YOUR DEVICE DUE TO IMPROPER SETTINGS OR ANY OTHER REASON AT ALL.**

So anyway, **let’s begin.**

**Tired of suffering the pains of Samsung Manufacturing? Well, other than Underclocking, we got another trick up our sleeve. That’s Undervolting.**

**Undervolting is the process of lowering your Processor’s Operating Voltage to reduce heat production and power consumption while giving up nothing at all.**

## PREPARATION STEPS (And FUCKING FOLLOW THESE):

Step 1: Obtain the latest version of xxTR Kernel. (At the time of writing, It’s xxTR Kernel V46 Beta 4). It can be downloaded from the pinned message in the xxTR Telegram Group. If you’re somehow not in the group, GET IN IT.

Step 2: Obtain the xxTR Kernel Manager App. It also can be downloaded by the pinned message in the xxTR Telegram Group. If you try any other Kernel Manager to tune xxTR Kernel, I won’t support you in any way.

Step 3: Have COMMON SENSE. For example, bigger number =/ Better.

Step 4: Have at least some very basic knowledge of how Frequencies on Processors work. Otherwise get out of here.

Step 5: On the xxTR Kernel Manager, go in “DEVICE” and verify your ASV Table. The minimum number for each component is 0 and the maximum is 15. The higher it is, the more of a lucky bastard you are. Higher in this case means better ability to undervolt.

Let’s move on. And I am not responsible for any bullshittery you do with your device. If you follow the guide properly, you won’t have anything unexpected occur to you.

## UNDERVOLTING STRATEGIES

Not everyone has a lot of time on their hands, but it’s also true that many people have never touched grass in their entire life. But we also have people in the middle, so rejoice! We have strategies to accommodate every one of you. Let’s begin, shall we?

## 1: The Global Adjustment Strategy (I won’t talk to people who use this one)

It does exactly what you (probably) think it does. **Globally** adjusts the Voltage for every frequency your CPU can use, so you don’t need to think about anything other than quite literally moving one slider.

**Note: Global Adjustment is MANDATORY for people who look to undervolt MIF and CP too.**

**1:** Open xxTR Kernel Manager

**2:** Swipe from the left corner of the screen to the right (Some people actually don’t know this)

**3:** Locate: GPU, POWER, then scroll down and locate CPU big Voltage and CPU LITTLE Voltage.

**4:** Go in POWER and locate MIF and CP. CP is your MODEM. It makes Mobile Data and Wi Fi possible on your phone. This chip runs quite fucking hot. So, we undervolt it. Start by gradually reducing the voltage by –2. The most I recommend if you don’t care too much is –5. Same goes for MIF.

**4a: SIGNS OF INSTABILITY:**

MIF: Your phone will freeze, the screen will display anomalous colors, etc. MIF crashes are very brutal, and they will scare you. They are especially dangerous when they happen while you are producing data, since it can get corrupted. That is rare, however, don’t chicken out just yet. A force reboot is all it takes to reanimate your phone.

CP: No Data and/or no Wi Fi are a sign of CP instability. Just dial back the undervolt.

**5:** Go in GPU and locate a switch that allows you to either go in Global Mode or Individual Mode. Switch it so it goes in GLOBAL MODE. Afterwards, start dialing back the voltage slider by –25mV steps. After you cross –50mV total, dial back by –10mV steps. If you can’t be bothered in fine tuning it, just slam –50mV and pray it’s stable. 

5a: SIGNS OF INSTABILITY + HOW TO VERIFY

A strongly unstable GPU will freeze the screen (But system will still appear to be running as it should. For example, you will be able to still hear notifications or even tap on apps, but the screen will just be frozen to the last frame the GPU processed). A mild instability will manifest in the form of stutters, momentary freezes in the UI. If you’re running games, they will freeze, stutter heavily, or even show visual artifacts (flashing points on the screen, corrupted textures, etc.).

### To verify the stability of your Undervolt, you either play games or use benchmarks. I recommend benchmarks. Obtain 3DMark and once you open the app, download Slingshot Extreme and Wildlife. Run both, for one verifies OpenGL ES 3.1 and the other tests Vulkan. They are different APis and behave differently. One may be unstable when the other isn’t.

**6:** This goes for both CPU big Voltage and CPU LITTLE voltage. Once you have located the Global Voltage Control Switch for both, start dialing back by –25mV steps ONE AT A TIME. (If you do both, you won’t be able to tell which one is getting unstable, wasting your time). CPU has a ton of frequency steps, so only use Global Adjustment for it if you REALLY can’t spend some time fine tuning it. You won’t get much out of it.

**6a: SIGNS OF INSTABILITY + HOW TO VERIFY**

When CPU BIG is unstable, apps start crashing and you are unable to boot them back up. It may eventually freeze your phone. If the instability is very pronounced, your phone will shut down altogether. 

When CPU LITTLE is unstable, the phone usually just shuts down. Little Cores are CLUSTER 0, which means they are responsible for the system’s very base stability. If Core 0 (which is a little core) miscalculates, your system will crash.

To verify the stability of the CPU, obtain Geekbench 5, which offers a good compromise between intensity of the workload and time saving. Geekbench 4 is better if you don’t have much time on your hands, and Geekbench 6 is for dumbasses. Keep in mind that the first 50% portion of Geekbench is SINGLE THREADED. This means that your Exynos 9810 will rely on BOOST frequencies, which are known to undervolt LESS, and they can and WILL limit your undervolt if you use Global. So, if your phone crashes during the Single Threaded test, your problem is LIKELY the Turbo Frequencies. If it crashes during the multi-threaded test, well your CPU can’t handle that uV.

**Little Tip for NOOBS:** To avoid the aforementioned Single Threaded limit situation (And to potentially increase your undervolt), locate CPU HOTPLUG and shutdown both switches. This will disable the Turbo Frequencies, making your CPU solely rely on its base speed in peak operating states.

Congrats! You made it to the end of the Global Voltage Strategy. Now let’s move onto the Second Approach, which is the SMARTEST.

## 2: THE SMART SCALING STRATEGY (Normal/Smart People use this one)

If you’re here, I assume you’re fairly smart and that you already have a certain degree of knowledge of the arguments treated in the GLOBAL VOLTAGE STRATEGY GUIDE (Which will be FUNDAMENTAL here). If you’re not, it sucks to be you, you shouldn’t be here and I will not repeat them again, so go read the Global Voltage Strategy steps to learn something.

**This one requires an increased amount of brain power, for you will need to wield a certain skill, which is called “APPROXIMATION”**. The better your skill in that regard, the more time you can save. Essentially, this Strategy relies on finding one or more “Baseline Frequencies” and testing them, in order to obtain the maximum possible undervolt specifically for them. Then, according to the undervolt obtained, you will scale the voltage required for the neighboring frequencies.
Baseline Frequencies for CPU BIG:

2704MHz (ONLY INCLUDE THIS IF YOU PLAN ON USING HOTPLUGGING. Useful to approximate the voltage for the frequencies that go from 2496MHz to 2652MHz. 2860MHz and 2886MHz states are extremely inefficient and will barely undervolt if at all.)

1794MHz (This is the Holy Grail of this CPU. It’s the Stock Base Frequency. It will be useful to approximate the voltage for the frequencies that go from 1261MHz to 2314MHz.)

858MHz (This is one of the lowest frequencies for Big. It will be useful to approximate the voltage for the frequencies that go from the min 598MHz to 1170Mhz.)

Baseline Frequencies for CPU LITTLE:

2002MHz: Useful to approximate down to 1950MHz.

1794MHz: Stock. Useful to approximate down to 1053MHz.

715MHz. Useful to approximate down to 208MHz and up to 949MHz.

**Note: GPU generally only needs 598MHz and 338MHz as baseline frequencies. It doesn’t have a lot of steps.**

**1:** After understanding these Baseline Frequencies, make sure you have Geekbench 5 and 3DMark (Slingshot Extreme and Wildlife) ready, in order to test. 

**2:** DISABLE HOTPLUG and ENABLE INDIVIDUAL VOLTAGE CONTROL IN GPU, CPU BIG VOLTAGE AND CPU LITTLE VOLTAGE.

**3:** Lock CPU BIG to 1794MHz Min AND Max. Apply your desired undervolt, possibly in –25mV steps at first and then –10mV after you reach over –50mV total.

**4:** Run Geekbench 5 until 1794MHz becomes unstable. Note down the maximum undervolt number it was stable at. 

**5:** Using the maximum undervolt 1794MHz was stable at (For example, let’s say –68mV like for me), start applying a similar undervolt to all the frequencies between 1261 and 2314MHz. The closer you get to the bottom or the upper limit of this frequencies range, the more conservative you’ll have to be. For example, 1794MHz and 1690MHz are very near to each other. If 1794MHz was stable up to –68mV, chances are 1690MHz will be stable at –68mV too, and maybe even a little more (you can tweak this, but then your Strategy would remind more of the Individual Voltage Adjustment). So, proceed further down the frequencies and keep applying an undervolt similar to 1794MHz, using your common sense. By the time you reach 1469MHz, you’ll probably have to dial back, for example to –62mV or even –55mV, to keep everything stable. (The lower the frequency becomes, the less it can undervolt. The frequencies in the middle however (1469 to 2106MHz) are the ones who usually undervolt the best).

**Note: The above procedure is basically the principle of the Smart Scaling Strategy.**

In a Nutshell, the lower the frequency gets, the less it will undervolt, and the higher the frequency gets, the less it will undervolt. The key here is to keep in mind the relation between each frequency’s voltage. It’s like a line that you must go along with.

**6:** Repeat Step 4 and then Step 5 with the rest of the baseline frequencies for Big, as well as those of GPU and CPU LITTLE. Keep in mind that for GPU you MUST use 3DMark. Don’t even think about using GEEKBENCH COMPUTE. I’ll beat the shit out of you.

**EXTRA 7:** To test Hotplug Frequencies, Re-Enable Hotplug and find the minimum stable voltage for 2704MHz, through the FIRST HALF of Geekbench. Once you find the maximum Undervolt Value for it, approximate for all the nearby frequencies. Hotplug must be off while testing 1794MHz (and similar frequencies) because it can interfere with the testing of 1794MHz and the other Baselines.

Note: Remember that to test 2704MHz as Single Core Boost you must have Hotplug enabled, then head to CPU Big max frequency, and set 2704MHz. You will see the number reverting to a lower value, but that’s normal and your input has been received.

## 3: The Individual Voltage Tuning Strategy (You need to go outside)

**Oh, so you got time to waste huh?** Well, that’s pretty good I suppose. If you’re here, you probably know what you’re getting yourself into. If you don’t, go read the previous sections of this guide, so you can learn how to do what you want to do.

**Individual Voltage Tuning isn’t inherently harder or dangerous and it’s rather easy to explain. It’s just really, really time consuming. But who cares! You even forgot what color the grass outside is, so let’s proceed.**

**1:** Locate GPU, POWER, CPU big Voltage and CPU LITTLE voltage

**2:** For Power, Locate CP and MIF and start testing granularly each – step. 

**3:** For GPU and CPU, enable individual Voltage Tuning and go ham. Remember –25mV steps for the first 50mV and then proceed at –10mV steps (Or if you’re in a hurry, for some reason, -15mV).

**4:** Test each and every Frequency with the appropriate benchmark for the component you’re targeting. You should definitely lock either CPU or GPU at the frequency you’re testing, otherwise you’ll never be able to tell if your settings are stable at each step.

## 4: Desktop Strategy (I use this one)

**Can’t be bothered with battery life or fine tuning every frequency known to man? Well, you’re in the right place. You may know that Desktop PCs generally run at one fixed frequency, be it the CPU or the GPU. This is just that.**

**1:** Lock Big CPU’s min frequency so that it’s the same as max base frequency (NOT MAX BOOST FREQUENCY). Do the same for CPU Little

**2:** GPU Governor must be “always_on”. GPU is harder to control unless you’re in Game Mode, so just leave its minimum frequency untouched.

**3:** Undervolt the static CPU frequency (Or its turbo frequencies too if you have hotplug enabled) and find the minimum stable point through Geekbench 5. 

**4:** Repeat step 3 for GPU, except that obviously, you use 3DMark to test the stability. 

### Note: Individual Voltage control is preferred in this case. You don’t need to touch frequencies you’re not going to use anyway. 

*That’s it. I hope you will come out of this Document a little bit less dumb than you were previously. Now go on and do whatever. Every phone is different. Don’t fucking ask how to undervolt on the group again. (Unless you want to request Rule-of-thumb undervolt to save the highest amount of time. But we won’t be liable for your potentially crashed device).*

- **This File's Revision is final. Probably. Lmk if it's got issues, or if you got questions.** -
- **2024 Update: Watch out for Power Throttling during testing, as it may affect the reliability of your measurements. Power throttling occurs when the CPU or GPU requests a lot of current, and the PMIC drops the supplied voltage due to the high load. This issue will be particularly prominent if you have already applied a significant undervolt, since the CPU will no longer have much extra voltage to rely on in case of Vdrop. This will cause the CPU to reduce performance according to how bad the lack of voltage is, without crashing, unless the voltage falls too low. To detect this problem, control if the CPU temperatures are too good to be true, or if the power draw is below 5W under "full load". The 1794MHz frequency state should normally draw between 8 and 10W in serious benchmarks. No, CPU Throttling Test is not a serious benchmark.**
