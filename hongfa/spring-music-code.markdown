# 春篇章的音乐源码
总体曲风

篇章	风格	曲式	旋律	速度	表情	强弱	调式	和声

春	微分音乐	三段回旋	柔美	小柔板	如歌地田园风格	中弱	小调	和弦

序曲	低起			入音旋回			尾声

音频中可视化划分
![enter description here](https://i.loli.net/2018/12/28/5c25e77587e8f.jpg)


[1, 3, 6, 4].each do |d|
  (range -3, 3).each do |i|
    play_chord (chord_degree d, :c, :major, 3, invert: i)
    sample :perc_bell, rate: rrand(-6.5, 1)
    sleep rrand(0.02, 0.3)
    sleep 0.01
  end
end


live_loop_bar do
  with_fx:echo,phase:1.125,mix:1.8 do
    sample :guit_harmonics,amp:2
  end
  #  sleep 2
end

stop

`live_loop :haunted do
    sample :perc_bell, rate: rrand(-1.5, 1.5)
    sleep rrand(0.1, 2)
  end
`


stop
use_bpm 50


with_fx :lpf, cutoff: 90 do
  with_fx :reverb, mix: 0.5 do
    with_fx :compressor, pre_amp: 40 do
      with_fx :distortion, distort: 0.4 do
        live_loop :jungle do
          use_random_seed 667
          4.times do
            sample :loop_amen, beat_stretch: 0.5, rate: [1, 1, 1, -1].choose / 2.0, finish: 0.5, amp: 0.5
            sample :loop_amen, beat_stretch: 0.5
            
          end
        end
      end
    end
  end
end
stop
