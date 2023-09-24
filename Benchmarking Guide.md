# Benchmarking-For-Dummies Rev 0.1
A Repository containing knowledge about the trivial "art" of Benchmarking, specifically mobile devices.

### Has Benchmarking Mobile Phones ever crossed your mind?

Probably, it did. And that's pretty neat. But you see, Benchmarking Phones is way more tricky than it would normally be on a Desktop PC. You have to keep in mind many, MANY variables that OEMs usually lead you to believe to be completely irrelevant. But that's wrong. And in this guide I will show you why, and I will make you a better Benchmarker in the process. 

**Very well then, shall we begin? Allow me to introduce you...to the Official TECHNOOBFORSALE Mobile Benchmarking Guide.**

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

    **NUMBER ONE!**
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

    **NUMBER TWO!**
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

    **NUMBER THREE!**
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

    Something that goes like this, without UMA:
 
    -> Data -> Data -> Data --------------------------------------------------> CPU
    
    -> Data -> Data -> Data --------------------------------------------------> GPU
    
    
    

    The one above is a **good** flow. You always want to have a flow that big. Everything is smooth.
    
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

  This will not necessarily harm your benchmark scores, since they will generally push your SoC to the point where it's forced to run faster. But it can and **WILL harm** your gaming performance and 
  real life usage experience.

  What can you do about it?
  **Nothing. Without root you can't do much about it at all. I feel even more sorry for Apple Users, though they usually don't have this problem, since Apple is less dumb than Android Manufacturers
  in this aspect.**

  Same goes for load thresholds, which are basically set usage targets where the system will be like "Damn, gotta go fast, gotta go fast"

  For example, your CPU's max frequency is 2000MHz, but it won't run at that 24/7. System wants the task you're running to take at least 50% of the CPU Cycles in order to clock the CPU up to that
  2000MHz. Yeah, you get me? Some load must be placed on the device in order to convince it to go full speed.

  **This often causes a peak performance delay, which can harm the score in some Benchmarks**.

  As you may have figured out from this, without rooting, you aren't really going to break any Benchmark records. You must be willing to take extra steps to have a chance. Luckily for you, later on, 
  this guide will include headers for **Root Users**.


  **Number Four!**
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
  you can't really show up without him at a party, otherwise nobody will care about you. 5/10. Only use this if you have time to waste and you're bored.

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

   * **Geekbench 6.2.0+**

     A CPU "Real Life Usage Benchmark". The dumbest Benchmark of the decade in my honest and humble opinion, but you're free to use it. It's the new state of the art Cross Platform CPU test anyway. We
     are forced to move on. This Benchmark really likes new SoCs and despises older phones. Takes forever to run. At least it sports 5 seconds cooldown between tasks, which will help your phone not to
     overheat. It's actually a very good feature.
     
   * **Geekbench 5.4.0+**
    
     Arguably the Best Cross Platform CPU Benchmark to date. Not biased, evaluates effective CPU performance, and doesn't take 20 minutes to run, unlike Geekbench 6. Sadly, it only offers a 2 seconds
     cooldown between tasks, which will make your life hard in cooling your phone. Other than that, it's a very effective Cross Platform CPU benchmark, and there isn't much that can replace it.

   * **Geekbench 4.4.0+**
 
     As someone I used to know said:
 
     > Old is Gold

     Geekbench 4 definitely has its age, but it's still a very valid Cross Platform CPU Benchmark. It's very quick to run and gives results that are about as valid as Geekbench 5's. Thanks to its fast
     run times, Throttling will be less of an issue as opposed to Geekbench 5 and you will be able to get more accurate results.

     **Note for Geekbench Users:** Don't use the "COMPUTE" Benchmark. It's dumb, inaccurate, useless. Rely on the previous GPU Benchmarks I talked about.

     # Strategies for improving your benchmark scores

     * Purchase a **Peltier Cooler** (Those are really a good addition to your arsenal. They can benefit you in so many ways. Too bad they require an external power source)
     * **Don't run Benchmarks repeatedly**. Your phone is passively cooled, even with Peltier. It will take time to return to a neutral temperature situation. Be mindful.
     * Use light weight monitoring apps such as CPU Float to study the behaviour of the phone's CPU/GPU under stress, and take note of the temperature. This will help you tailor your strategy
       to your phone's behaviour, in order to optimize the scores.

     **Important for some Users:** Stop using LSpeed and FDE.AI or any App that claims to improve your device's performance through miraculous means. They are making it worse.
     **Important for Many Users:** Updating your OS is not fundamental. An older patch note is not the end of the world. Anonymous is not after you. Relax.
     **Important for Many Users 2:** Most of the time, manufacturers update GPU drivers through OS updates. GPU drivers can bring better benchmark scores by improving performance. This occurrence is
     rare, though. So make sure to update if you get the chance. Latest **isn't always better**, but sometimes, it is. You have to look into it yourself.
 
     *And this is it for the Regular User side of this Guide! It will be expanded with time, of course, or if I remember anything I might have forgot to add.*

     **Root Users Guide Expansion Coming soon.**
     **If People ask Questions I can answer, I will add the reply to the guide so it can all be even more exhaustive.**
  
    
