# SAVE-STATE

Saves bits across attempts.

Currently it works up to 4 bits.
When reaching number 16, it skips to [number 17](https://youtu.be/vPKynTlqqdM) and bricks all the triggers.

```spwn
import "save-state"

state = @save_state::new()

state.sum.display(100, 100)

wait(0.05) // waiting at least 0.05 seconds (3 frames) from the beginning of the level is ideal

if state.sum == 0 {
    state.save(1)
    BG.pulse(rgb(1,0,0), 0.1, 0.1, 0.1)
} else {
    state.save(0)
    BG.pulse(rgb(0,1,0), 0.1, 0.1, 0.1)
}
```
