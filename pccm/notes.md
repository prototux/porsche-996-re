# Notes

* The IVI is clearly one from a chinese OEM, seemingly for mostly changan cars, as well as some geely and DFSK cars
* * The source code clearly references some models (B17, Geely CV, Geely SV, S401, Changan V301 S, Changan R103 H15T, DFSK F507, CS35, CS75, CD101, C201, B211)
* The IVI also seems to follow a "mcu for low level stuff, with a android SoC for display', actually with 2 subsystems over UART, main MCU and a DVD player (?!?)
* The android part seems to be mostly a stock Android marshmallow (6) AOSP rom with their custom "coagent" apps on top of it
* For some reason, i cannot find the skin/theme/customization for porsche, it looks like the resources for that are not in the apk
* Actually, there's no reference to any porsche stuff in the APK, looks like the customization is only a theme somewhere for the APKs and some CAN code in the MCU (?!?)
* There's pretty much no security, if you stay on the version you get a debug menu, in this menu you can launch the default AOSP launcher, then install any apk from a sd card in the navigation sd slot
* The navigation seems to be a 3rd party one from iGo, pretty much untouched
* The wifi seems to exist, but there's no default way to enable it, need to check that
* The USB ports doesn't seems to be used for ADB/debug
* There's plenty of debug apps, seems like they again did the "hey, it works on my test bench, let's ship it as is!"
* The AOSP launcher is here, but i don't find how/where it launches the real IVI app
* The apps are pretty much all in odex/oat, so the apk needs to be patched to reintroduce the classes.dex file in them
