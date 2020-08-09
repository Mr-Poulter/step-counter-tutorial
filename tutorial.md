# Step Counter

## Step 1
This program will count down steps from a step goal, and show you a
smiley face on the screen when you have met your goal.

First up, get rid of the **start** and **forever** blocks, and create a
variable called **step goal**.

## Step 2
You will use the **A button** to start your goal, and use the **shake** event
to detect when you have taken a step. Drag both of these in from **Input**
and then set your **step goal** to 10 when **A** is pressed.

*The shake event isn't great at detecting real steps, but good enough for now.*

```blocks
let step_goal = 0
input.onButtonPressed(Button.A, function () {
    step_goal = 10
})
input.onGesture(Gesture.Shake, function () {
	
})
```

## Step 3
From **Loops** drag in a **while** loop after you set your variable.
This loop keeps checking to see
if it needs to keep running instead of running a fixed number of times.

From **Logic** drag in a **<** block and replace the **true** in the loop
with this comparison, then change it to the **>** comparison.

```blocks
let step_goal = 0
input.onButtonPressed(Button.A, function () {
    step_goal = 10
    while (0 > 0) {
    	
    }
})
input.onGesture(Gesture.Shake, function () {
	
})
```

## Step 4
This loop will keep running while the comparison is **true**, so we want
it to run while the **step goal** is greater than 0. Drag your **step goal**
variable into the *left* side of the comparison.

Inside the loop drag a **show icon** block and set it to a *sad face* and
after the loop show a *happy face* icon.

```blocks
let step_goal = 0
input.onButtonPressed(Button.A, function () {
    step_goal = 10
    while (step_goal > 0) {
        basic.showIcon(IconNames.Sad)
    }
    basic.showIcon(IconNames.Happy)
})
input.onGesture(Gesture.Shake, function () {
	
})
```

## Step 5
Test it out using the **A button**.
Your code should mostly work now but you will only see a sad face because
the steps never go down.

Drag a **change step goal** block into the **on shake** event, and set the
amount to **-1** and try it again.

```blocks
let step_goal = 0
input.onButtonPressed(Button.A, function () {
    step_goal = 10
    while (step_goal > 0) {
        basic.showIcon(IconNames.Sad)
    }
    basic.showIcon(IconNames.Happy)
})
input.onGesture(Gesture.Shake, function () {
    step_goal += -1
})
```

## Step 6
Load your program onto a physical Micro:bit (with a battery) and see how
well the step detection works (*Hint: not very well*).

What else could you do to let you know you have hit your step goal, without
having to look at the screen?

Save your program into your **Digital Technologies** folder as **Step Counter**.
