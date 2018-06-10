# Tilburg 2

# Coded by Sam Aaron
一首比较长的

    use_debug false
    load_samples :guit_em1, :bd_088
    
    
    live_loop :high do
      tick
      synth :zawa, wave: 1, phase: 0.25, release: 1, note: (knit :e3, 8, :c1, 4).look, cutoff: (line 60, 120, steps: 6).look
      synth :beep, wave: 1, phase: 0.25, release: 1, note: (knit :e3, 8, :c1, 4).look, cutoff: (line 50, 100, steps: 6).look
      sleep 4
    end
    
    with_fx :reverb, room: 1 do
      live_loop :lands, auto_cue: false do
    use_synth :dsaw
    use_random_seed 310003
    ns1 = (scale :e2, :minor_pentatonic, num_octaves: 2).take(4)
    ns2 = (scale :e4, :minor_pentatonic, num_octaves: 2).take(4)
    ns3 = (scale :e6, :minor_pentatonic, num_octaves: 2).take(4)
    8.times do
      play ns1.choose, detune: 12, release: 0.1, amp: 2, amp: rand + 0.5, cutoff: rrand(70, 120), amp: 1
      play ns2.choose, detune: 12, release: 0.1, amp: 2, amp: rand + 0.5, cutoff: rrand(50, 100), amp: 1
      play ns3.choose, detune: 12, release: 0.1, amp: 2, amp: rand + 0.5, cutoff: rrand(40, 80), amp: 1
      sleep 0.125
      
    end
      end
    end
    
    live_loop :fietsen do
      sleep 0.25
      sample :guit_em9, rate: -10
      sleep 7.75
    end
    
    live_loop :tijd do
      sample :bd_haus, amp: 1.5,rate: -10,cutoff: 10
      sleep 2.5
    end
    
    live_loop :init do
      sample :loop_industrial, beat_stretch: 1,rate: -10,cutoff: 10
      sleep 1
    end
