---
title: Getting Started With Tiva C Series MCU
author: Vikas Gaikwad
date: 2016-04-25 20:55:00 +0800
categories: [Blogging, Tutorial]
tags: [getting started]
pin: false
comments: true
---

Hey I just got this a very powerful Texas Instruments <strong>Tiva C Series TM4C123G</strong> <strong>ARM-Cortex M4F</strong> launchpad to work around RTOS(Real Time Operating Systems). I thought lets gets introduced with this powerful 32-bit ARM Cortex M4F based device having very good online and offline <span style="color:#33cccc;"><a style="color:#33cccc;" href="http://www.ti.com/tool/ek-tm4c123gxl#supportandcommunity">community support</a> </span>for beginner and professional developers  from TI.

I am very much interested to soon get you on the tour of RTOS supported by this MCU, but before getting it more complex lets start from the basic introduction of MCU board, Tools required for programming, list of supported RTOS and many more on the bucket, I will get it one by one for you.

Here we will gets familiar with Tiva C Series Launchpad, and its hardware features , pinouts and software tools ....

<strong><span style="color:#ff9900;">Introduction to Tiva C Series</span> <span style="color:#33cccc;"><a style="color:#33cccc;" href="http://www.ti.com/lit/ds/spms376e/spms376e.pdf">TM4C123G ARM</a></span>-Cortex-<span style="color:#33cccc;"><a style="color:#33cccc;" href="https://en.wikipedia.org/wiki/ARM_Cortex-M">M4F</a> </span>:</strong>

Lets us understand about ARM-Cortex-M4 Core first , Here The <b>ARM Cortex-M</b> is a group of <a title="32-bit" href="https://en.wikipedia.org/wiki/32-bit">32-bit</a> <a class="mw-redirect" title="Reduced instruction set computer" href="https://en.wikipedia.org/wiki/Reduced_instruction_set_computer">RISC</a> <a title="ARM architecture" href="https://en.wikipedia.org/wiki/ARM_architecture">ARM</a> processor cores licensed by <a title="ARM Holdings" href="https://en.wikipedia.org/wiki/ARM_Holdings">ARM Holdings</a>. The cores are intended for <a title="Microcontroller" href="https://en.wikipedia.org/wiki/Microcontroller">microcontroller</a> use, and consist of the Cortex-M0, M0+, M1, M3, M4, and M7 cores.

Cortex-M4 processor Core is very commonly used in industries for various applications as below beacause of ...
<ul>
	<li>The ARM<sup>®</sup> Cortex<sup>®</sup>-M4 processor is ARM’s high performance embedded processor developed to address digital signal control markets that demand an efficient, easy-to-use blend of control and signal processing capabilities.</li>
</ul>
 
<ul>
	<li>The combination of high-efficiency signal processing functionality with the low-power, low cost and ease-of-use benefits of the Cortex-M family of processors is designed to satisfy the emerging category of flexible solutions.</li>
</ul>
 
<ul>
	<li>Specially prefers this core for applications like this :The motor control, automotive, power management, embedded audio and industrial automation, and mainly used in Home Automation and Building Automation.</li>
</ul>
Well there is lot more to talk on this , you guys also can explore about Cortex-M4 core.

We will now focus on some thing practical things , I mean about Tiva C Series Launchpad and lets understand more about its specifications and pin-outs and some other use cases.

<!--[caption id="attachment_366" align="aligncenter" width="546"] -->
<img class="  wp-image-366 aligncenter" src="https://vksgaikwad3.files.wordpress.com/2016/04/img_20160423_192847335.jpg?w=612" alt="IMG_20160423_192847335" width="546" height="307" /> 
##### Tiva C Series ARM Cortex-M4F Launchpad

The picture shown above is the Tiva C series Launchpad , we will look at its specifications
<div class="row ten-column no-margin">
<div class="c3 push2">
<h3>Specs :</h3>
<h4>Part Number</h4>
</div>
</div>
<div class="row ten-column no-margin">
<div class="c3 push2">

<a href="http://www.ti.com/tool/ek-tm4c123gxl">EK-TM4C123GXL</a>

<strong>Microcontroller Features</strong>
<ul>
	<li>80MHz</li>
	<li>256KB Flash</li>
	<li>32KB RAM</li>
	<li>2-KB EEPROM</li>
	<li>On-chip ROM with drivers and boot loaders</li>
	<li>2x 12ch 12-bit ADCs (1 MSPS)</li>
	<li>16x Motion PWM channels</li>
	<li>24x Timer/Capture/Compare/PWMs</li>
	<li>3x Analog comparators</li>
	<li>4x SPI/SSI, 4x I2C, 8x UART</li>
	<li>USB Host/Device/OTG</li>
	<li>2x CAN</li>
	<li>Low-power hibernation mode</li>
	<li>43x GPIO pins</li>
