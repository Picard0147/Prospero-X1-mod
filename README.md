# Prospero-X1-mod
Some scripts to kill original mining software and run the custom (lightweight) one

WHEN YOU TRY TO USE MY TIPS OR (IN FUTURE) SCRIPTS, YOU MAKE IT ON YOUR OWN RISK.
I'M NOT RESPONSIBLE FOR BRICKING YOU DEVICE SO BE CAREFULL...
BEFORE SOMETHING WRONG HAPPENS, MAKE SURE THAT YOU HAVE AT LEAST 
4GB MICROSD CARD AND HAVE PROPER SOFTWARE AND KNOWLEGE TO RECOVER DAMAGED 
MINER OS BY RUNING RECOVERY FROM MICROSD CARD.

Now the interesting part ;)
Point is to create script that can automatically
- install another cgminer in paraler with original, so in some directory of "ba" user (prospero is default for now)
- kill the original one including web UI
- copy config from original or create config teplate for Prospero X-1 or 1.5
- prepare start and shutdown scripts to allow simple control over ssh (ssh miner 'sh start/stop' or similar)

So here is some possibility to disable Blackaroow default control system (uncluding webUI) by simple editing file "/startServices.sh" 
/etc/init.d/ntp start
/etc/init.d/ssh start
/etc/init.d/php5-fpm start  //need to be deleted or preferably commented out 
/etc/init.d/nginx start     //need to be deleted or preferably commented out
chmod a+rw /dev/spidev0.0
chmod 666 /dev/ttyS0
chmod 666 /dev/ttyS3
/etc/init.d/bamc start      //need to be deleted or preferably commented out
ifconfig eth0

It's possibly key to make life with Prospero easier but I have to test it.

