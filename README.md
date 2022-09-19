# Godot4-MixamoLibraries
Make reusable Mixamo animations libraries that can retarget other models in Godot 4

![Controller Screenshot](https://github.com/pemguin005/Godot4-MixamoLibraries/blob/main/Screenshots/MixamoLib.GIF)

## UPDATE
Adobe's terms of service 6.2.E state not to make datasets or databases from their content so libraries of their animations cannott be shared here. 
To respect their service, all Mixamo animation libraries have been removed. I'm leaving only the Mixamo Godot Bone Map.tres, but you can still make your own Mixamo libraries!

This project is now for creating open animation libraries that DO NOT USE Mixamo and can be used freely. The open libraries should be mixamo Skeleton compatible. So you can still rig your characters with Mixamo if you prefer, just be sure to reimport with the Mixamo bone map.

## Features

- Mixamo bone map.tres file, that makes Godot ready Mixamo rigs/animation libraries an option.
- OpenBot CC0 model files - for making open humaniod animations (OpenBot is Mixamo animation compatible)
- OpenDog CC0 model files - for making open canine animations
- Free/Open Godot animation libraries for humanoids and dog 

## Requirements
- Godot 4.0.13 Alpha or newer
- BoneMap.res file (for either the OpenBots or Mixamo)
- A model rigged with either a Mixamo, OpenBot, or OpenDog skeleton

# Tutorial

A quick demonstration followed by a more indepth tutorial on how to use these libraries.

https://youtu.be/cetPEHgmATA

## Concept

Godot can retarget skeletons and animations. This means you can re-use animations, and animation libraries across models. To take advantage of this feature, always reimport your character skeleton with a bone map. This project provides a bone map for Mixamo rigged skeletons, as well as an open bone map and OpenBot model for animating. The OpenBot is cross-compatible with the Mixamo skeleton and animations-- but the Openbot is creative commons 0 license!  Any animations and libraries made on OpenBot is cross compaitble across all Mixamo models OpenBot mapped skeletons. Consider making aniatmions with the bot, turning them into libraries, and sharing them here so we all can benefit from an open library of open animations.


# How to use Library files once you have them:

- Drop into Godot's filesystem any Mixamo rigged model, or OpenBot rigged model (in the base Tpose for best results)
- Double click the model to open the Re-import menu
- Select the skeleton, and select the bone map drop down, and select the Mixamo or OpenBot bone map.
- Drop this character model into scene, right click it and select "Make local".
- Select their animation player, click Animation > Manage Animations > Load Library > and select a library.res

It's now mapped to the new character!

# How to create your own library files with Mixamo characters:

## 1.A Steps on Mixamo
- Download the Ybot model, import into blender
- Use the YBot in Mixamo to download all the animations you want
- Use the default fbx for downlaods, "Without skin", and select 'in place' when possible.

## 2. Steps in Blender
- Import base Mixamo YBOT, or OpenBot
- Import each animation fbx (in another collection for easy visiblity, and easy removal later).
- In the Animation tab, change the view to the "Nonlinear animation player"
- Name the first animation, and click push down to add it to the base Ybot.

- In the Nonlinear animation player, hit the 'N' key, a menu will appear on the right.
- Click the small drop down to select an animation from another armature
- Press Space bar to play the animatinon, name its animation, click push down.
- Repeat until all armatures animations are named and pushed to the base armature.
- Delete all other animatinon armatures.
- Save, check scale, export as glb. placeholder materials to save space.

## 3. Steps in Godot
- Bring .GLB into Godot filesystem
- Re-import, click "Skeleton3d", bone map drop down, load mixamo bone map.res.
- Drop the .glb into the scene, transfom 0,0,0,
- Right click > Make Local, Save as scene.
- Go to animation player, (test if you want that it works).
- Click Animation > Manage Animations
- To the right of Global, click the save icon, save the library.

DONE library now exists and it can be used on any skeleton that's been mapped in Godot

![Controller Screenshot](https://github.com/pemguin005/Godot4-MixamoLibraries/blob/main/Screenshots/Screenshot.jpg)

## Background

Explanation and inspiration  originally from FinePointCGI. Additional info can be found in their video about troubleshooting skelelon remapping. This project was inspired entirely by this video.
https://www.youtube.com/watch?v=NBukd3NmK88

## Support

Support me by checking out my music at https://bonesinthewalls.bandcamp.com, https://open.spotify.com/artist/3eKiNBKa9Jel0Ev98hcZll?si=dX0koLvrSWarOkSMaEmbmg, or searching "Bones in the Walls" where ever you stream music.
