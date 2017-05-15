# 3D Printing <br><small>A 5 step tips and tricks guide to using 3D printing in Architectural Practice</small>

Chris Bickerton • January 2017

![A section of a project 3d printed]({{site.baseurl}}/assets/3d-print/mel-tower.jpg)

# Introduction

As 3D printers become more common in AEC practice, we thought it would be useful to put together this tips and tricks guide to help out those within our industry who have access to a printer, but need a bit of help understanding the steps required to complete a print.

BVN has been using 3D printing to help communicate our projects since 2013, and after 4 years we are seeing a huge uptake of the technology across a wide variety of project types and stages.  We are currently working towards the goal of having the capability to produce 3D printed models in every one of our project teams.

This document is a brief summary of the advice I give day to day, and I am hoping it will be a useful resource to all those who at the beginning of their 3D printing journeys.  Not knowing what printer you are trying to use, I have kept the advice generic enough to help point you in the right direction, but at times I will refer directly to the printers that are in BVN’s fleet.

# 1. Get to know the machine that you will be using.

There are many, many different types of 3D printers around these days, each slightly different so you need to get familiar with the one at hand.

At the time of publishing here at BVN we have 3 types of FFF (Fused Filament Fabrication) printers – The Makerbot 2x, Ultimaker 2 Extended + and the Ultimaker 3 Extended.  

To get started you probably are going to have to do a bit of research or asking around. These questions probably will get you 90% of the way there:

## What resources do I have access to?  Are there any good ‘how to’ tutorials available?

Don’t underestimate the wealth of knowledge available online.  There are really good tutorials out there.  I have the Ultimaker App on my phone which I refer to constantly. There are also really good community based forums online – typically if you have a question, someone else has had the same question before you and found the answer!

## Do I need an induction?  Make a booking?

Here at BVN we try to run frequent induction sessions, to make sure we are all using the machines safely, and to give a good introduction to the basics.  If someone knows how to use the machine, you are better off learning from them!

As our printers are often running constantly, make sure that you have time booked for your model.

## What slicer software do I need to run the machine, and does it need to be installed on your computer?

A slicer is the program that is used to generate the file which the 3D printer uses to create your model.

For the Makerbot, we currently use Makerbot Desktop, and for our Ultimakers we use the latest version of Cura, but this is generally specific to the machine that you are using.

## What material(s) (and colour(s)) do I want to print with?  Does it need to be ordered in?  

There are many, many different materials available to print with on the market.  We typically use PLA based filament for its sustainability benefits, which come in a whole range of colours as well as composites such as timber-PLA and metal-PLA.  If you are doing a lot of printing, make sure that you order from the same supplier to ensure that colours match!  

Some machines are able to print with more than one filament at a time, so you might be able to choose multiple colours or print with dissolvable supports.  There are also printers out there that are able to print in full colour, if that is something that you would like to achieve.

## How big a model can I print?

The build volume of the machine will determine the maximum size of a part, you will need to fit your design within this volume.  For larger models you may need to split it up into smaller pieces.  This varies from machine to machine.

BVN’s Makerbot 2x has a build volume of 246mm length x 152mm width x 155mm height.

BVN’s Ultimakers have a build volume of  233mm length x 233mm width x 305mm height.

# 2. Creating a 3D printable model.

There are many was of creating a model ready to print, depending on which program you are working in, each much to specific to go into in this guide.  So here are some easy to remember rules of thumb:

# What scale do I want to model at, and how long will it take to print?

This is really important to consider early, especially if you intend to do an iterative series of models. Remember that the bigger the model is, the longer it will take to print.  A model at 1:100 will take about 4 times as long as the same model at 1:200.  Ask yourself, is the time required to print this going to become a barrier to your designing?

As a rule of thumb, I tend to use a scale 1 step smaller than if I were modelling by hand.  So if I would build a 1:500 model by hand, it is probably OK to print it at 1:1000.  The printer will generally be able to handle the detail at the smaller scale, and in my opinion a larger 3D printed model can run the risk of looking a bit unresolved.  

If asked to give a quick estimate of time when beginning it will take to print a model I usually estimate about 8-10 hours a piece.  This of course varies wildly depending on the machine and what you want to print (I have seen print times ranging from 20 minutes to 100 hours), but at the time of publishing 8-10 hours seems to be a good goal, as it allows you to put on one print in the morning, and one as you leave to go home.

## Is the model able to be printed?

Typically you want to ensure that the model you are creating is watertight (no holes or surfaces with no thickness), with all elements at a suitable thickness for printing (as a rule of thumb I suggest you start with 1-2mm, and then get thinner as you get more experienced).

As you would expect, the better your drafting is, the better the quality of the resulting print.

## What file do I need to output?

Our printers can take .stl and .obj files.  Check what files your slicer software can use, and work out how to export this file type from your modelling software.  You may need to investigate plugins, but a quick google search or a question to a colleague will usually give you an idea what you need to do.

# 3. Prepare your file in your slicer software.

This process differs between different softwares, but here are some tips:

## Optimise your model for speed

Time is usually the biggest constraint when 3d printing, so we want to make sure we optimise our file set up to speed things up!

Most slicer software comes with default ‘simple’ settings which will work perfectly fine for producing a model, however there are usually massive time savings if you delve into the more advanced settings.  

Typically a ‘low res’ model is perfectly acceptable for an architectural model and will usually go unnoticed, so I generally advise to print at a lower quality setting than is typically standard.

At a minimum, you will want to understand how nozzle type, layer height, wall thickness and infill density affect the time required to print.

## Check if you need supports

If you are using a FFF (Fused Filament Fabrication) machine (Like a Makerbot or Ultimaker) the majority of overhangs will need to be supported by automatically generated supports, to avoid the model slumping.  These supports can be torn away after your print has completed.

If you don’t want to use supports, you can also look into printing your model on its side or upside down to avoid overhangs.

# 4. Print your model

This process will also differ machine to machine, but here are a few things to be aware of to ensure your print does fail.

## Make sure your print will stick to the build plate

The majority of prints fail because they don’t stick correctly to the build plate. A bit of care is recommended when setting up to ensure this doesn’t happen

Firstly, ensure that the machine, especially the build plate it properly calibrated.  There are typically instructions in your printers documentation on how to do this.  Take the time to go through these step by step if you are having issues.

A very thin layer of glue from a glue-stick will also help PLA prints stick.  Only a very fine layer is needed, and If there is accumulated glue on the glass plate give it a quick wash in warm water and start fresh.

If you are printing in ABS, a small amount of filament dissolved in Acetone and brushed onto the plate will help your print stay put.

## Make sure you have enough material (properly) loaded.

Kind of obvious, but this happens surprisingly often.  Make sure that there is enough material loaded to complete the print.  Also check for tangles, as these will cause your print to fail.

# Remove your print with care

Prints can often be very rigidly stuck to the build plate, so be careful when removing them.  If you are having difficulty, you can always soak everything in warm water for 15 minutes or so, this should make it easier to remove.

Try and minimise the amount of glue you use, as this will make your print easier to remove!

# 5. Share your work and teach others!

Every print you do is a little bit of design research, make sure you share what you learn with others so everyone can be involved in the fun.  We all come across different problems and opportunities while we work, so it is really important to share what you learn!  I find a carefully photographed model to be a very powerful resource to share.

3D printing is quickly become standard practice in Architecture firms, so do your part for your practice and industry by helping others to use this awesome technology!  
