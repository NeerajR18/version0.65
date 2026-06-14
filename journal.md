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

<img width="975" height="517" alt="image" src="https://github.com/user-attachments/assets/367d3ed0-541b-4b01-a5eb-d9276d812d54" />


I assigned footprints and now I have to place all the components.
For this, I used the grid from the guide,and the generated plate from the ai03 plate generator.

#### Time taken - around 2 hrs to make the schematic and place all switches.

## Journal 2

Today, I did the entire PCB layout!
This is my favourite part of the entire PCB design because it really gets me thinking because of constant changes to the layout and I get to crashout.

<img width="975" height="343" alt="image" src="https://github.com/user-attachments/assets/00c1f792-39a0-41db-a3b2-d841cb9ccb86" />

I had already laid down the keys, so all I had to do was routing. I had also not laid out the diodes and added the stabilizers correctly. The Leopold does not have a very long right shift so, I had to change those, and also while updating the schematic, some of the footprints were changed only in the PCB editor, which caused it to change.
I fixed everything, then I decided that the top right of the PCB is the best placed for the supermini. It increases the height a bit, but yes, that is inevitable imo but it is also almost equivalent to the size of the Leopold 660m(with case but yes since this is custom, I have my say ;D )

This is how the keyboard looked after I placed the diodes.

<img width="975" height="444" alt="image" src="https://github.com/user-attachments/assets/2186d92b-974c-4675-a3e9-0fce7f35b79e" />

Now, routing is always a challenge with the matrix, as it can be optimised in such a way that there is no need for vias and it looks clean.
I had to change the pins many times while routing this.
I routed all the diodes first. I have my own way of routing diodes so that it passes with some gap with the holes.
Sure, the normal way is fine but there is always a risk.

<img width="975" height="321" alt="image" src="https://github.com/user-attachments/assets/88e2e5bc-a78c-4242-a6a6-0a2eeb918aaa" />

Here are some images of the PCB routing process-

<img width="975" height="431" alt="image" src="https://github.com/user-attachments/assets/54597d34-61b2-4f1d-994e-ef3dd42188b0" />

This was the first routing layout I did. The GPIOs were unreachable and the traces were too far apart, increasing the width of the PCB.
I changed this.

I changed my pins a few more times and reached to this layout. All that was left were the ground connections and battery connections.
I added the battery connections.
<img width="975" height="406" alt="image" src="https://github.com/user-attachments/assets/2eb1f3b3-f9ab-45db-86e3-848689b6e513" />


I then added a ground plane on both sides to finish the PCB. I also made the edge.cuts to finalise the board edges.
This is how it looks.
<img width="975" height="435" alt="image" src="https://github.com/user-attachments/assets/f66f610b-1767-4e10-a06b-95342a35d1e5" />

DRC was run, and no errors occured!
I need to add some silkscreen, and add keycaps and switches to the PCB to move to CAD.

#### Time taken - around 2.5 hours to finish up the PCB routing, remaining layout etc. (I also changed many things in the schematic for the PCB, thus the long time.)

## Journal 3 

Now, I started by adding the keycaps. Since I have already done a PCB design, I had a easy way to add the switches and keycaps, by taking the x,y,z and angle values and noting them and directly plugging them in. This is also a fun but time taking part
This is how the first keycap looks-

<img width="975" height="698" alt="image" src="https://github.com/user-attachments/assets/9443f5db-09f8-4591-9163-d6cfffd986e5" />


KiCad crashed on me once today while adding the keycaps

Here is me adding the backspace keycap
<img width="975" height="800" alt="image" src="https://github.com/user-attachments/assets/255bf1e8-9751-46da-b8db-32ca4d403cdf" />


This is some tiresome work, but here is the PCB after I added half of the keycaps
<img width="975" height="471" alt="image" src="https://github.com/user-attachments/assets/b4c70947-02a5-4fe2-a91b-dd41867b5525" />


And the last keycap 
<img width="952" height="939" alt="image" src="https://github.com/user-attachments/assets/ee1c944f-eb4f-4d82-a18f-3aa09f05ea4a" />


This is how the PCB looks 
<img width="975" height="419" alt="image" src="https://github.com/user-attachments/assets/8c3a4e67-9e67-4460-b08c-d25fdb9f5239" />


#### Time taken - 50 minutes to manually add and align all switches and keycap models.

## Journal 4

I started CAD today. I have decided for a sandwich mount case. I also will leave out the space for the devboard.

I imported the the .step of the PCB from KiCad to Fusion.

<img width="975" height="600" alt="image" src="https://github.com/user-attachments/assets/bf0bb9c8-3059-4dab-a2f0-d32916a1e5a4" />


Then, I made a sketch to make the base.
The base was made to have 8mm thick walls on each side.

<img width="975" height="498" alt="image" src="https://github.com/user-attachments/assets/d3b67d1c-10ae-4eed-ad4e-c73a4b1d8252" />


I then extruded only the base under the pcb. 

<img width="975" height="596" alt="image" src="https://github.com/user-attachments/assets/85a8bdc2-3efe-4172-8219-48666cbd9cda" />


Then I made the walls and aligned it to the Top edges of the PCB

<img width="975" height="483" alt="image" src="https://github.com/user-attachments/assets/dfd51632-6c08-44f4-9178-72cd80211ac9" />

<img width="975" height="542" alt="image" src="https://github.com/user-attachments/assets/e17176ab-6eb4-4d7d-8240-e01ff3f208d4" />

