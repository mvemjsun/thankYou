![Thank you](https://github.com/mvemjsun/thankYou/blob/master/thankYou.png)

# CSS , HTML & JS say Thank You !

## TL;DR
This is an attempt to say thank you 🙏🏻to the key workers in the fight against Corona virus using a combination of CSS, HTML and some Java script !!

## Background
These are strange times, most of us locked up at home trying to go about the daily lives as "normally" as we can. Society has finally realised the importance of its most essential contributors who are key to our wellbeing and survival but often go unnoticed and under compensated.

We have been trying to thank you to these key workers in various ways and one of the early ways to raise awareness was children drawing rainbows and then posting the pictures on the window of their houses. This is my attempt to do the same albeit using software. I hope that it's fun and useful read for you.

## Discussion of the HTML
Most of the HTML is simple and quite self explanatory, I will discuss some of the key points here.

- We will set up a `sky` then layout a `viewArea` in front of it that will house the rainbow colours and finally we will say "Thank You"

- The `sky` CSS class has a width of 100% so that it spans the whole view & it has a height that is the same as the `viewArea` CSS class. We have also given it a `linear-gradient` so that it appears as sky above the white clouds.

- The `viewArea` is a flex container. The items in the flex container will be placed in a `column` one above the other and will be aligned in the centre.
The individual rainbow colours are driven using the CSS classes `v`, `i`, `b`, `g`, `y`, `o` & `r` in the HTML each for one of the 7 VIBGYOR 🌈colours. The classes are similar, they form a set of semi circles that are then laid on top of each other by a `top` displacement that grows by 40px for each colour. Similarly the `height` and `width` also decrease proportionally for each following colour.
We then have the `thankYouText` CSS class and the `thankYouText::before` CSS pseudo class.

- The property `-webkit-background-clip` ensures that the background of the text is clipped at its content box.
- The idleText CSS class 😎, 
The idea behind setting up of this class and the pseudo class is so that we can display & hide (opacity) the main class `thankYouText` & the pseudo element `thankYouText::before` one after the other at regular interval.
The `background` of the Thank You text is set using the global variables `shade1` & `shade2` respectively. These are set one by one from a standard set of gradients defined in the `shades` array.

- The script  🚀
When the page loads a scripts starts to execute at regular intervals that sets the variables `shade1` & `shade2` and the opacities of `thankYouText` and its pseudo element which gives the magic effect of the shining rainbow.
