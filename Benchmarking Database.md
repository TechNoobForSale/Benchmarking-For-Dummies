# This File is a Database of the benchmarks from all devices I currently own, as well as my own remarks about each result. 
## You may use this for comparison purposes. It will be updated more and more with time. A variety of benchmarks will be included. 


### Applications include but are not limited to: 3DMark, Geekbench 4, GFXBench 

### Data created:  22/01/2023
### Data update 1: 24/01/2023
### Data Update 2: 04/08/2023
### Github Upload on: 18/11/2023  

## NOTE: These benchmarks are performed with high levels of attention to prevent overheating or background apps interference so they are to be taken as BASELINES for comparisons.

# Devices Involved:
### Samsung Galaxy S8 (E8895, 4GB RAM) (Further Testing Planned|2704MHz,839MHz)

### Samsung Galaxy Note9 (E9810, 8GB RAM)

### Samsung Galaxy S5 (MSM8974AC, 2GB RAM) (Further Testing Planned|2899MHz)

### Samsung Galaxy Tab 2 8'0 (OMAP 4430, 1GB RAM)

### Samsung Galaxy Tab E 9'6 (Spreadtrum SC7730SE 4xCortex A7 @1300MHz, Mali 400 MP2 512MHz, 1.5GB RAM)

### HMD Global Nokia 8 (MSM8998, 4GB RAM)

### Huawei P8 Lite (2015) (K620, 2GB RAM)

### Samsung Galaxy S3 (E4412, 1GB RAM)

### Asus Vivobook 2013 (i7 4500U + GT 740m, 8GB RAM) (Further Testing Planned|Better Score)

### Asus ROG Strix G15 (R9 5900HX + RTX 3060M, 32GB RAM) (Further Testing Planned|uV)
### HP Probook 4310s (Core 2 Duo T6570 + ATi Mobility Radeon 4330, 4GB RAM)

### iPad Pro 2020 11' (A12Z, 6GB RAM)

### Realme GT Neo 2 (Snapdragon 870, 8GB RAM) (External Device, may lack data)
### Desktop PC (i5 12600K + RTX 3060 Ti, 16GB RAM)(External Device, may lack data)

## TEST SUITE LOG

-----------------------------------------------
# HP Probook 4310's Data:                         <--
-----------------------------------------------
### (Under Load) Benchmark: Icestorm Unlimited

### Stats: Core 2 Duo T6570: 2094MHz|GPU: 450MHz

Total Score: 17,321

GPU SCORE: 18,073

GPU Test 1: 125,82FPS

GPU Test 2: 57,13FPS

CPU SCORE: 15,122

CPU Test: 48,01FPS

------------------------------------------------

(Full Power, GPU Overclock):
Benchmark: Icestorm Unlimited
Stats: Core 2 Duo T6570 @2094MHz|GPU: 625MHz
Total Score: 21,326
GPU SCORE: 23,952
GPU Test 1: 170,07FPS
GPU Test 2: 75,05FPS
CPU SCORE: 15,414FPS
CPU Test: 48,94FPS
------------------------------------------------
(Full Power,CPU, GPU Overclock):
Benchmark: Icestorm Unlimited
Stats: Core 2 Duo T6570 @2802MHz|GPU: 625MHz
Total Score: 21,326
GPU SCORE: 23,952
GPU Test 1: 170,07FPS
GPU Test 2: 75,05FPS
CPU SCORE: 15,414FPS
CPU Test: 48,94FPS
------------------------------------------------
Benchmark: Cloud Gate 
Stats: CPU: 2094MHz|GPU: 450MHz
Total Score: 1,287
GPU SCORE: 1,297
GPU Test 1: 6,01FPS
GPU Test 2: 5,31FPS
CPU SCORE: 1,254
CPU Test: 3,98FPS
------------------------------------------------
Benchmark: Cloud Gate
Stats: CPU: 2094MHz|GPU: 625MHz
Total Score: 1,618
GPU SCORE: 1,770
GPU Test 1: 8,32FPS
GPU Test 2: 7,16FPS
CPU SCORE: 1,246
CPU Test: 3,96FPS
------------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 2094MHz|GPU: 625MHz
Single Core: 1,396
Multi Core: 2,322

Single Stats:
Crypto: 99
Integer: 1705
Floating Point: 1142
Memory: 1406

Multi Stats:
Crypto: 196
Integer: 3087
Floating Point: 2144
Memory: 1398
-------------------------------------------------


