# Godot4-OpenAnimationLibraries 

Ready-to-use animation libraries and bone maps for the Godot 4.x Game Engine

[Watch my video](https://youtu.be/zCvCHO6sk3Y?si=qJ8ILE4eWoNjmLqr) here for more information and a bit of walkthrough. I have many videos on this topic.


## Prerequisites

In order to use these you need a 3D model with the following:
- A standard game dev skeleton
- One animation applied (t-pose is fine)
- Godot 4.x
- Patience to double check your work!


## Setup and Usage

### 1. Import Your Model

1. Prepare your model by giving it a standard skeleton, and adding one animation to it (a tpose works perfectly here). 
2. Import your model into Godot, and open the advanced import menu for it.
3. Select the Skeleton, and click the drop down to add a new bone map.
4. Select the Profile dropdown, and add a new Humanoid Profile

### 2. Bone Map Properly

The bone map must show green dots for every bone. Each bone must be the correct bone or this whole process will fail. DO NOT ASSUME it's mapped prpoerly because you see green dots. 
#
1. Click each bone, and confirm the bone Godot requests, matches the appropriate bone on your own skeleton.
2. In the 'Groups' drop down, confirm the face, and hands are correct as well.
3. Click 'Reimport' when your done to apply those changes.
#
 The bone map must show green dots for every bone. Each bone must be the correct bone or this whole process will fail. DO NOT ASSUME it's mapped prpoerly because you see green dots. 

### 3. Add an Animation Library to Your Model
1. Open your model in Godot (either as it's own saved scene, added into another scene with 'make local' or expanded with 'editable children. We just need to access it's child nodes.)
2. Select its AnimationPlayer (if it doesn't have one, see section 1, step 1.)
3. Click the button "Animation", and "Manage Animations". (If you want to make your own library file, and not just add to this one, skip now to section 4)
4. Click the button "Add Library", and select one of the library files from this repo, or one you have made.
5. Enjoy all the animations! You're done!

### 4. Making your own Library files
If you're own model has animations you'd like to pass to other models, complete sections 1-3:3

1. Go to the in the "Animation", "Manage Animations" menu.
2. Double click the animation collection and give it a name (defaults to "Global" but name it something more discernible to tell your library files part later on)
3. To the right of the collection, click the Save Icon.
4. Select, "Make Unique" then click the icon again and select "Save As"
5. Save your library file, and consider donating/sharing the animations to this project!

Now for any models with a standard skeleton you can follow sections 1-3 to give them that library file.

## FAQ

#### What is a "standard game dev skeleton?"

A hierarchical bone structure, where the bones are properly all in a parent/child chain through the whole body. This makes IKs work properly in game engines, and is why Unity, Godot, Unreal, Mixamo, and many other softwares encourage you use a game dev skeleton. Blender's Rigify does NOT give you a game dev skeleton.

#### Where can I get a game dev skeleton?

- Mixamo can autorig your character with a game dev skeleton. It's a free and easy option for beginners.

- Rigodotify is a free tool I made that uses Blender's Rigify as a base, but ensures the skeleton is game ready.

- Make your own skeleton and rig in whatever software you like

- Use any other software that produces a hierarchical bone structure.


#### Only some of my body is animating correctly! Why?

- Your bone map is likely incorrectly mapped for either the source animations, or the new model trying to use them. Open the advanced import menu again in Godot, click the skeleton, open it's bone map, and ensure that each Godot bone is correctly matched with the bone your skeleton.


#### Root Motion is action weird! Why?
- Does your model have a root bone? some folks don't notice, and they bring in a model without a root bone, and try to use the hips for root motion. This can get really buggy and may not work as expected. If your model doesn't have a root bone, it's not hard to add one. Load youtube and search for how to add a root bone. (essentially parent your whole deform skeleton rig to a new bone named "root", and ensure "deform bone" is checked so it exports properly)

#### Your Mixamo bone map is faulty and didn't work for me, WHY??

- Some Mixamo models have slight differences, I can't plan for that, you can still use that bone map, but you'll need to double check where things went awry. Likely the root, or hips are incorrectly referencing the wrong bone.
