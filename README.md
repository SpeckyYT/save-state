# SAVE-STATE

Saves a bit across attempts.

```spwn
import "save-state"

state = @save_state::new()

state.bit.display(100, 100)

wait(0.05) // waiting at least 0.02 seconds from the beginning of the level is ideal

if state.bit == 0 {
    state.save(true)
    BG.pulse(rgb(1,0,0), 0.1, 0.1, 0.1)
} else {
    state.save(false)
    BG.pulse(rgb(0,1,0), 0.1, 0.1, 0.1)
}
```
