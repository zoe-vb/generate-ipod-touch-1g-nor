# Preparing a NOR file for iPod Touch 2G
### This process is different to the iPod Touch 1G because we now have LLB support! <br>
Copy all the files from Firmware/all_flash/all_flash.n72ap.production into the data folder <br>
Rename the files to look as below <br>
`recoverymode.img3, applelogo.img3, batterylow0.img3, batterylow1.img3, dtree.img3 (originally DeviceTree.n72ap), glyphcharging.img3, glyphplugin.img3, needservice.img3, iboot.img3 and llb.img3` <br>
Delete the other files that aren't mentioned <br>
Now due to the fact that A: Apple made the NOR contain encrypted img3 files and B: We have LLB now anyway which decrypts the images, we no longer have to worry about decrypting <br>
Now compile `generate_nor` as described in the `main` branch. And run `./generate_nor` <br>
This leaves you with a NOR image.
