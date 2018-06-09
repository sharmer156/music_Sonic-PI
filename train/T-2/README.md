#So to summarise, Sonic Pi’s ADSR envelopes have the following phases: 
attack - time from 0 amplitude to the attack_level, 
decay - time to move amplitude from attack_level to decay_level, 
sustain - time to move the amplitude from decay_level to sustain_level, 
release - time to move amplitude from sustain_level to 0 
play 60, attack: 2
sleep 3

play 65, attack: 0.5

play 60, attack: 0.7, release: 4

play 60, attack: 4, release: 0.7

play 60, attack: 0.5, release: 0.5

play 60, attack: 0.3, sustain: 1, release: 1

play 60, attack: 0.1, attack_level: 1, decay: 0.2, sustain_level: 0.4, sustain: 1, release: 0.5 
![](https://i.imgur.com/V36PcFf.jpg)
#pan 偏向于某一边，-1为左，1为右，0或者不知道为平衡

# Welcome to Sonic Pi v3.1
#release 和attack都是伸缩播放时长，有区别release直接上升第一个音节然后再拉伸，attack是线性伸缩
play 60, release: 2
play 60, attack: 2
sleep 3
play 65, attack: 0.5
stop
use_synth :mod_tri
#beep 柔化，pulse 四边形话音频，fm和弦化
#mod_形成风格连续（原曲为轻柔的），mod_beep神秘感,mod_dsaw电吉他，mod_saw快的电吉他，:mod_sine轻柔化，:mod_tri电音化
play 55, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 50, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 60, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 62, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 66, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 63, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 57, beans: 0.5, cheese: 3, eggs: 0.1, beans: 2,amp:1,release:1
sleep 0.25
play 50
sleep 0.25
play 57
sleep 0.25
stop

use_synth :tb303
play 38
sleep 0.25
use_synth :dsaw

play 50
sleep 0.25
use_synth :sprophet
play 57
sleep 0.25

stop
use_synth :prophet
#saw 使声音尖锐化的风格，电音
play 38
sleep 0.25
play 50
sleep 0.25
play 62

stop
play 38
sleep 0.25
play 50
sleep 0.25
play 62
sleep 0.25

stop
use_synth :saw
#saw 使声音锐化的风格，电音
play 38
sleep 0.25
play 50
sleep 0.25
play 62
sleep 0.25


