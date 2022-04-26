## Drum Machine

~~~ Ruby
# DRUM MACHINE

use_bpm 100

#######################################################

k = [1,0,1,0,0,0,0,1,0,0,1,0,0,0,0,0] # kick

s = [0,0,0,0,1,0,0,0,0,0,0,0,1,0,0,0] # snare

t = [1,0,0,0,1,0,0,0,1,0,0,0,1,0,0,0] # clap (snap2)

c = [1,0,1,0,1,0,1,0,1,0,1,0,1,0,1,0] # close hi-hat

o = [0,1,0,0,0,1,0,0,0,1,0,0,0,1,0,0] # open hi-hat

#######################################################

live_loop :beat_maker do
  16.times do |i|
    sample :drum_tom_hi_hard if k[i] == 1
    sample :drum_snare_hard if s[i] == 1
    sample :perc_snap2 if t[i] == 1
    sample :drum_cymbal_closed if c[i] == 1
    sample :drum_cymbal_pedal if o[i] == 1
   
    sleep 0.25
  end
end

~~~
