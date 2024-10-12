---
title: How to add support for Excalidraw Rendering in Quartz
---

All credits to bartkl for making the plugin. What an awesome piece of code!

I am not super knowledgeable about all of this, so all I did was clone bartkl's quartz repository and copied all instances of `RenderExcalidraw` to their corresponding locations in my Quartz set-up. A little crude, but does the job just fine.

![[Screenshot 2024-10-12 at 11.26.05 AM.png|Screenshot showing all instances of RenderExcalidraw in bartkl's code]]

For `index.ts` and `quartz.layout.ts`,  you copy the pieces of code into their appropriate lines. For `RenderExcalidraw.ts`, simply copy the whole file into `/quartz/components`.

I noticed that the Excalidraw files were put in the attachments folder. I believe the code turns them into .svg files for display on the website. A nice little feature I've noticed is how it actually turns the file into two .svg files -- one for dark mode, and one for light.

This won't give you the ability to directly open Excalidraw files on the website, but rather as an attachment within your .md file -- this is to be assumed by default.