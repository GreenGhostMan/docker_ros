docker image ကို သုံးဖို့ အောက်ပါအတိုင်း pull လုပ်ပါ။

docker pull ghostmanvsrobot/ros-kinetic-base

ပြီးရင် အောက်က script ကို ရေးပြီး run ပါ။

#!/usr/bin/bash
xhost +local:root
docker run -it --network='host' --env='DISPLAY' --env='QT_X11_NO_MITSHM=1' --volume='/tmp/.X11-unix:/tmp/.X11-unix:rw' --volume='/path/to/hostdir:/containerdir' ghostmanvsrobot/ros-kinetic-base bash
