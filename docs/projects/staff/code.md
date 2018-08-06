# Coding Craig's Staff
## @description @boardgame@ craig's staff: coding challenge

## ~ avatar avatar 

Program different light patterns to make Craig's staff light up like a diamond! 

## ~

**Concepts:** 

* Light
* Brightness
* Sound

## Duration ~ 10 minutes

## Step 1: Coding the light

Open [MakeCode](@homeurl@) in your web browser.

From ``||light:LIGHT||``, drag 2 ``||light:show ring||`` and place them into the ``||loops:forever||`` block. 
Make one ``||light:show ring||`` all blue and the other all white.

```blocks
forever(function () {
    light.showRing(
    `blue blue blue blue blue blue blue blue blue blue`
    )
    light.showRing(
    `white white white white white white white white white white`
    )
})
```

## Step 2: Set the brightness

Set the brightness value higher to make the pixels have a brighter glow.

From ``||light:LIGHT||`` drag a ``||light:set brightnes||``  into the ``||loops:on start||``.
 Set the brightness to ``200``

```blocks
light.setBrightness(200)
```

## Step 3: Coding your staff to make noise

From ``||input:INPUT||``, drag out a ``||input:on shake||``. Next, drag a ``||music:play sound||`` from the ``||music:MUSIC||`` and place it into the ``||input:on shake||``. From the dropdown menu, click **magic wand**. 

```blocks
input.onGesture(Gesture.Shake, function () {
    music.playSound(music.sounds(Sounds.MagicWand))
})
```

This will make your staff play a magical sound when you shake it! 

## Step 4: Glowing rainbow in the dark

From ``||input:INPUT||``, drag out a ``||input:on light dark||``. Then, drag a ``||loops:repeat 4 times||``  from the ``||loops:LOOPS||`` and place it into the ``||input:on light dark||``. Change the 4 to 20. Lastly, drag a ``||light:show animation||`` from the ``||light:LIGHT||`` and place it into the ``||loops:repeat 20 times||``. Change the 500 ms to 30000 ms.

```blocks
input.onLightConditionChanged(LightCondition.Dark, function () {
    for (let i = 0; i < 20; i++) {
        light.showAnimation(light.rainbowAnimation, __internal.__timePicker(30000))
    }
})
``` 

### ~

Good job, you are all done!

Download all the code to your @boardname@ and start making your staff!

### ~button /projects/staff/make
NEXT: Start making!
### ~
