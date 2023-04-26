~~~ruby
4.times do
  sample :loop_amen, rate: 0.75
  sleep 2.3
end

##| live_loop :flibble do
##|   sample :ambi_choir, rate: 0.2
##|   sample :bd_haus, rate: 1
##|   sleep 0.5
##| end

##| live_loop :guit do
##|   with_fx :echo, mix: 0.5, phase: 0.25 do
##|     sample :guit_em9, rate: 0.5
##|   end
##|   sample :guit_em9, rate: -0.5
##|   sleep 8
##| end
~~~
