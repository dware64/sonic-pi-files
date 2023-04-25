~~~ruby
'''
PLAY NOTES ALL AT ONCE
'''
##| play 60
##| play 67
##| play 69

'''
PLAY NOTES IN SQUENCE
'''
##| play 60
##| sleep 1
##| play 67
##| sleep 1
##| play 69

'''
USE NOTES FROM THE C-MAJOR SCALE TO CREATE A MELODY
(72, 74, 76, 77, 79, 81, 83 or :C5 :D5 :E5 :F5 :G5 :A5 :B5)
USE SLEEP WITH DIFFERENT VALUES TO VARY THE RHYTHM.
'''
##| use_bpm 120

##| play 72
##| sleep 0.25
##| play 76
##| sleep 0.25
##| play 76
##| sleep 0.25
##| play 72
##| sleep 0.5
##| play 83
##| sleep 0.25
##| play 74
##| sleep 0.25
##| play 83
##| sleep 0.25
##| play 79
##| play 84

'''
REPEAT A MELODY
'''

##| 2.times do
##|   play :c4
##|   sleep 0.5
##|   play :d4
##|   sleep 0.5
##|   play :e4
##|   sleep 0.5
##|   play :c4
##|   sleep 0.5
##| end

'''
USE REPITION INSIDE REPITION
'''
##| 4.times do
##|   4.times do
##|     play :c4
##|     sleep 0.25
##|   end
##|   play :d4
##|   sleep 0.5
##|   play :f4
##|   sleep 0.5
##| end

'''
DRUM BEAT
'''
##| live_loop :drums do
##|   sample :drum_heavy_kick
##|   sleep 1
##| end

'''
STEADY DRUM BACKBEAT
'''
##| use_bpm 100

##| live_loop :drums do
##|   sample :drum_heavy_kick
##|   sleep 1
##|   sample :drum_snare_hard
##|   sleep 1
##|   sample :drum_heavy_kick
##|   sleep 1
##|   sample :drum_snare_hard
##|   sleep 1
##| end

'''
MULTIPLE LIVE LOOPS
'''
use_bpm 100

live_loop :drums do
  sample :drum_heavy_kick
  sleep 1
  sample :drum_snare_hard
  sleep 1
  sample :drum_heavy_kick
  sleep 1
  sample :drum_snare_hard
  sleep 1
end

live_loop :hihat do
  sample :drum_cymbal_closed
  sleep 0.25
  sample :drum_cymbal_pedal
  sleep 1
end

'''
CHANGE THE SYNTH - 4 BASS TRACK
'''
##| live_loop :bass do
##|   use_synth :fm
##|   play :c2
##|   sleep 0.25
##|   play :c2
##|   sleep 2
##|   play :e2
##|   sleep 0.75
##|   play :f2
##|   sleep 1
##| end

'''
CHANGE THE LENGTH OF NOTES
attack and release control the amplitude of a note over time:
'''
##| play 60, attack: 1, release: 3

'''
You could make a short staccato note by setting attack to zero and 
release to a very short value:
'''
##| play :c4, attack: 0, release: 0.2

'''
EXAMPLE DRUM TRACK
'''
use_bpm 100

live_loop :drums do
  sample :drum_heavy_kick
  sleep 1
  sample :drum_snare_hard
  sleep 1
  sample :drum_heavy_kick
  sleep 1
  sample :drum_snare_hard
  sleep 1
end

live_loop :hihat do
  sample :drum_cymbal_closed
  sleep 0.25
  sample :drum_cymbal_pedal
  sleep 1
end

live_loop :bass do
  use_synth :fm
  play :c2, attack: 0, release: 0.25
  sleep 0.25
  play :c2, attack: 0, release: 0.3
  sleep 2
  play :e2
  sleep 0.75
  play :f2
  sleep 1
end
~~~