------------------------------------------------
# Samsung Galaxy S8's Data                         <--
------------------------------------------------
(Devcheck Open, Naptime Open, Accubattery Open, Devcheck Open):
Stats: CPU: 2314/1690|GPU: 572MHz
Benchmark: Icestorm Unlimited
Stats: M2 Cores: 2314MHz|A53 Cores: 1690MHz|GPU: 572MHz
Total Score: 37,085
GPU SCORE: 41,473
GPU Test 1: 194,9FPS
GPU Test 2: 167,8FPS
CPU SCORE: 27,064
CPU Test: 85,9FPS
------------------------------------------------
Stats: Big: 2652MHz|Little: 2002MHz|GPU: 764MHz, GPU score seems anomalous. Probably CPU Bottleneck
Benchmark: Icestorm Unlimited
Total Score: 41,388
GPU SCORE: 45,379
GPU Test 1: 206,4FPS
GPU Test 2: 188,9FPS
CPU SCORE: 31,647
CPU Test: 100,5FPS
------------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 2652/2002MHz|GPU:764MHz

Single Core: 2214
Multi Core: 7556
-Note: The CPU was unfortunately throttling down to 2496MHz occasionally. 7600+ Multi is possible at 2652MHz.
Single Core Stats:
Crypto: 1,429
Integer: 2,336
Floating Point: 1,812
Memory: 2,740

Multi Core Stats:
Crypto: 6,921
Integer: 9,730
Floating Point: 7,325
Memory: 3,172
----------------------------
-2314/1690 run (Stock) - seems to not have throttled
Single Core: 2,006
Multi Core: 6,850

Single Core Stats:
Crypto: 1,252
Integer: 2,075
Floating Point: 1,586
Memory: 2,669