I then imported the plate.dxf from ai03's plate generator 
<img width="975" height="821" alt="image" src="https://github.com/user-attachments/assets/4d52b7d2-3ea4-4662-b057-0ede3afadd88" />

I then aligned the plate to the keycaps, extruded the sides to match the entire base length.

<img width="975" height="442" alt="image" src="https://github.com/user-attachments/assets/96166930-9d39-4031-ae59-fef807d3c5ea" />

<img width="975" height="783" alt="image" src="https://github.com/user-attachments/assets/9a8e42c2-b733-49cc-8d1d-aa097625ab6e" />


This was the case halfway done.
<img width="975" height="483" alt="image" src="https://github.com/user-attachments/assets/2a6b7f89-0e05-4cfb-9293-6d3a5b008286" />


I then made the top part of the sandwich from the same sketch I used for the walls.

<img width="975" height="698" alt="image" src="https://github.com/user-attachments/assets/6c015ed4-8199-4556-9775-9a89fd109660" />


Finally, I ended up with this

<img width="975" height="600" alt="image" src="https://github.com/user-attachments/assets/57720318-4b72-4a2e-8ead-82faa1245e08" />


I made the holes for countersunk hex screws.
<img width="975" height="760" alt="image" src="https://github.com/user-attachments/assets/bbba5f2b-ec6a-422d-8b11-76dc15d81ca0" />

<img width="975" height="532" alt="image" src="https://github.com/user-attachments/assets/4dbc8c0e-9097-487d-bdda-12ef8e441faa" />


I added the screws in Fusion.
<img width="975" height="467" alt="image" src="https://github.com/user-attachments/assets/e6d47ee0-80ca-48c5-b858-f48383fdc45e" />
<img width="975" height="465" alt="image" src="https://github.com/user-attachments/assets/7dc3d2e8-cfc9-4a76-8629-35714e3c21ce" />


#### Time taken- around 2 hours for entire case design.

## Journal 5
While the earlier case will work, hobbyist 3d printing cannot accomodate such large sizes. So, to counter this, I designed another case of the same layout, split in 3 pieces in the base and a top with 2 pieces, making an integrated plate case.

I started with a new sketch with same measurements.
<img width="975" height="490" alt="image" src="https://github.com/user-attachments/assets/deb54e4a-0c79-4298-bc58-99f1d73d53de" />


I extruded all the base parts one by one
<img width="975" height="538" alt="image" src="https://github.com/user-attachments/assets/08bcca8b-a8bf-49e0-b874-ace5a159271e" />


Next, the walls 
<img width="975" height="546" alt="image" src="https://github.com/user-attachments/assets/25e1a420-f5b7-429f-8626-5062ebc2600c" />


Aligned everything.
<img width="975" height="363" alt="image" src="https://github.com/user-attachments/assets/7df0c344-92e5-433c-9719-4af4c7d05011" />


I imported the plate and then extruded it and aligned it with the switches.
<img width="975" height="281" alt="image" src="https://github.com/user-attachments/assets/36d3ad14-d988-4956-a064-41a236d6215c" />


Then extruded the sides to complete the plate.
<img width="975" height="602" alt="image" src="https://github.com/user-attachments/assets/f7e44541-6618-4fd5-90f8-9025da09234b" />


After fixing the walls, this is how the case looked.
<img width="975" height="494" alt="image" src="https://github.com/user-attachments/assets/92329579-87b5-41a7-81bb-21e1105658ed" />
<img width="975" height="635" alt="image" src="https://github.com/user-attachments/assets/40b84179-b582-46a5-ad02-21c19554448a" />


I then added the extruded the top part
<img width="975" height="433" alt="image" src="https://github.com/user-attachments/assets/ffabd2e8-249d-4e7e-a42e-d589d61ed183" />

I cleaned up everything, made the cutout for the nice!nano.
I added colors to the keyboard and the color scheme I am going for.
<img width="975" height="554" alt="image" src="https://github.com/user-attachments/assets/b784a5a9-0ef8-4f3b-8524-c8ae053b6932" />


Then I added holes for the screws
<img width="975" height="417" alt="image" src="https://github.com/user-attachments/assets/67f9bf0a-bba2-40fc-8f22-ac912fea14ca" />


Inserted screws
<img width="975" height="423" alt="image" src="https://github.com/user-attachments/assets/a6df24b6-c662-45b1-b29d-1d0e4a129711" />
<img width="975" height="504" alt="image" src="https://github.com/user-attachments/assets/c2d3e96b-90d8-4392-acc8-e0c80b6fa02a" />


For the split case, I also added small tab like structures to help for structural integrity
<img width="322" height="314" alt="image" src="https://github.com/user-attachments/assets/116922b7-fc8c-4ff9-8756-d8beee176235" />


And done!

#### Time taken - around 1.5 hours for split case design. 

## Journal 6
I made the firmware for the keyboard. I am using ZMK, which is pretty new to me and so are bluetooth keyboards.
This was a pretty huge task. I first set up ZMK on my device using the docs.
<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/f13aae17-eeb3-4bdc-a348-05d4822ad848" />

After this, I edited the keymaps and all config files, and made the .uf2 file.
The firmware itself was pretty easy to do but the configuration and manual assignment was pretty slow from my side, and I had to keep verifying it.
It took me 9 commits to fix the errors to build the .uf2 file.
Anyways, I am ready to submit. I have also made the BOM and repo.

#### Time taken- around 1.5 hours for firmware.
