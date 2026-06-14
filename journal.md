## Journal 1

I started my first project for KEEB!

I have decided to make a Leopold 660m layout keyboard, a wireless keyboard with the Supermini nrF52840.
Now, I had to find some reference keyboards since I have not used the Supermini or made a wireless keyboard.
I found a great project on a 65% keyboard. It uses through hole components but that is not a big problem, since I know how the matrix and connections work. I only needed to refer to the battery connections and the GPIOs I can use.
This is the reference I found : https://github.com/RafaelCasamaximo/voidPointer
This is a really great project in my opinion and since it was already built, it was even more helpful.
All I had to do now was make the schematic, assign the footprints and start building!

I like minimal keyboards, so I have only the keys, the supermini and a sandwich mount case (or integrated plate) case.
The repo I was referring to also had a slider switch, which was pretty cool!
I added all the components, and placed them according to the reference.
I also had fewer switches compared to the reference, so I made some changes to the matrix.

While I do not have all the images of my schematic building process, I do have the full schematic ready. 
I am using Gateron hotswap sockets for this keyboard, along with SOD-123 diodes. All my footprints are from the marbastlib library(along with supermini)

[To Insert-schematic image]

I assigned footprints and now I have to place all the components.
For this, I used the grid from the guide,and the generated plate from the ai03 plate generator.

#### Time taken - around 2 hrs to make the schematic and place all switches.

## Journal 2

Today, I did the entire PCB layout!
This is my favourite part of the entire PCB design because it really gets me thinking because of constant changes to the layout and I get to crashout.

[To Insert-keyboard image 1]
I had already laid down the keys, so all I had to do was routing. I had also not laid out the diodes and added the stabilizers correctly. The Leopold does not have a very long right shift so, I had to change those, and also while updating the schematic, some of the footprints were changed only in the PCB editor, which caused it to change.
I fixed everything, then I decided that the top right of the PCB is the best placed for the supermini. It increases the height a bit, but yes, that is inevitable imo but it is also almost equivalent to the size of the Leopold 660m(with case but yes since this is custom, I have my say ;D )

This is how the keyboard looked after I placed the diodes.

[To Insert-keyboard image 2]
Now, routing is always a challenge with the matrix, as it can be optimised in such a way that there is no need for vias and it looks clean.
I had to change the pins many times while routing this.
I routed all the diodes first. I have my own way of routing diodes so that it passes with some gap with the holes.
Sure, the normal way is fine but there is always a risk.

[To Insert-keyboard image 3]
Here are some images of the PCB routing process-

[To insert - keyboard image 4]
This was the first routing layout I did. The GPIOs were unreachable and the traces were too far apart, increasing the width of the PCB.
I changed this.

I changed my pins a few more times and reached to this layout. All that was left were the ground connections and battery connections.
I added the battery connections.
[To insert - keyboard image 5]

I then added a ground plane on both sides to finish the PCB. I also made the edge.cuts to finalise the board edges.
This is how it looks.
[To insert - keyboard image 6]
DRC was run, and no errors occured!
I need to add some silkscreen, and add keycaps and switches to the PCB to move to CAD.

#### Time taken - around 2.5 hours to finish up the PCB routing, remaining layout etc. (I also changed many things in the schematic for the PCB, thus the long time.)

## Journal 3 

Now, I started by adding the keycaps. Since I have already done a PCB design, I had a easy way to add the switches and keycaps, by taking the x,y,z and angle values and noting them and directly plugging them in. This is also a fun but time taking part
This is how the first keycap looks-

[To insert - keycap 1]

KiCad crashed on me once today while adding the keycaps

Here is me adding the backspace keycap
[To insert - keycap 2]

This is some tiresome work, but here is the PCB after I added half of the keycaps
[To insert- keycaps half]

And the last keycap 
[To insert- space]

This is how the PCB looks 
[To insert- final pcb]

#### Time taken - 50 minutes to manually add and align all switches and keycap models.

## Journal 4

I started CAD today. I have decided for a sandwich mount case. I also will leave out the space for the devboard.

I imported the the .step of the PCB from KiCad to Fusion.

[To insert- imported PCB]

Then, I made a sketch to make the base.
The base was made to have 8mm thick walls on each side.

[To insert- sketch]

I then extruded only the base under the pcb. 

[To insert- Bottom base]

Then I made the walls and aligned it to the Top edges of the PCB

[To insert-base]
[To insert- base2]

I then imported the plate.dxf from ai03's plate generator 
[To insert - plate]

I then aligned the plate to the keycaps, extruded the sides to match the entire base length.

[To insert- Plate aligned]
[To insert - Plate extruded]

This was the case halfway done.
[To insert- Halway assembly]

I then made the top part of the sandwich from the same sketch I used for the walls.

[To insert-Top]

Finally, I ended up with this

[To insert-Final]

I made the holes for countersunk hex screws.
[To insert -Screw]
[To insert- Full holes]

I added the screws in Fusion.
[To insert- Scrwes]

#### Time taken- around 2 hours for entire case design.

## Journal 5
While the earlier case will work, hobbyist 3d printing cannot accomodate such large sizes. So, to counter this, I designed another case of the same layout, split in 3 pieces in the base and a top with 2 pieces, making an integrated plate case.

I started with a new sketch with same measurements.
[To insert- New sketch]

I extruded all the base parts one by one
[To insert- Extrusion]

Next, the walls 
[To insert- Walls]

Aligned everything.
[To insert- Alignment]

I imported the plate and then extruded it and aligned it with the switches.
[To insert- Plate dxf]

Then extruded the sides to complete the plate.
[To insert-Completed plate]

After fixing the walls, this is how the case looked.
[To insert- Full plate]

I then added the extruded the top part
[To insert- Top added]

I cleaned up everything, made the cutout for the nice!nano.
I added colors to the keyboard and the color scheme I am going for.
[To insert- coloring]

Then I added holes for the screws
[To insert-Complete]

Inserted screws
[To insert- Screws]

For the split case, I also added small tab like structures to help for structural integrity
[To insert tab]

And done!

#### Time taken - around 1.5 hours for split case design.