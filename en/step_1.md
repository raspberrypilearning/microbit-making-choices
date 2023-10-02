## Allowing users to make choices

There might be a situation where you want a user to be able to choose from a set of options. 

### The variable

To do this you need to make a variable. 

Open the `Variables`{:class='microbitvariables'} menu in your Toolbox, and click **Create a variable**. 

Give your variable a **meaningful** name, one that represents the choice the user is making. 

Drag the `set`{:class='microbitvariables'} block into the `on start`{:class='microbitbasic'} and set the value of your variable to `1`.

### Changing the variable

Next you need to add some inputs that the user can use to change the value in the variable.

You can use buttons or gestures. 

```microbit
let tune = 0
input.onButtonPressed(Button.A, function () {
    tune += -1
    if (tune < 1) {
        tune = 4
    }
})
input.onButtonPressed(Button.B, function () {
    tune += 1
    if (tune > 4) {
        tune = 1
    }
})
```

You also want to make sure the variable can't go below `1` or above the number of options you have. In the example above there are 4 options for tunes.

### Changing the output based on the variable

Now all that is left for you to do is to use an `if`{:class='microbitlogic'} block to change the micro:bit's behaviour depending on the value of the variable. 

Open the `Logic`{:class='microbitlogic'} menu and drag an `if`{:class='microbitlogic'} block into the Workspace. 

When making choices, you don't want an `else`{:class='microbitlogic'} but you need an `else if`{:class='microbitlogic'} for each option. 

Click the `+` symbol to add the `else if`{:class='microbitlogic'} blocks, until you have the right amount. Then click the `-` symbol under the else to remove it. 

<img src="images/elseif-blocks.gif" alt="An animation showing the + symbol used to add three 'else if' sections. Finally, the 'else' is removed from the end by clicking the '-' symbol next to it" width="350"/>

Use the `0 = 0`{:class='microbitlogic'} blocks and the variable name block to set up each of your ifs. 

```microbit
basic.forever(function () {
    let tune = 0
    if (tune == 1) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Dadadadum), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Duck)
    } else if (tune == 2) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Punchline), music.PlaybackMode.UntilDone)
    } else if (tune == 3) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Birthday), music.PlaybackMode.UntilDone)
    } else if (tune == 4) {
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Baddy), music.PlaybackMode.UntilDone)
    }
})
```