</ul>
<h4></h4>
</div>
<div class="c3 push2">
<h4></h4>
<h4>Supported Family</h4>
<a href="http://www.ti.com/tiva-c">Tiva C Series TM4C123x MCU</a>
<h4>Featured Microcontroller</h4>
<a href="http://www.ti.com/product/tm4c123gh6pm">TM4C123GH6PM</a>
<h4>Why this LaunchPad?</h4>
<p style="padding-left:30px;">Features a Tiva C Series microcontroller ideal for any system or design that requires the three Cs: <span style="color:#33cccc;">connect, communicate, control</span></p>

<h4 style="padding-left:30px;"></h4>
</div>
</div>
<strong>On-board Emulation:</strong>The EK-TM4C123GXL LaunchPad features on-board emulation, which means you can program and debug your projects without the need for additional tools.

 
<h2>What's Included?</h2>
The Tiva C Series LaunchPad includes everything you need to get started with ARM Cortex-M4 development!
<ul>
	<li>Tiva C Series TM4C LaunchPad Evaluation Board (EK-TM4C123GXL)</li>
	<li>On-board In-Circuit Debug Interface (ICDI)</li>
	<li>USB Micro-B plug to USB-A plug cable</li>
	<li>README First document</li>
	<li>Free EK-TM4C123GXL TivaWare for C Series software downloads.</li>
</ul>
<h4>Switches, LEDs & Jumper:</h4>
Two general-purpose user switches, a reset switch, power LED, and user-programmable RGB LED are provided on board to ease development. A jumper is also included to allow current measurements, as well.
<h2>Board GPIO Mapping:</h2>
Lets understand the mapping of GPIOs of MCU on this launchpad. Most of the pins on this board are highly multiplexed as shown in picture below.

<!-- [caption id="attachment_377" align="aligncenter" width="621"] -->
<img class="  wp-image-377 aligncenter" src="https://vksgaikwad3.files.wordpress.com/2016/04/tiva_c_launchpad_pinout_001b.jpg" alt="tiva_c_launchpad_pinout_001b" width="621" height="465" /> 

<center>Pin Mapping</center>

 

Tiva  C Series and many other boards like MSP430 and other boards of Texas Instruments have <a href="http://www.arduino.cc/">Arduino</a> like programming support, which really helps to make the fast prototyping and developing any applications very quickly.
<h2>Programming ARM Like Arduino:</h2>
<a href="http://energia.nu/">Energia</a> is the tool  which allows the users to make this happens. wow...

<a href="http://energia.nu/">Energia</a>  is  an <a href="https://github.com/energia/energia" target="_blank">open-source</a> electronics prototyping platform started by <strong>Robert Wessels</strong> in January of 2012 with the goal to bring the Wiring and Arduino framework to the Texas Instruments MSP430 based LaunchPad, now it has very god support for other Texas MCUs also.
<h2>Software Programming Tools:</h2>
<ol>
	<li><a href="http://energia.nu/">Energia</a>(Open Source IDE)</li>
	<li><a href="http://www.ti.com/tool/ccstudio">CCS</a>(Code Composer Studio) : Use for complex projects,developments, RTOS, mainly Industrial use.</li>
	<li><a href="http://www.ti.com/ww/en/launchpad/software.html#tabs">CCS Cloud</a> programming.</li>
	<li><a href="https://www.iar.com/">IAR Embedded Workbench</a></li>
	<li><a href="http://www.keil.com/">Keil</a>-ARM</li>
	<li><a href="https://temboo.com/hardware/ti">TeMBOO</a> - IoT applications.</li>
	<li><a href="https://gcc.gnu.org/">GCC ARM Complier</a></li>
</ol>
 

Well guys this tutorial was just an introductory tutorial  for giving you introductions about hardware and software tools for programming .

We will soon going to live for creating our first Tiva C Series TM4C123G ARM-Cortex-M4F projects and also we are going to create an <strong>TI-RTOS(SYS/BIOS)</strong> based projects in CCS6.1.

Guys stay tune with me to explore on programming and developing interesting application with ARM-Cortex systems.

 

Cheeerrrrrr..............

 

 


<h4></h4>
 