## Allowing users to make choices

There might be a situation where you want a user to be able to choose from a set of options. 

### The variable

To do this you need to make a <code style="background-color: #dc143c">Variable</code>. 

Open the <code style="background-color: #dc143c">Variables</code> menu in your Toolbox, and click **Create a variable**. 

Give your variable a **meaningful** name, one that represents the choice the user is making. 

Drag the <code style="background-color: #dc143c">set</code> block into the <code style="background-color: #1e90ff">on start</code> and set your variables value to `1`.

### Changing the variable

Next you need to add some <code style="background-color: #d400d4">Inputs</code> that the user can use to change the value in the variable.

You can use <code style="background-color: #d400d4">Buttons</code> or <code style="background-color: #d400d4">Gestures</code>. 

<div style="position:relative;height:calc(250px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_YWkUYA8516WY" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>

You also want to make sure the variable can't go below `1` or above the number of options you have. In the example above there are 4 options for tunes.

### Changing the output based on the variable

Now all that is left for you to do is to use an <code style="background-color: #00a4a6">if</code> block to change the micro:bit's behaviour depending on the value of the variable. 

Opn the <code style="background-color: #00a4a6">Logic</code> menu and drag an <code style="background-color: #00a4a6">if</code> block into the Workspace. 

When making choices, you don't want an <code style="background-color: #00a4a6">else</code> but you need an <code style="background-color: #00a4a6">else if</code> for each option. 

Click the `+` symbol to add the <code style="background-color: #00a4a6">else if</code> blocks, until you have the right amount. Then click the `-` symbol under the else to remove it. 

<img src="images/elseif-blocks.gif" alt="An animation showing the + symbol used to add three 'else if' sections. Finally, the 'else' is removed from the end by clicking the '-' symbol next to it" width="350"/>

Use the <code style="background-color: #00a4a6">0 = 0</code> blocks and the variable name block to set up each of your ifs. 

<div style="position:relative;height:calc(250px + 5em);width:100%;overflow:hidden;"><iframe style="position:relative;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---codeembed#pub:_DLYiFJcMrebk" allowfullscreen="allowfullscreen" frameborder="0" sandbox="allow-scripts allow-same-origin"></iframe></div>
