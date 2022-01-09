# SAVE-STATE

Saves a bit across attempts.

*currently only 1 bit works*

```spwn
import "save-state"

state = @save_state::new()

state.sum.display(100, 100)

wait(0.05) // waiting at least 0.03 seconds from the beginning of the level is ideal

if state.sum == 0 {
    state.save(1)
    BG.pulse(rgb(1,0,0), 0.1, 0.1, 0.1)
} else {
    state.save(0)
    BG.pulse(rgb(0,1,0), 0.1, 0.1, 0.1)
}
```
