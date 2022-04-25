## Ring Tone Example

~~~ ruby
use_synth :chipbass

5.times do
  play [:F, :C, :As4, :C, :F].tick
  sleep 0.2
end

sleep 1

13.times do
  play [:G, :G, :As4, :C, :C, :As4, :G, :C, :F, :C, :As4, :C, :F].tick
  sleep 0.2
end
~~~
