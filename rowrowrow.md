# Row Row Row

~~~ Ruby

with_transpose -12 do
  use_synth :sine
end

use_bpm 110

play_pattern_timed [:C,:C,:C,:D,:E,:E,:D,:E,:F,:G],[1,1,0.6,0.4,1,0.6,0.4,0.5,0.5,1]

sample :drum_cymbal_hard
sleep 1

play_pattern_timed [:C5,:C5,:C5,:G,:G,:G,:E,:E,:E],[0.33,0.33,0.34,0.33,0.33,0.34,0.33,0.33,0.34]

play_pattern_timed [:C,:C,:C,:G,:F,:E,:D,:C],[0.33,0.33,0.34,0.6,0.4,0.6,0.4,1]

sample :drum_cymbal_hard

~~~
