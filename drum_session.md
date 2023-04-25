
~~~ ruby
live_loop :beat do
  sample :drum_heavy_kick
  sleep 0.5
  sample :drum_snare_soft
  sleep 0.5
end

live_loop :hihat do
  sleep 3.9
  sample :drum_cymbal_closed
  sleep 0.1
end

live_loop :bass do
  use_synth :dsaw
  play :a2, attack: 1, release: 2, amp: 0.3
  sleep 2.5
  use_synth :tech_saws
  play :a1, attack: 1, release: 1.5, amp: 0.8
  sleep 1.5
end

live_loop :lead do
  with_fx :slicer do
    chords = [(chord :A4, :minor7), (chord :A4, :minor), (chord :D4, :minor7), (chord :F4, :major7)]
    use_synth :blade
    play chords.choose, attack: 1, release: 2, amp: 1
    sleep 2
  end
end
~~~
