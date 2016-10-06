# nvfan
**NVidia Fan control patch on UBUNTU**

monitor NVidia GPU temperature and set fan speed to avoid overheating
(guess nvidia wants to kill my old GPU :D with last driver update)


**the problem:** nvidia doing crazy this as flicks, monitor detect fail, screen resolutions change and crashes
all due to overheating while fan sits on 30% ~ 40%, sometimes on 30& when over 90º

using ubuntu 16.04 and nvidia 304.171 on my G71GL [Quadro FX 1500]

this is a simple script to solve my specific problem until ubuntu/nvidia solve it.
i'm sharing it as is, fell free to adapt, use at you own risk.

##settings:

MAX - play alarm sound (dont know if it works because i've never reached it)

TOP - start increasing fan pwm by 5% (and repeat) while over this value

AUTO - revert to driver control when droping below this point

WATCH - monitor timer tick


##features:

revert to driver control when leaving the script


##notes:

to allow this kind of control i had to set coolbits to 4

    sudo nvidia-xconfig --cool-bits=4

_be sure to revert to original settings when the problem is solved (/etc/X11/xorg.conf backup)_