Multi Core Stats:
Crypto: 6,154
Integer: 8,686
Floating Point: 6,707
Memory: 3,110
------------------------------------------------
Benchmark: Slingshot Unlimited:
Stats: CPU: 2652/2002MHz|GPU: 764MHz
-Note: CPU occasionally throttled down to 2496MHz in the CPU test. 5,000+ score is possible but only at 839MHz GPU, but I prefer not to run benchmarks at unreliable frequencies (839MHz requires significantly higher voltage than 764MHz to run (And runs SIGNIFICANTLY hotter too), but does not give a significant performance benefit).
Total Score: 4,785 (5,047 recorded at 839MHz GPU)
GPU SCORE: 5,539 (6,048 at 839MHz)
GPU Test 1: 34,4FPS (37,4FPS at 839MHz)
GPU Test 2: 18,5FPS (20,3FPS at 839MHz)
CPU SCORE: 3,240
CPU Test 1: 54,1FPS
CPU Test 2: 34,5FPS
CPU Test 3: 18,3FPS
-----------------------------------------------
Benchmark: Slingshot Extreme Unlimited OpenGL ES 3.1
Stats: CPU: 2652/2002MHz|GPU: 839MHz
-Note: Second run will be at 764MHz. 839MHz test is, once again, merely for numbers. Note well, that CPU in these tests has probably dropped from 2652 down to 2496-2314MHz. Heat from the processor is nearly unmanageable for this phone. 839MHz GPU did not throttle, however it reached 99°C, which was just 1°C shy of thermal throttling. For comparison, 764MHz merely went up to 67°C. Big difference. Leaves headroom for the CPU, which in fact on the 764MHz run scored higher.
Total Score: 4,060 (Though I've seen very slightly higher scores in the past)
GPU SCORE: 4,438
GPU Test 1: 32,7FPS
GPU Test 2: 13,7FPS
CPU SCORE: 3,128
CPU Test 1: 56,0FPS
CPU Test 2: 31,9FPS
CPU Test 3: 17,7FPS

-764MHz GPU Run
Total Score: 3,903 (Though I think I've seen very slightly higher scores in the past)
GPU SCORE: 4,151
GPU Test 1: 31,0FPS
GPU Test 2: 12,7FPS
CPU SCORE: 3,228
CPU Test 1: 56,3FPS
CPU Test 2: 33,9FPS
CPU Test 3: 18,1FPs
--------------------------------------------------
Benchmark: Miscellaneous GFXBench (2314/1690/764):
Notes: Slight GPU Throttling noticed in some workloads. It's unavoidable with my current cooling.
Render Quality (High Precision): 3.636 mP PSNR
1080p Texturing Offscreen: 10.890 MTexels/s
1080p Tessellation Offscreen: 72FPS (4.300 Frames)
1080p ALU 2 Offscreen: 132FPS (7.895 Frames)
1080p Driver Overhead 2 Offscreen: 19FPS (1.160 Frames)
1080p T-Rex Offscreen: 142FPS (7.947 Frames)
1080p Manhattan 3.0 Offscreen: 86FPS (5.341 Frames)
1080p Manhattan 3.1 Offscreen: 60FPS (3.721 Frames) Note: This was probably achieved at 839MHz
1440p Manhattan 3.1.1 Offscreen: TBD
1080p Car Chase Offscreen: 33FPS (1.960 Frames)
1080p Aztec Ruins Vulkan Normal Tier Offscreen: 31FPS (1.986 Frames)
1080p Aztec Ruins OpenGL Normal Tier Offscreen: 37FPS (2.356 Frames)
1440p Aztec Ruins OpenGL High Tier Offscreen: 13FPS (845 Frames)
----------------------------------------------------------------------

------------------------------------------------
# Samsung Galaxy Note9's Data                      <--
------------------------------------------------
(Same load as first S8 benchmarks), Stock with no boost
Benchmark: Icestorm Unlimited
Stats: M3 Cores: 1794MHz (No Boost)|A55 Cores: 1794MHz|GPU: 572MHz
Total Score: 47,563
GPU SCORE: 54,910
GPU Test 1: 285,8FPS
GPU Test 2: 205,0FPS
CPU SCORE: 32,394
CPU Test: 102,8FPS
------------------------------
Benchmark: Icestorm Unlimited
Stats: Big: 2314MHz (With Boost up to 2886MHz)|Little: 2002MHz|GPU: 598MHz
Total Score: 57,822
GPU SCORE: 64,952
GPU Test 1: 349,3FPS
GPU Test 2: 237,0FPS
CPU SCORE: 41,773
CPU Test: 132,6FPS
------------------------------
Benchmark: Wildlife Unlimited
Stats: GPU @598MHz
Score: 2,489 (2,802 with A12)
FPS: 14,9FPS (16,8FPS with A12)
-------------------------------
Benchmark: Wildlife Unlimited
Stats: GPU @730MHz, Android 12 
Score: 3,110
FPS: 18,6FPS
-------------------------------
Benchmark: Slingshot Unlimited
Stats: 2002/2002/740, Android 12
TOTAL: 6,060
GPU SCORE: 7,421
CPU SCORE: 3,691
GPU Test 1: 42,8FPS
GPU Test 2: 25,9FPS
CPU Test 1: 62,5FPS
CPU Test 2: 37,9FPS
CPU Test 3: 21,2FPS
---------------------------------
Benchmark: Slingshot Extreme OpenGL ES 3.1 Unlimited:
Stats: 2002/2002/730, Android 12
Notes: On Android 10, a higher GPU and overall score has been achieved thanks to 800MHz GPU)
Total: 5,126 (5,184 on A10)
GPU SCORE: 5,761 (6,086 on A10)
CPU SCORE: 3,700
GPU Test 1: 39,2FPS (41,4FPS on A10)
GPU Test 2: 18,4FPS (19,4FPS on A10)
CPU Test 1: 63,4FPS
CPU Test 2: 37,3FPS
CPU Test 3: 21,3FPS
-------------------------------------
Benchmark: Miscellaneous GFXBench
Stats: 2704/2314/1794/710, Android 12

Render Quality (High Precision): 3.635 mB PSNR
1080p Texturing Offscreen: 8.910 MTexels/s
1080p Driver Overhead 2 Offscreen: 34FPS (2.023 Frames)
1080p ALU 2 Offscreen: 125FPS (7.522 Frames)
1080p Tessellation Offscreen: 102FPS (6.106 Frames)
1080p T-Rex Offscreen: 154FPS (8.619 Frames)
1080p Manhattan 3.0 Offscreen: 98FPS (6.059 Frames)
1080p Manhattan 3.1 Offscreen: 58FPS (3.612 Frames)
1440p Manhattan 3.1.1 Offscreen: 33FPS (2.048 Frames)
1080p Car Chase Offscreen: 36FPS (2.119 Frames)
1080p Aztec Ruins Vulkan Normal Tier Offscreen: 35FPS (2.230 Frames)
1080p Aztec Ruins OpenGL Normal Tier Offscreen: 38FPS (2.457 Frames)
1440p Aztec Ruins OpenGL High Tier Offscreen: 13FPS (846 Frames)
-------------------------------
Benchmark: Geekbench 4
Stats: 1924/1950MHz, without boost|GPU: 598MHz
Single Core: 2,928
Multi Core: 9,868

Single Core Stats:
Crypto: 1,480
Integer: 2,738
Floating Point: 2,607
Memory: 4,198

Multi Core Stats:
Crypto: 7,150
Integer: 11,967
Floating Point: 10,697
Memory: 4,582


-2002/2002MHz (Boost disabled, no throttling) Run:
Single Core: 3,013
Multi Core: 10,173

Single Core Stats:
Crypto: 1,540
Integer: 2,861
Floating Point: 2,715
Memory: 4,168

Multi Core Stats:
Crypto: 7,477
Integer: 12,321
Floating Point: 11,106
Memory: 4,612


-2106/2002MHz (Boost disabled, Briefly Throttled to 2002MHz. 10,600 Multi is possible) Run:
Single Core: 3,146
Multi Core: 10,563

Single Core Stats:
Crypto: 1,624
Integer: 3,000
Floating Point: 2,847
Memory: 4,305

Multi Core Stats:
Crypto: 7,530
Integer: 12,848
Floating Point: 11,579
Memory: 4,658


-2314/2002MHz (Boost up to 2886MHz, Throttled down to 2002MHz) Run:
Single Core: 4,014 (Though I've seen up to 4,080)
Multi Core: 11,156 (Probably can surpass 11,200) Update: Record achieved at 11,717 by PrinceHackey

Single Core Stats (2886MHz):
Crypto: 2,225
Integer: 4,060
Floating Point: 3,878
Memory: 4,562

Multi Core Stats (2314MHz):
Crypto: 8,402
Integer: 13,785
Floating Point: 11,943
Memory: 4,748

-1794/1794 (Boost disabled, no throttling) Run:
Single Core: 2,743
Multi Core: 9,225

Single Core Stats:
Crypto: 1,377
Integer: 2,569
Floating Point: 2,443
Memory: 3,925

Multi Core Stats: 
Crypto: 6,711
Integer: 11,205
Floating Point: 9,986
Memory: 4,259

---------------------------------------------------
# Samsung Galaxy S5's Data                            <--
---------------------------------------------------
Benchmark: Icestorm Unlimited
Stats: Krait 300 Cores: 2265MHz|GPU: 462MHz
Total Score: 19,440
GPU SCORE: 20,122
GPU Test 1: 111,4FPS
GPU Test 2: 72,0FPS
CPU SCORE: 17,380
CPU Test: 55,2FPS
----------------------------------------------------
Benchmark: Icestorm Unlimited
Stats: Krait 300: 2841MHz|GPU: 572MHz
Total Score: 23,255
GPU SCORE: 23,852
GPU Test 1: 130,6FPS
GPU Test 2: 86,0FPS
CPU SCORE: 21,380
CPU Test: 67,9FPS
-----------------------------------------------------
Benchmark: Slingshot Unlimited
Stats: CPU: 2265MHz|GPU: 462MHz
Total Score: 1,208
GPU SCORE: 1,160
GPU Test 1: 8,3FPS
GPU Test 2: 3,6FPS
CPU SCORE: 1,411
CPU Test 1: 34,2FPS
CPU Test 2: 15,2FPS
CPU Test 3: 6,9FPS
-----------------------------------------------------
Benchmark: Slingshot Unlimited
Stats: CPU: 2764MHz|GPU: 578MHz
Total Score: 1,437
GPU SCORE: 1,386
GPU Test 1: 9,7FPS
GPU Test 2: 4,4FPS
CPU SCORE: 1,647
CPU Test 1: 38,4FPS
CPU Test 2: 17,1FPS
CPU Test 3: 8,4FPS
------------------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 2764MHz|GPU: 578MHz
Single Core: 1127
Multi Core: 3130

Single Core Stats:
Crypto: 59
Integer: 1218
Floating Point: 774
Memory: 1719

Multi Core Stats:
Crypto: 234
Integer: 4241
Floating Point: 2629
Memory: 2105

-2841MHz CPU Run (Slightly Throttled on AES and SGEMM):
Single Core: 1141
Multi Core: 3187

Single Core Stats:
Crypto: 60
Integer: 1250
Floating Point: 792
Memory: 1690

Multi Core Stats:
Crypto: 237
Integer: 4336
Floating Point: 2678
Memory: 2102

-2265MHz CPU Run:
Single Core: 1,005 (Though I have registered up to 1,017)
Multi Core: 2,799 (Though I have registered up to 2,805)

Single Core Stats:
Crypto: 49
Integer: 1049
Floating Point: 662
Memory: 1659

Multi Core Stats:
Crypto: 191
Integer: 3729
Floating Point: 2306
Memory: 2095
-------------------------------------------------------------
Benchmark: Miscellaneous GFXBench
Render Quality (High Precision): 3.506 mB PSNR
1080p Texturing Offscreen: 3.247 MTexels/s
1080p Driver Overhead 2 Offscreen: 5,2FPS (312FPS, This might've been made on 2841MHz)
1080p ALU 2 Offscreen: 26FPS (1.551 Frames)
1080p T-Rex Offscreen: 27FPS (1.511 Frames)
1080p Manhattan 3.0 Offscreen: 12FPS (761 Frames)

-----------------------------------------------------------


--------------------------------------------------------
# Samsung Galaxy Tab 2 8'0's Data                          <--
--------------------------------------------------------
Samsung Galaxy Tab 2 8'0 (Under Load)
Benchmark: Icestorm Unlimited
Stats: Cortex A9 V1 Cores: 1008MHz|GPU: 307MHz
Total Score: 1,435
GPU SCORE: 1,245
GPU Test 1: 8,0FPS
GPU Test 2: 4,1FPS
CPU SCORE: 3,081
CPU Test: 9,8FPS
-----------------------------------------------------
Galaxy Tab 2 (Full Power, Overclocked):
Benchmark: Icestorm Unlimited
Stats: Cortex A9 V1: 1520MHz|GPU: 512MHz
Total Score: 2,342
GPU SCORE: 2,035
GPU Test 1: 12,3FPS
GPU Test 2: 6,9FPS
CPU SCORE: 4,957
CPU Test: 15,7FPS
-----------------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 1520MHz|GPU: 512MHz
Single Core: 436
Multi Core: 732

Single Core Stats:
Crypto: 24
Integer: 616
Floating Point: 289
Memory: 355

Multi Core Stats:
Crypto: 49
Integer: 1097
Floating Point: 528
Memory: 386
------------------------------------------------------

-----------------------------------------------------
Samsung Galaxy Tab E 9'6's Data                       <--
-----------------------------------------------------
Samsung Galaxy Tab E 9'6 (Under load)
Benchmark: Icestorm Unlimited
Stats: Cortex A7 Cores: 1300MHz|GPU: 512MHz
Total Score: 2,685
GPU SCORE: 2,343
GPU Test 1: 9,7FPS
GPU Test 2: 10,8FPS
CPU SCORE: 5,484
CPU Test: 17,4FPS
--------------------------------
Samsung Galaxy Tab E 9'6 (Full Power):
Benchmark: Icestorm Unlimited
Stats: Cortex A7: 1300MHz|GPU: 512MHz
Total Score: 2,866
GPU SCORE: 2,411
GPU Test 1: 9,8FPS
GPU Test 2: 11,3FPS
CPU SCORE: 8,428
CPU Test: 26,8FPS
--------------------------------
Benchmark: Geekbench 4
Stats: CPU: 1300MHz|GPU: 512MHz
Single Core: 410
Multi Core: 1098 (Though I might at some point have seen 1100+)

Single Core Stats:
Crypto: 17
Integer: 484
Floating Point: 229
Memory: 611

Multi Core Stats:
Crypto: 71
Integer: 1589
Floating Point: 776
Memory: 735
--------------------------------
Benchmark: GFXBench 1080p T-Rex Offscreen: 3,6FPS (197 Frames)
--------------------------------
HMD Global Nokia 8's Data        <--
-------------------------------
Benchmark: Icestorm Unlimited
Stats: Big: 2361MHz|Little: 1900MHz|GPU: 710MHz
Total Score: 40,016
GPU SCORE: 53,216
GPU Test 1: 283,1FPS
GPU Test 2: 195,6FPS
CPU SCORE: 21,420
CPU Test: 68,00FPS
---------------------------------------------
Benchmark: Icestorm Unlimited
Stats: Big: 2361MHz (2457MHz was ignored by the device)|Little: 2112MHz|GPU: 710MHz
Total Score: 41,291
GPU SCORE: 53,726
GPU Test 1: 286,50FPS
GPU Test 2: 197,2FPS
CPU SCORE: 22,811
CPU Test: 72,4FPS
---------------------------------------------
Benchmark: Icestorm Unlimited
Stats: Same as above, but GPU Drivers updated to V474
GPU SCORE: 57,227
GPU Test 1: 309,3FPS
GPU Test 2: 208,1FPS
CPU Test: 73,8FPS
---------------------------------------------
Benchmark: Slingshot Unlimited:
Stats: CPU: 2361MHz,2112MHz|GPU: 710MHz
Total Score: 5,270
GPU SCORE: 6,507
GPU Test 1: 39,3FPS
GPU Test 2: 22,1FPS
CPU SCORE: 3,165
CPU Test 1: 59,3FPS
CPU Test 2: 33,3FPS
CPU Test 3: 17,3FPS
---------------------------------------------
Benchmark: Slingshot Extreme Unlimited OpenGL ES 3.1
Stats: CPU: 2361MHz,2112MHz|GPU: 710MHz
Total Score: 4,073
GPU SCORE: 4,452
GPU Test 1: 28,5FPS
GPU Test 2: 14,7FPS
CPU SCORE: 3,139
CPU Test 1: 57,6FPS
CPU Test 2: 32,2FPS
CPU Test 3: 17,6FPS
--------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 2361MHz,2112MHz|GPU: 710MHz
Single Core: 1,970
Multi Core: 6,788

Single Core Stats:
Crypto: 1,213
Integer: 2,162
Floating Point: 1,442
Memory: 2,518

Multi Core Stats: 
Crypto: 5,978
Integer: 9,013
Floating Point: 6,232
Memory: 2,818

-2361/1900MHz run (Stock)
Single Core: 1,973
Multi Core: 6,593

Single Core Stats:
Crypto: 1,213
Integer: 2,161
Floating Point: 1,446
Memory: 2,530

Multi Core Stats:
Crypto: 5,856
Integer: 8,704
Floating Point: 6,077
Memory: 2,802
----------------------------------------------
Benchmark: Miscellaneous GFXBench:
Stats: 2361/1900/710
Render Quality (High Precision): 3.632 mB PSNR
1080p Texturing Offscreen: 10.030 MTexels/s
1080p Driver Overhead 2 Offscreen: 71FPS (4.281 Frames)
1080p ALU 2 Offscreen: 91FPS (5.438 Frames)
1080p Tessellation Offscreen: 79FPS (4.746 Frames)
1080p T-Rex Offscreen: 113FPS (6.302 Frames)
1080p Manhattan 3.0 Offscreen: 61FPS (3.761 Frames)
1080p Manhattan 3.1 Offscreen: 42FPS (2.579 Frames)
1440p Manhattan 3.1.1 Offscreen: 23FPS (1.418 Frames)
1080p Car Chase Offscreen: 25FPS (1.460 Frames)
1080p Aztec Ruins Vulkan Normal Tier Offscreen: 28FPS (1.769 Frames)
1080p Aztec Ruins OpenGL Normal Tier Offscreen: 26FPS (1.668 Frames)
1440p Aztec Ruins Vulkan High Tier Offscreen: 9,6FPS (617 Frames)
1440p Aztec Ruins OpenGL High Tier Offscreen: 9,8FPS (629 Frames)

--------------------------------------------
# Huawei P8 Lite (2015)'s Data                 <--
--------------------------------------------
Huawei P8 Lite (2015, Under Load)
Benchmark: Icestorm Unlimited
Stats: Cortex A53 Cores: 1200MHz|GPU: 500MHz
Total Score: 5,448
GPU SCORE: 4,982
GPU Test 1: 18,4FPS
GPU Test 2: 26,3FPS
CPU SCORE: 8,098
CPU Test: 25,7FPS
-----------------------------------
Huawei P8 Lite (2015, Full Power):
Benchmark: Icestorm Unlimited
Stats: Cortex A53: 1200MHz|GPU: 500MHz
Total Score: 5,497
GPU  5,002
GPU Test 1: 18,40FPS
GPU Test 2: 26,5FPS
CPU SCORE: 8,415
CPU Test: 26,7FPS
-----------------------------------
Benchmark: Geekbench 4
Stats: CPU: 1200MHz|GPU: 500MHz
Single Core: 563 (Though I have recorded up to 565)
Multi Core: 2,488

Single Core Stats:
Crypto: 376
Integer: 580
Floating Point: 347
Memory: 894

Multi Core Stats:
Crypto: 2,012
Integer: 3,339
Floating Point: 2,203
Memory: 1,117

-----------------------------------
# Samsung Galaxy S3's Data            <--
-----------------------------------
Samsung Galaxy S3 (Under load)
Benchmark: Icestorm Unlimited
Stats: Cortex A9 V2 Cores: 1400MHz|GPU: 533MHz
Total Score: 3,679 
GPU SCORE: 3,181
GPU Test 1: 10,2FPS
GPU Test 2: 21,6FPS
CPU SCORE: 8,128
CPU Test: 25,8FPS
-----------------------------------------------
Samsung Galaxy S3 (Full Power, Overclocked):
Benchmark: Icestorm Unlimited
Stats: Cortex A9 V2: 1704MHz|GPU: 700MHz
Total Score: 4,515
GPU SCORE: 3,909
GPU Test 1: 13,00FPS
GPU Test 2: 24,6FPS
CPU SCORE: 9,879
CPU Test: 30,4FPS
-----------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 1400MHz|GPU: 533MHz
Single Core: 509 (Though I have recoded up to 510)
Multi Core: 1348 (Though I have recorded up to 1370)

Single Core Stats:
Crypto: 23
Integer: 618
Floating Point: 285
Memory: 720

Multi Core Stats:
Crypto: 92
Integer: 1979
Floating Point: 1010
Memory: 751

-1704MHz Run
Single Core: 588 (Though I recorded up to 600)
Multi Core: 1537 (Though I recorded up to 1594)

Single Core Stats:
Crypto: 28
Integer: 745
Floating Point: 338
Memory: 750

Multi Core Stats:
Crypto: 112
Integer: 2301
Floating Point: 1151
Memory: 763
------------------------------------------------


------------------------------------------------
# Asus Vivobook 2013's Data                        <--
------------------------------------------------
(Rainmeter, CoreTemp, Hwinfo)
Benchmark: Icestorm Unlimited
Stats: i7 4500U: 2394MHz|GPU: 1053MHz
Total Score: 61,292
GPU SCORE: 91,390
GPU Test 1: 453,32FPS
GPU Test 2: 353,68FPS
CPU SCORE: 28,473
CPU Test: 90,39FPS
-------------------------------------------------
(Full Power, Maybe CPU BOTTLENECKED)
Benchmark: Icestorm Unlimited
Stats: i7 4500U: 2694MHz|GPU: 1189MHz
Total Score: 73,284
GPU SCORE: 111,515
GPU Test 1: 560,75FPS
GPU Test 2: 427,05FPS
CPU SCORE: 33,313
CPU Test: 105,76FPS
-------------------------------------------------------------
Benchmark: Wildlife Unlimited
Stats: GPU: 1189MHz
Score: 2,791
FPS: 16,72FPS
-------------------------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 2694MHz|GPU: 1189MHz
Single Core: 3,580
Multi Core: 6,340

Single Core Stats:
Crypto: 3216
Integer: 3634
Floating Point: 3189
Memory: 4137

Multi Core Stats:
Crypto: 6031
Integer: 7198
Floating Point: 6393
Memory: 4409
------------------------------------------------------------
Benchmark: Cloud Gate
Stats: CPU: 2394MHz|GPU: 1053MHz
Total Score: 4,947
GPU SCORE: 7,112
GPU Test 1: 28,91FPS
GPU Test 2: 33,24FPS
CPU SCORE: 2,396
CPU Test: 7,61FPS
------------------------------------------------------------
Benchmark: Cloud Gate
Stats: CPU: 2694MHz|GPU: 1189MHz
Total Score: 5,895
GPU SCORE: 8,904
GPU Test 1: 36,27FPS
GPU Test 2: 41,51FPS
CPU SCORE: 2,701
CPU Test: 8,58FPS

------------------------------------------------------------
# Asus ROG Strix G15's Data                                    <--
------------------------------------------------------------
Asus ROG Strix G15 (Same load as previous PC)
Benchmark: Icestorm Unlimited
Stats: R9 5900HX: 3249MHz|GPU: 1702MHz
Total Score: 171,370
GPU SCORE: 341,644 (CPU BOTTLENECKED)
GPU Test 1: 1298,30FPS (CPU BOTTLENECKED)
GPU Test 2: 1735,54FPS
CPU SCORE: 62,444
CPU Test: 198,24FPS
-----------------------------------------------------------
Asus ROG Strix G15 (Full Power, CPU BOTTLENECK):
Benchmark: Icestorm Unlimited
Stats: R9 4900HX: 4600MHz|GPU: 2100MHz (CPU BOTTLENECKED)
Total Score: 237,209
GPU SCORE: 494,117
GPU Test 1: 1948,96FPS
GPU Test 2: 2393,16FPS
CPU SCORE: 84,124
CPU Test: 267,06FPS
------------------------------------------------------------
Asus ROG Strix G15 (Full Power):
Benchmark: Wildlife Unlimited
Stats: GPU: 2100MHz
Score: 58,610
FPS: 350,96FPS
------------------------------------------------------------
Asus ROG Strix G15 (Full Power):
Benchmark: Wildlife Extreme Unlimited
Stats: GPU: 2100MHz
Score: 18,915
FPS: 113,27FPS
------------------------------------------------------------
Benchmark: Cloud Gate
Stats: CPU: 3249MHz|GPU: 1702MHz
Total Score: 44,592
GPU SCORE: 115,735 (CPU BOTTLENECKED)
GPU Test 1: 482,61FPS
GPU Test 2: 525,63FPS
CPU SCORE: 14,150
CPU Test: 44,92FPS
-------------------------------------------------------------
Benchmark: Cloud Gate:
Stats: CPU: 4600MHz|GPU: 2100MHz
-Aborted. CPU Refuses to scale above 3250MHz, impacting the score.
Score is similar to previous benchmark, therefore it's pointless to list.
-------------------------------------------------------------
Benchmark: Geekbench 4
Stats: CPU: 3250MHz|GPU: 1702MHz
Single Core: 4,688
Multi Core: 28,847

Single Core Stats: 
Crypto: 5,609
Integer: 4,518
Floating Point: 4,626
Memory: 4,935

Multi Core Stats:
Crypto: 13,999
Integer: 35,964
Floating Point: 36,064
Memory: 5,719

-4600MHz Run:
Single Core: 6,298 (Though I have recorded up to 6,374)
Multi Core: 34,737

Single Core Stats:
Crypto: 7,786
Integer: 6,325
Floating Point: 6,624
Memory: 5,379

Multi Core Stats:
Crypto: 13,996
Integer: 45,221
Floating Point: 41,701
Memory: 5,888

------------------------------------------------------------
# iPad Pro 2020 11''s Data                                    <--
------------------------------------------------------------
iPad Pro 2020 11' (No load, power saving, CPU performance Anomalous on iOS Devices) 
Benchmark: Icestorm Unlimited
Stats: CPU: 1704MHz|Little Cores: Unknown|GPU: Unknown
Total Score: 62,765
GPU SCORE: 153,030
GPU Test 1: 813,95FPS
GPU Test 2: 562,63FPS
CPU SCORE: 20,482
CPU Test: 65,02FPS
------------------------------------------------------------
iPad Pro 2020 11' (CPU Might Perform Anomalously, CPU BOTTLENECK):
Benchmark: Icestorm Unlimited
Stats: CPU: 2496MHz|GPU: Unknown
Total Score: 105,046
GPU SCORE: 194,955
GPU Test 1: 1160,22FPS
GPU Test 2: 667,73FPS
CPU SCORE: 40,184
CPU Test: 127,57FPS
------------------------------------------------------------
iPad Pro 2020 11' (Full Power):
Benchmark: Wildlife Unlimited
Score: 13,455
FPS: 80,5FPS
------------------------------------------------------------
iPad Pro 2020 (Full Power):
Benchmark: Wildlife Extreme Unlimited
Score: 3,357
FPS: 20,1FPS
Notes: This device scores higher in the normal Wildlife Extreme (Around 3550)
------------------------------------------------------------
Benchmark: Slingshot Unlimited (CPU Performance Anomalous on iOS Devices. Figures may be unreliable for back to back comparisons.)
Total Score: 7,256
GPU SCORE: 26,950 (Some have seen up to 30,000+)
GPU Test 1: 147,61FPS (But I have recorded up to 177,68FPS)
GPU Test 2: 115,69FPS
CPU SCORE: 2,039
CPU Test 1: 11,63FPS
CPU Test 2: 18,28FPS
CPU Test 3: 14,66FPS
------------------------------------------------------------
Benchmark: Slingshot Extreme Unlimited (Same as Above):
Total Score: 6,226
GPU SCORE: 18,538 (Some have seen above 18,600)
GPU Test 1: 108,86FPS (Some have seen above 110FPS)
GPU Test 2: 63,99FPS
CPU SCORE: 1872
CPU Test 1: 8,39FPS
CPU Test 2: 16,46FPS
CPU Test 3: 13,78FPS
--------------------------------------------------------------
Benchmark: Miscellaneous GFXBench
1080p Texturing Offscreen: 49683 MTexels/s
1080p Driver Overhead 2 Offscreen: 251FPS (15.083 Frames)
1080p ALU 2 Offscreen: 332FPS (19.910 Frames)
1080p T-Rex Offscreen: 509FPS (28.506 Frames)
1080p Manhattan 3.0 Offscreen: 304FPS (18.865 Frames)
1080p Manhattan 3.1 Offscreen: 211FPS (13.115 Frames)
1440p Manhattan 3.1.1 Offscreen: 115FPS (7163 Frames)
1080p Car Chase Offscreen: 128FPS (7590 Frames)
1080p Aztec Ruins Normal Tier Offscreen: 160FPS (10.299 Frames)
1440p Aztec Ruins High Tier Offscreen: 57FP (3707 Frames)
4K Aztec Ruins High Tier Offscreen: TBD
------------------------------------------------------------
# Realme GT Neo 2's Data                                       <--
------------------------------------------------------------
(Full Power, Maybe CPU BOTTLENECKED)
Benchmark: Icestorm Unlimited
Stats: Prime: 3187MHz|Big: 2419MHz|Little: 1804MHz|GPU: 670MHz
Total Score: 92,586
GPU SCORE: 153,822
GPU Test 1: 779,2FPS
GPU Test 2: 585,8FPS
CPU SCORE: 38,685
CPU Test: 122,8FPS
-----------------------------------------------------------
Benchmark: Wildlife Unlimited
Stats: GPU: 670MHz
Score: 4,237
FPS: 25,4FPS
----------------------------------------------------------
Benchmark: Wildlife Extreme Unlimited
Stats: GPU: 670MHz
Score: 1,203
FPS: 7,2FPS
----------------------------------------------------------
Benchmark: Slingshot Extreme Unlimited OpenGL ES 3.1
Total Score: 8,330
GPU SCORE: 10,416
GPU Test 1: 64,4FPS
GPU Test 2: 34,9FPS
CPU SCORE: 4,898
CPU Test 1: 87,1FPS
CPU Test 2: 52,3FPS
CPU Test 3: 27,0FPS
----------------------------------------------------------
Benchmark: Slingshot Unlimited OpenGL ES 3.0
Total Score: 9,919
GPU SCORE: 14,090
GPU Test 1: 80,6FPS
GPU Test 2: 49,4FPS
CPU SCORE: 4,872
CPU Test 1: 89,0FPS
CPU Test 2: 51,6FPS
CPU Test 3: 26,8FPS
-----------------------------------------------------------




----------------------------------------------------------
# Desktop PC as of 24/01/2023's Data                 <--
----------------------------------------------------------
Desktop PC (Full Power, CPU BOTTLENECK):
Benchmark: Icestorm Unlimited
Stats: i5 12600K (Stock)|GPU: 2100MHz
Total Score: 282,878
GPU SCORE: 607,547
GPU Test 1: 2700,96FPS
GPU Test 2: 2584,62FPS
CPU SCORE: 98,551
CPU Test: 312,86FPS
----------------------------------------------------------
Desktop PC (Full Power):
Benchmark: Wildlife Unlimited
Stats: GPU: 2100MHz
Score: 72,458
FPS: 433,88FPS
----------------------------------------------------------
Desktop PC (Full Power):
Benchmark: Wildlife Extreme Unlimited
Stats: GPU: 2100MHz
Score: 22,054
FPS: 132,06FPS
--------------------------------------------------------------------
DATA LOG END-
