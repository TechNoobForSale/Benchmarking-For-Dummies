# Benchmarking-For-Dummies Rev 0.8
A Repository containing knowledge about the trivial "art" of Benchmarking, specifically mobile devices.

### Has Benchmarking Mobile Phones ever crossed your mind?

Probably, it did. And that's pretty neat. But you see, Benchmarking Phones is way more tricky than it would normally be on a Desktop PC. You have to keep in mind many, MANY variables that OEMs usually lead you to believe to be completely irrelevant. But that's wrong. And in this guide I will show you why, and I will make you a better Benchmarker in the process. 

**Very well then, shall we begin? Allow me to introduce you to...

 ## The Official TECHNOOBFORSALE Mobile Benchmarking Guide.**

* Benchmarking is the Process through which the performance of a Device is evaluated through comparison with a baseline or a standard.
  Say that this Process evaluates devices with a score system, giving them one or more tasks to solve, using the baseline set by System A, which scored 1000 points. A certain System B runs the same 
  task and scores 500 points. This means that System B is half as fast as System A at performing that specific task. That means that you would rather own System A to perform said task, since it's 
  better at doing it.

  Now normally, for Desktop PCs (And to some extent, Laptops), running the task on your system is all you will ever need to do, to obtain an indicative result (Though some variables still do apply).

  **However for Mobile Devices, stuff is frustratingly harder.**
   Let me show you what I mean by giving you a list of the things you have to look for on these cursed phones.

  * Thermal Throttling
  * Background Processes
  * Kernel Performance 
  * Frequency Scaling **(Especially Important in Games)**
  * Power Throttling **(This will be Addressed way later in the guide, since it only applies to Root + Overclock Users)**
  * Load Thresholds **(Especially Important in Games x2)**
  * System Bandwidth
  * Cooling Solution

    Let's Address each of these points one at a time, before we get down to the actual Benchmarking Tools you have to obtain to properly Benchmark. We will start following a Priority Order. The most 
    frustratingly important things will come first.

    ## NUMBER ONE!
    Thermal Throttling + Cooling Solution

    Man. You heard of this already. Who didn't? In order to keep itself safe, any piece of silicon is instructed by software and/or hardware to obey to a set Maximum Temperature, which as you may know, 
    is defined by °C or °F or K or whatever the hell you use, doesn't matter. Too hot, BAD. Too cold, Ehhhhh it depends (More on this later).

    This is usually not a problem for Desktop Devies. Big, Strong, Mighty active cooling systems are ready to dispatch the heat produced by your CPU/GPU/RAM and others with incredible speed and 
    efficiency, so long as it's properly maintained.

    Well, most Mobile Devices don't really have access to that. Those little Systems on a Chip are forced to be sandwiched in minuscule Passive Cooling Systems, that nowadays often rely on the "Vapor 
    Chamber" technology (It's just nerdy terms for a copper slab with some droplets of a thermally conductive liquid in it that evaporates when stuff gets hot to get heat away, with questionable 
    efficacy).

    So as you might have figured already by now, this is not good news for something that produces tons of heat such as modern mobile phones's SoCs. And it indeed isn't. Snapdragon 8 Gen 2, Apple A16 
    Bionic, Dimensity 9200 etc, they all thermal throttle and they thermal throttle hard.

    Now, now, I know. The OEMs are telling you that "uhm actually 8 Gen 2 is super efficient and runs ultra cool and thanks to this new ultra protonic cooling system the temps are 5203% lower with 534% 
    more vapor cooling are-"

    **Yeah, you get what I mean, right?**

    I want you to **Forget** all that you've been told about it.

    Snapdragon 8 Gen 2 and pals, they all overheat. And they overheat badly. OEMs just got good at not letting you know. You might know Snapdragon 810 
    and 8 Gen 1 for being infamous power hogs that burn your hands, and don't get me wrong, their silicon is actually bad, but they aren't bad chips on paper. They were simply harder to **manage**. 
    which  meant OEMs had to spend more for cooling (Spoiler alert: They weren't willing to do so), and as we all know, that didn't work out. 8 Gen 1 and Co were shipped with underwhelming cooling 
    solutions that helped people get their hands acquainted to the feeling of a Samsung Galaxy Note7 without risking to lose their life in the process.

    Most of the benchmark scores you've been given by leaks and whatnot, they are a lie. They are hardly indicative of the real performance of the SoCs we have in our hands. Few people are able to 
    efficiently keep these chips under control, and even fewer actually care about it.

    So for this area, in a nutshell, Thermal Restraints are a dominant variable behind your lackluster benchmark scores. Your phone has a powerful Chip but the cooling is as good as a PC with fried 
    fans and peanut butter for CPU thermal paste.

    Also another thing that you've probably always had standing right in front of your eyes but you never really thought much of it, because you've been fooled, like the rest of us.

    Ever heard of IHS? Stands for **Integrated Heat Spreader**. Yeah, the one that you remove from CPUs to do delidding if you're an enthusiast, right? The IHS is metal, right? Yeah! It's metal. Metal 
    is great at conducting heat! What would we do without metal for IHS on CPUs? God bless metal.


    **The IHS of your Mobile Phone's Chip is Plastic, and they know you don't realize it.** To you the Conclusion for that. I have faith you can realize instantaneously what that means.


    **Alright this is if you're a bit dense. Plastic is a big no no for heat transfer. Heat is trapped, phone overheats. No matter what Cooling System they sponsor for the device. It's the Root of All 
    Evil. Heat can't escape fast enough. Physics bro.**
 
    Most Modern Mobile Devices have a throttling threshold set at 95°C. Sounds quite high, right? Yeah, it is, but it's a necessary evil. It's regualarly met anyway. These phones would need to run at
    130°C in order to not throttle, which is completely unreasonable.
 
    **Colder IS better** when it comes down to benchmarking, but our Lithium batteries dislike it if it drops too low, so be careful. Anything below 10°C on battery requires careful planning and a lot
    of attention. Battery Voltage drops with temperature, and if it gets too low, phone will shut down under load due to Vdrop below Critical Threshold (Load on the battery will cause its voltage to
    drop. If the voltage drops too low, components will starve from voltage, crashing the device. Alternatively, if there's an overwhelmingly high current requirement but the voltage is high enough,
    the phone will power throttle, and the performance will be crippled, but at least the device won't shutdown).

    ## NUMBER TWO!
    Background Processes

    Well you see, this normally wouldn't be a problem. This actually hardly is ever a problem on Desktop PCs, since people are sane enough to close apps that are running there. But you see, Google likes
    to make our life impossible so Android runs 4000 background processes just for the fun of it. I offer my deepest apologies to iOS users, since you guys are cursed as well, well, a bit less, but the
    difference is that you guys can't do anything about it.

    So anyways, Mobile Benchmark results are often tainted by the absolutely insane amount of apps that people run on their devices for no reason. Big Rule if you want to benchmark, KEEP THAT APP 
    HISTORY CLEAN. Apps take memory, bandwidth and CPU cycles as they run, and that means less power to allocate to the task you want to run and obtain a rating for. Less Power available means lower 
    scores.

    There's no "One-For-All" solution to get rid of background apps. You simply can't ever close them all, you'd eventually crash the system (Yeah, it's that bad). But you can at least get rid of apps 
    that YOU installed and that are running in the background without telling you.

    With root, a lotta things are possible, but for this guide I'll assume you don't have root and that you're **dense as hell**.
    Your phone has a thing called "Developer Options" in the Settings. Varies according to the manufacturer how you get to it, but normally you have to find your phone's build number in the settings
    and tap on it 7 times. Afterwards, scroll to the bottom and find the Background Limit and put "No Background Apps".

    Obviously, that won't close all the background apps, since many are seriously stubborn, but that's all you can do if you're a non root user, other than clearing your app history and uninstalling
    apps that might be taking up power. Most manufacturers offer you the ability to check what apps are running behind the scenes, and that's good. Check which ones are, and shut them down. This is
    **fundamental**.

    Usually a fresh reboot and setting of "No Background Apps" In developer options should do it for 90% of cases. If your phone is bloated as hell with useless stuff, for the love of God, format it.
    You won't be getting good results like that, ever.

    ### NUMBER THREE!
    System Bandwidth + Load Thresholds + Frequency Scaling

    **Wow talk about a bundle of factors!**
    
    System Bandwidth is the most important of these factors, however. You may know that any device relies on something called "RAM" to store fundamental data and (especially) move it around. No RAM, no 
    life. RAM is the floor you're walking on. CPU and GPU are simply your legs.

    If you are somewhat acquainted with desktops, you might be familiar with the term "Bottleneck". That's what we are going to treat here. On a respectable Desktop PC, CPU and GPU have separate RAM
    that is dedicated solely to each and often has huge bandwidth. You'd see an Nvidia GPU with super duper fast GDDR6 memory that offers hundreds of GB/s of bandwidth. Same goes for the DDR4 or DDR5
    you might have in your PC. All dedicated to your CPU, to keep it well fed.

    Well, phones have to SHARE. They use something called UMA (Unified Memory Architecture)

    As nobody ever said:

    > What is yours is mine!

    CPU, GPU, NPU, everything in your phone is relying on that same LPDDR4/5 RAM to function, but the bandwidth is one, so they have to share.
    And do you know what happens when you face a group of greedy people with something they really want?
    
    **War.**

    **Alright, it ain't that deep, maybe.**
    
    Basically, your CPU, GPU, any component, they need bandwidth to be kept well fed with data. The moment they are starved, that's when you see a bottleneck in that area. And a bottleneck is literally
    what the word sounds like. A sudden space restriction that chokes out whatever is trying to pass through.

    Something that goes like this, without UMA (Unified Memory Architecture):
 
    -> Data -> Data -> Data --------------------------------------------------> CPU
    
    -> Data -> Data -> Data --------------------------------------------------> GPU
    
    
    

    The one above is a **good** flow. You always want to have a flow that big. Everything is smooth and it goes where it should.
    
     -> Data -> Data -> Data -------------------------------------------------> CPU   -(x) GPU
 
    
    
    And this's a **bad** flow, a small UMA. It's not big enough to house both the data flows. GPU is choking, CPU is good. But the roles may be reversed (Though GPU is often the one that is greedier 
    and needs more data to flow into it).

  What does this mean? This means that GPU will have its performance lowered because the Bandwidth can't keep it working as hard as it possibly could. What does this imply? This implies performance
  being left on the table. In these situations, making GPU more powerful through overclocking is not going to yield any performance benefit, same goes to CPU.

  In simple words, even Modern Phones have limited Bandwidth. This isn't a RAM AMOUNT problem. This is a problem of how much DATA can that RAM send around at any time. Modern phones have powerful
  CPU and GPU that needs to be fed, or else the performance will be crippled.

  It's hard to pinpoint exactly how bad the bottleneck represented by RAM is in these devices, but it's something that mainly affects performance in games.
  Ever heard people recommending to get Dual Channel Memory on Desktop PCs with integrated graphics?  Yeah, we are in that exact same situation on Mobile, except we can't upgrade our RAM for more
  bandwidth.


  **Sad thing, is that there's nothing you can do about it. You'd need to Overclock it, and most OEMs already make it impossibly hard to push CPU and GPU on phones, let alone RAM!**

  **So this whole Third Point was just to let you know that there's a hidden Limiting Factor to your benchmark scores, that nobody will tell you about (Nobody knows about it, actually)**

  Let's move on the next point. Frequency Scaling.
  In order to save power, Phone Manufacturers allow your SoC to lower or raise its frequency according to the load placed on it.

  **Often however, these foolish OEMs are way too conservative, and they will opt to keep the SoC at low frequencies for as long as possible, even if it means crippling your performance (Oneplus,Samsung
  I'M LOOKING AT YOU)***

  This will not necessarily harm your Benchmark scores, since those apps will generally push your SoC to the point where it's forced to run faster. But it can and **WILL harm** your gaming performance 
  and real life usage experience.

  What can you do about it?
  **Nothing. Without root you can't do much about it at all. I feel even more sorry for Apple Users, though they usually don't have this problem, since Apple is less dumb than Android Manufacturers
  in this aspect.**

  Same goes for load thresholds, which are basically set usage targets where the system will be like "Damn, gotta go fast, gotta go fast"

  For example, your CPU's max frequency is 2000MHz, but it won't run at that 24/7. System wants the task you're running to take at least 50% of the CPU Cycles in order to clock the CPU up to that
  2000MHz. Yeah, you get me? Some load must be placed on the device in order to convince it to go full speed.

  **This often causes a peak performance delay, which can harm the score in some Benchmarks**.

  As you may have figured out from this, without rooting, you aren't really going to break any Benchmark records. You must be willing to take extra steps to have a chance. Luckily for you, later on, 
  this guide will include headers for **Root Users**.


  ### Number Four!
  Kernel Performance

  I will try to keep it simple, since this isn't really my area of expertise, but I ran into problems with this before, several times, and it's something even I can't solve. It's up to the **Almighty
  Developer**.

  Not all Kernels are made equal. Some are made buggy, some are made blazing fast. Some Kernel will have flawed performance. This is why Benchmarking is important. You never know what awaits you. 
  Kernel A offers 100% of the CPU performance, but for some obscure reason, Kernel B only accomplishes 80% of the CPU performance of Kernel A, despite running on the same Hardware or hell, even the 
  same OS.

  Nothing you can do about it, other than picking a different Kernel and praying it performs better.
  Luckily, this is a *very* rare problem, and you likely won't have to deal with it.

  With this out of the way, let's move onto the Suggested Benchmarking Suites...but first...

  # USERSIDE BENCHMARK REQUIREMENTS

  * **Patience** (It **WILL** piss you off)
  * **Time** (It **IS** time consuming)
  * **Common Sense** (Perhaps you shouldn't run Linpack outside with 45°C Ambient, right?)
  * **Dedication** (Trial and Error. Every Phone is different. Get to know your phone, study what you care about).


  **Alright let's move onto the Benchmarking Apps/Suites**

  * **AnTuTu Benchmark**

  The Holy Grail of Mobile Benchmarking...right? Right?
  Well, **kinda**. It's good if you got some time to waste and want some arbitrary results. This Benchmark likes to disagree with other (Often more reliable) Benchmarks, but it's the popular Kid, and
  you can't really show up without him at the party, otherwise nobody will care about you. 5/10. Only use this if you have time to waste and you're bored (or you want to prove that you're faster
  to someone who knows nothing about Benchmarks).

  * **3DMARK**

  Now THIS is where the Gold is at! The STATE OF THE ART Benchmark Suite. **THE Game Performance Benchmark**. According to my experience, this Benchmark Suite is the most representative of the
  actual performance you will get in games. It's also **CROSS PLATFORM**, and that's AMAZING for Benchmarking. For modern devices, **Wildlife Unlimited** and **Wildlife Extreme Unlimited** are 
  recommended (Solar Bay Unlimited for Ray Tracing). Why Unlimited?

  **Because you want to be able to compare the performance of your device with upcoming, far faster Chips. The goal of benchmarking is comparison, and what use is a score that is capped by V-sync? You 
  need to run it offscreen, so you can obtain an INDICATIVE result.**
 
  **Note:** 3DMark is mostly a GPU Benchmark Suite, but older subsets of it (Such as Slingshot Extreme and Icestorm) include a CPU section. Older devices (But also newer) should definitely give a shot
  to Slingshot Extreme Unlimited OpenGL ES 3.1, and Slingshot Unlimited OpenGL ES 3.0. They are Legacy Benchmarks by now, but they are still supported and still somewhat intensive.

   **Run Icestorm if you want to see Lightspeed. But don't take its results seriously, unless you're comparing with some really, REALLY old phone.**

  **Note 2:** GPUs of our Mobile Phones tend to overheat way less than the CPU, so in 3DMark you won't have to worry about heating as much, so long as you're using common sense and running your phone 
  in a cool environment. Besides, a number of SoCs still have a very inefficient GPU that can single handedly overheat the whole thing (Such as Snapdragon 888, Dimensity 9200, etc).

  * **GFXBench**

   Another really respectable Benchmarking app. Unfortunately, it's not representative of the Game Performance as much as 3DMark. Its strength is the variety of Feature Tests it offers, as well as the 
   **Cross Platform** nature. If you're looking to compare the raw compute performance of Mobile GPUs, look no further than GFXBench. It's the App you're looking for.

   It has a TON of Benchmark Scenes, but the most important tests for modern devices are Aztec Ruins High Tier Offscreen (Vulkan/OpenGL) and Manhattan 3.1.1 Offscreen, as well as Car Chase Offscreen.
   The Low Level tests are important too, and you should run each and every one of them.

   Overall a very practical and professional Testing Suite. You should have that around.

   * **Basemark GPU**

     Another Cross Platform GPU Benchmarking Application. Way less known than the competitors, but it's still good enough, specially if you're low on time. Run "Official Offscreen Medium" to obtain 
     results that are comparable cross-platform. This Benchmark App even offers the chance to make Custom Runs, unlike Mobile 3DMark.
     This app will also ask you to download either ASTC or ETC2 Texture Compression. Use ASTC. Phones that don't support ASTC usually can't even run the Benchmark anyway. Anything newer than 2015 goes.

   * **Geekbench 6.2.0+**

     A CPU "Real Life Usage Benchmark". The dumbest Benchmark of the decade in my honest and humble opinion, but you're free to use it. It's the new state of the art Cross Platform CPU test anyway. We
     are forced to move on. This Benchmark really likes new SoCs and despises older phones. Takes forever to run. At least it sports 5 seconds cooldown between tasks, which will help your phone not to
     overheat. It's actually a very good feature.
     
   * **Geekbench 5.4.0+**
    
     Arguably the Best Cross Platform CPU Benchmark to date. Not biased, evaluates effective CPU performance, and doesn't take 20 minutes to run, unlike Geekbench 6. Sadly, it only offers a 2 seconds
     cooldown between tasks, which will make your life hard in cooling your phone. Other than that, it's a very effective Cross Platform CPU benchmark, and there isn't much that can replace it.

   * **Geekbench 4.4.0+**
 
     As someone I used to know always said:
 
     > Old is Gold

     Geekbench 4 definitely has its age, but it's still a very valid Cross Platform CPU Benchmark. It's very quick to run and gives results that are about as valid as Geekbench 5's. Thanks to its fast
     run times, Throttling will be less of an issue as opposed to Geekbench 5 and you will be able to get more accurate results.

     **Note for Geekbench Users:** Don't use the "COMPUTE" Benchmark. It's dumb, inaccurate, useless. Rely on the previous GPU Benchmarks I talked about.
     **Benchmark Note:** This is a guide for Peak Performance Evaluation Benchmarking. Sustained Performance Evaluation also exists, as well as Stress Testing, but we will not talk about those in this
     guide. We are just looking to break records. You could use some of the Tweaks we apply before benchmarking in order to extend your battery life or slightly increase performance (Check **Very 
     Important** Section below).

     # Strategies for improving your benchmark scores

     * Purchase a **Peltier Cooler** (Those are **must-have** in your arsenal. They can benefit you in so many ways. Too bad they require an external power source).
       
     * **Don't run Benchmarks repeatedly**. Your phone is passively cooled, even with Peltier. It will take time to return to a neutral temperature situation. Be mindful.
       
     * Use light weight monitoring apps such as CPU Float to study the behaviour of the phone's CPU/GPU under stress, and take note of the temperature. This will help you tailor your strategy
       to your phone's behaviour, in order to optimize the scores. You can even use CPUFloat to measure the current loss (Which is the Power Draw of the phone, and it must be converted in W to be
       useful). Another great app for this purpose is Devcheck. It's heavier on the system, but it's great to ACCURATELY analyse temperatures and a bunch of other things (CPUFloat is VERY OFTEN 
       inaccurate in that regard). Devcheck is best if used with root, but even non-root users will find use in it. It's better than CPU-Z.
 
       **Note:** Devcheck's Monitoring overlay is reserved to Devcheck Pro Users. I don't really encourage piracy, but I know what you're thinking, and I know you probably know what I'm thinking.
 
     ## (VERY IMPORTANT)
     Before running the Benchmark**, disable Mobile Data, disable Bluetooth, disable GPS, disable Account Sync in the settings and still in the settings, head over to app settings and disable **Google 
     and Google Play Store.** If you have more Google Apps installed that are not fundamental to the system's functioning, disable them too. You can re-enable them after you're done benchmarking.
 
     **Also turn on Plane Mode, and afterwards, re-enable Wi-Fi (Yes, you can do that)**.
 
     We disable Google Apps since they have a really bad habit of running in the background and stealing **a lot** of CPU cycles. Meanwhile we disable Bluetooth, Mobile Data etc to drag down to a
     minimum the heat sources inside your phone. All we want to run is your CPU and/or GPU. Bluetooth also steals some CPU cycles, which nobody likes when benchmarking. So disconnect your headphones 
     bro.
 
     iOS users can't do most of that, but you guys can still enable Plane Mode, Disable Bluetooth and Mobile data, GPS and also disable Background App Refreshing in the settings.

     **Important for some Users:** Stop using LSpeed and FDE.AI or any App that claims to improve your device's performance through miraculous means. They are making it worse.
     
     **Important for Many Users:** Updating your OS is not fundamental. An older patch note is not the end of the world. Anonymous is not after you. Relax.
     
     **Important for Many Users 2:** Most of the time, manufacturers update GPU drivers through OS updates. GPU drivers can bring better benchmark scores by improving performance. This occurrence is
     rare, though. So make sure to update if you get the chance. Latest **isn't always better**, but sometimes, it is. You have to look into it yourself.
 
     **Important For Many Users 3:** Modern Qualcomm devices seem to hide CPU Frequency Throttling even when the SoC is experiencing it, so the user won't be able to know if and when the phone
     is thermal throttling and/or power throttling.
 
     *And this is it for the Regular User side of this Guide! It will be expanded with time, of course, or if I remember anything I might have forgot to add.*

     
     **If People ask Questions I can answer, I will add the reply to the guide so it can all be even more exhaustive.**


     **Well then, time to hop onto the ROOT USERS matter. You guys can do FAAAR more.**


     So, I welcome you to the next Big Thing...

     # THE ROOT USER TECHNOOBFORSALE BENCHMARKING GUIDE!

     **Man. Root is amazing. Too bad that OEMs are pushing hard to make it completely worthless, but they still weren't successful!**

     With root, you can do a lot more things than a normal user. Things that will allow you to gain an "unfair" edge when benchmarking. But does it really matter? All we see is **Scores**.

     **Things you can do with Root for Benchmarking that you can't do on Vanilla:**

     * Overclocking
     * Undervolting
     * Throttling Management
     * CPU/GPU Governor Modifications
     * In-Depth App Management
     * Custom Kernel
     * Custom ROM
     * Charge Current Override
     * A Trillion Other things that aren't for Benchmarking
    
     **But fear not!** All these things that you CAN do for Benchmarking, already do all of the work!

     Let's start off following a Priority Order, of Course.

     ## NUMBER ONE. OVERCLOCKING + Undervolting
 
     ### REQUIREMENTS FOR THESE:
     * Patience (Fine Tuning of Undervolt and Overclock takes time)
     * Time (Look above)
     * Common Sense (If you see a slider, DO NOT drag it all the way to the max you dumb-)

     The number one way of increasing any device's speed. Overclocking is the holy grail of **free extra perforamnce**. On PCs it's pretty straight forward to accomplish, and on Mobile Devices the
     situation is similar. However, the recklessness of phone users is, on average, way higher than that of Desktop PC owners. That's why despite how straight forward overclocking usually is, they
     still manage to come back to you with their phone either dead or unstable.


     **What's dangerous about overclocking isn't Overclocking itself. It's who is doing it.**
  
     So, under this point of view, a CPU works something like this.

     CPU A is running at 1000MHz, with MHz being the measurement unit for the Frequency of a Processor.
     In order to run at 1000MHz, CPU A requires 1V. V being Volts, the measurement unit for the Voltage applied to the silicon.

     Insufficient voltage will cause instability and eventually will crash the system. Excessive voltage, on the other hand, will damage a system, in time, or instantaneously, depending on how **dumb**
     the Overclocker is.

     So in order for someone to increase the clockspeed of a CPU beyond its limit, they need to first do something called "Overvolting", which is the opposite of Undervolting. Done responsibly,
     increasing the voltage will not be inherently dangerous for the Processor. There are two danger factors for a CPU, in fact.

     * Voltage
     * Heat
    
     Overclocking increases **Both**. But luckily, they can be kept under control, especially Heat. By raising the frequency of a CPU, you're pretty much forced to increase the voltage. There's no
     getting around it. But the heat can be limited, either through more powerful cooling or a Thermal Throttling threshold.

     First however, let's introduce you to another concept too, so I can bring ourselves to the next point to maximize the safety of Overclocking.

     **Undervolting**

     Undervolting is the process of lowering a component's operating voltage to reduce heat output, power consumption and, to some extent, extend the useful life of the chip. without losing performance,
     unlike **underclocking**.
     
     Either way, what if I told you that 1V for **CPU A** is actually too much to sustain that 1000MHz target?

     That's right. Most manufacturers ship their CPUs to you with a significant margin for undervolting. That's because they produce millions of CPUs, and they don't want to risk shipping
     unstable chips, that's why they set a higher-than-necessary voltage for the chip.

     Luckily for us, most of the time, our chip has quite some headroom for undervolting.

     Let's say that this chip can actually handle the same 1000MHz while running at 0.9V instead of 1V. That's pretty good, right? Indeed! And this improvement, thanks to **undervolting**, also implies
     something else, something pretty amazing.

     **The Chip can handle a higher Frequency, while running the stock voltage (1V)**

     This means that you can obtain extra performance without any risk. In fact, doing some testing, we discovered that CPU A can actually handle 1100MHz at 1V! That's a 10% increase in frequency
     with a 0% increase in voltage compared to where we started from!

     This is why as a rule of thumb, you should **always** undervolt before you overclock, so that you get to know your CPU better, and see what it's capable of.
     
     **If you want to go further however, you will need to start increasing the voltage gradually to make higher frequencies stable.**
 
     **Undervolting should be performed with -25mV steps in order to ensure you gradually reach the point of instability. 25mV = 0,025V**
     **Meanwhile, for Overclocking, voltage should be increased with +25mV steps in case the default Voltage for the specified Frequency is unstable, until reliable.**

     Unlike PCs however, you're not free to set frequencies on Mobile. You are bound to a **Frequency Table**. Said frequency table already has default voltages assigned to it for each frequency step 
     (This is to make Frequency scaling possible, in order to save power).  This means that you will have to test those frequencies first and evaluate if they are stable at the default voltage. 
     Usually, anything above stock is at risk of being unstable, so you'll have to tune it as you see fit. If they are stable however, you can start undervolting the overclocked frequencies, too.

     Eventually, of course, you'll hit a roadblock, as the efficiency of CPUs decreases as the frequency goes up. More effort, less gains. So it's about striking the perfect balance.
     On phones, overclocking and undervolting are accomplished through Kernel Managers (A GUI for the User to manage Kernel parameters). To enable these features however, you require a *Custom Kernel*.

     Custom Kernels are a **must have** after you root your device, since they can potentially improve performance, battery life and introduce new features, too. Stock Kernels usually are not
     that good, and you can't do much with them other than performing **CPU/GPU Governor Modifications** and **Modifying Charge Current**.

     **The Price of Overclocking is Heat.** And as you may have already seen before, our devices already overheat at stock, so what exactly is the point here, what are we going to gain?
     That's a good question actually. This is why Benchmarking on Mobile is so hard. It's like mantaining your balance on a rope with nothingness beneath your feet. We do have some cards
     that come to our assistance, but they depend from the Custom Kernel, whether they are available or not.

     One of them is...

     ### Throttling Management

     Some Custom Kernels offer you the ability to tune the throttling threshold of the SoC. If increased, that will allow you to give the CPU more headroom to unleash its peak performance, before
     it's forced to downclock itself again to prevent Overheating. **Time is Points** in this case. The longer you can sustain peak performance, the higher you will score. So, your ability to
     **Cool the Device Down** is **Fundamental**.

     * Low Ambient Temperature
     * Peltier Cooling
    
       These two factors will often aid you quite a lot to obtain higher scores. However, in all fairness, they aren't enough, most of the time, specially after overclocking. So you need to be stubborn
       and push the temperatures **as low as you possibly can** before running any benchmark. You must play your cards right.

       **Another thing to keep in mind is what I call POWER CRASH**

       If you ever run a stressful Benchmark, with an overclock, after confirming that the voltage is perfectly stable, and yet the phone **SUDDENLY SHUTS DOWN**, that right there my friend, that's a
       **Power Crash**.

       In simple words, your phone's CPU/GPU required way too much Voltage and Current at the same time for the battery to handle. When load is placed upon a battery, it will experience something called
       **Vdrop**. This means that the battery's voltage will start dropping as current and voltage requested increases.

       **If the Load is excessive, the battery will eventually cross the minimum voltage threshold (Usually 3.2V). If that happens, the phone will **instantly** shutdown.**
       A CPU crash is often different from this, as it will freeze the phone first. Power Crashes however are similar to **Thermal Shutdowns**, in the sense that the phone will just go black and reboot.
       
       **(Thermal Shutdowns occur when despite the Thermal Throttling threshold, the phone keeps getting hotter, eventually hitting the shutdown temperature, which will crash the phone to keep it 
       safe from damage)**.

       Luckily, Power Crashes are usually only a problem for **old batteries, old phones and some lower tier phones.**

       Old Batteries because they lose their ability to provide Voltage and Current.
       Old Phones because they have weaker batteries and often fail to keep up with the demand.
       Lower tier phones because they also have weak batteries, and sometimes, weak charging speed.

       In fact this brings us to our next point. **Charging**.

       Charging is a **MUST** when running benchmarks on an overclock. It helps keeping your battery **up and running**, and prevents Power Crashes. Newer phones have insanely strong charging currents,
       so it's likely that so long as they are plugged in, they will be able to handle any overclock, till the limits of the CPU itself are reached.

       Older phones however, have relatively slow charging, which can quickly be saturated by the power demand of the system, causing a shutdown regardless.

       **So, for serious overclock Runs, make sure your phone is plugged in and fast charging at a Battery Percentage around 65-70% (This is the spot where the battery charges the fastest but also has
       the highest voltage).** 

       Lower means more charge current but less voltage available, and more means less charge current but more voltage available. Higher battery percentages will prevent a Power Crash, but a **Power 
       Throttle** will be more likely (The CPU downclocking itself due to sufficient voltage but insufficient Current being delivered to it).

       **To test Overclock Stability, I recommend Geekbench 5 for CPU and 3DMark Wildlife Unlimited and Slingshot Extreme Unlimited OpenGL ES 3.1 for GPU.**

       Geekbench 5 tests SINGLE CORE PERFORMANCE from 0% to 50% of the Benchmark run. So if the CPU crashes within that time, it's likely that your phone's Prime Cores are the problem. If it crashes
       later on, after 50%, other cores are the problem. Rembember that instant shutdown indicates a Power Crash (A Thermal Shutdown is quite rare unless you deliberately disabled Thermal Throttling,
       which I absolutely don't recommend).

       **Keep in mind that your phone's CPU is made by a variety of different cores. Usually a Strong Core, a bunch of Middle Cores and a bunch of power saving cores**.

       Signs of **Strong and Middle Cores instability**:
       * Apps Crashing
       * Inability to open apps
       * System Freeze
      
       Signs of **Power Saving Cores Instability**:
       * System freeze with shutdown
       * Sudden shutdown
      
       **Little Cores are, actually, the main Cores the system relies on to keep its runtime going. If Core 0 (Which is a Power Saving Core) crashes, the system will crash.**

       With that being said, let's go on.

       Signs of **GPU Instability**:
       * Screen Freeze or very low refresh rate or even black screen (System still responsive)
       * Artifacts while playing games
       * Poor FPS
       * Games/Benchmarks Freezing
      
       GPU is by far the least bothersome to deal with when it's unstable, since it hardly will crash the system, unless you messed up big time with the voltages, the frequency, or both.

       ### A Very Important Detail:

       We talked about this before. **Memory Bandwidth**. When overclocking GPU and CPU in a smartphone, you are likely to hit that wall harder than you would ever imagine. So your overclock might
       not be as effective as it should be, due to Bandwidth bottlenecks. GPU is mainly affected by this, since it's the greedier component when it comes down to bandwidth requirements.

       **Signs of Memory Bandwidth Bottlenecks:**
       * Little to no performance Gain in games
       * Poor GPU performance increase in Benchmarks/Games
       * Stutters, Late Texture Loading (Visible in games such as Genshin Impact)
       * **Performing the same GPU Benchmark at a lower resolution with and without overclock shows that the difference between Stock and OC is even smaller**
      
       The only fix for limited Memory Bandwidth is overclocking, but unfortunately, on most devices, RAM Overclocking is not something that Developers look a lot into, and if they do, it's really
       hard to mess with, which is very unfortunate.

       **Memory Bandwidth is so important that if you had the chance to overclock RAM alone, your device's CPU and GPU performance would VERY likely go up, even without touching their frequencies at 
       all.**

       So if you accomplish an impressive overclock for GPU (Rarely does Bandwidth cripple CPU) but the results are disappointing, be quick to blame Memory Bandwidth. Even I would've never imagined
       it to be the problem, yet it's such a no brainer if you think about it. Integrated Graphics. They NEED bandwidth, and if they have it, they become way faster.

       **Things obvious to this extent, that are right in front of our eyes, yet anyone hardly even notices.**

       **Well I did notice, and now I'm telling it to you, and I hope it will help you in whatever way.**

      #### This Guide Will be Updated as Questions are asked and/or I remember more things that are worth mentioning.

     - Last Revision: 0.8 (24/09/2023 16:27:05)
      
         
