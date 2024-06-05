# Godot4-OpenAnimationLibraries
Make reusable Mixamo animations libraries that can retarget other models in Godot 4

![Controller Screenshot](https://github.com/pemguin005/Godot4-MixamoLibraries/blob/main/Screenshots/MixamoLib.GIF)

## UPDATE
Adobe's terms of service 6.2.E state not to make datasets or databases from their content so libraries of their animations cannott be shared here. 
To respect their service, all Mixamo animation libraries have been removed. I'm leaving only the Mixamo Godot Bone Map.tres, but you can still make your own Mixamo libraries!

This project is now for creating open animation libraries that DO NOT USE Mixamo and can be used freely. The open libraries should be mixamo Skeleton compatible. So you can still rig your characters with Mixamo if you prefer, just be sure to reimport with a/the Mixamo bone map in Godot.

## Features

A handful of different animation libraries for a variety of scenarios and body types.




## Requirements
- Godot 4 stable
- A model with a semi-standard skeleton (Adobe's Mixamo tool can give you a game-ready skeleton, as well as a variety of blender plugins. I maintain a repository for a Blender plug-in called Rigidoify which will also give you game ready. humanoid, canid, equid, and felid skeletons based off the rigify control rig: https://github.com/catprisbrey/Rigodotify)
- The skeleton in Godot mapped to for your character.


# Tutorial

A quick demonstration followed by a more indepth tutorial on how to use these libraries.

https://youtu.be/cetPEHgmATA

## Concept

Building sharable libaries to use across all your Godot characters, to mix and match as needed.

Godot can retarget skeletons. So any skeleton, if mapped properly, (i recommend standard T poses, and standard game rig skeletons), can inherit animations from other models or even load entire library sets of animations that can be mixed and matched.


# How to use Library files once you have them:

- Drop into Godot's filesystem any Mixamo rigged model, or game dev skeleton rigged model (in the base Tpose for best results)
- Double click the model to open the Re-import menu
- Select the skeleton, and select the bone map drop down, and select the Mixamo bone map, or map your own bones manually if using a different skeleton.
- Drop you character model into scene
- Select their animation player, click Animation > Manage Animations > Load Library > and select a library.res

It's now mapped to the new character! If you had a proper skeleton compa that was properly mapped at import, then all the animations should work properly.

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
- Drop the .glb into the scene, transfom 0,0,0 as needed.
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

Support me by checking out my dev projects here or on https://catprisbrey.itch.io/character-idea-generator or my music at https://bonesinthewalls.bandcamp.com, https://open.spotify.com/artist/3eKiNBKa9Jel0Ev98hcZll?si=dX0koLvrSWarOkSMaEmbmg, or searching "Bones in the Walls" where ever you stream music.
