# Python-textured-sphere-no-geometry

Software textured sphere renderer, quick ported from C++ code. IT WORKS, but it's slow and not optimized. Sphere is drawn with pixels, no geometry needed. 

I spent many hours searching for Python code to meet this need for a project but could not find anything suitable using only pixels. All examples I've found involve sphere geometry.

Originally adapted from code posted by Plucky on allegro.cc 05/22/2002:
https://www.allegro.cc/forums/thread/186206/186206#target


Original code packed 5,6,5 into an 8-bit short int: 
"TEX_SIZE must be <= 256 due to coord_transform_table holding shorts. In this code, it needs to be a power of 2, but a couple of minor tweaks, and this constraint can go away."

This RGB packing can be removed from the Python code and better optimized. It's just sort of ignored for now which is inefficient. TEX_SIZE should be passable but code must be cleaned up first.

There's a problem with the textures not lining up at the wrap point. This is due to sloppy float-int truncation that needs attention. It did not do this in the C++ code. But in the interest of making this code more useful, the integer packing should not be used.

Contributions requested! It would be fun to see what the community can do to improve this code. I will be the first to admit this Python code needs work.

![TexturedSphere](https://github.com/Aeneas137/Python-textured-sphere-no-geometry/assets/46901366/732474b3-d29b-4f68-8635-83b233e8b266)

test 1
