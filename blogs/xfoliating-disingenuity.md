<style>
.image-center{
	display: block;
	margin-left: auto;
	margin-right: auto;
}
</style>

The idea actually reached it's inception during my time working on the [Covindia](https://covindia.com) website, when I was discussing stuff with [Srikar](https://github.com/AnantaSrikar). The first thing you notice when you text him is his "substantial" use of the phrase "xD". So yes, you can pretty much figure out the next course of action: make a bot that reacts to every xD it encounters until it annoys the sugar honey iced tea out of them.

To be very honest, the bot in itself is worth next to nothing. It's literally the second paragraph of [discord.py documentation](https://discordpy.readthedocs.io/en/latest/) about reading texts and output messages. A five year old could code it up. The only important significant aspect of this bot is the message texts.

My initial plan was to just spam multiple messages of "xD" whenever the ominous chant was, well, chanted. Being excruciatingly unintuitive, I decided to take it one step ahead and add in a cute splash of pseudo-randomized casual nihilism. I "composed" a bunch of text responses designed to make the user doubt their mental stability, or just laugh it off and make them reply with another xD, thus re-iterating it to the point of annoyance. Either way, win-win.

Because what's life without a satisfying morning cup of home brewn dysphoria (and java). So that's what I did. Making the bot stand out by forcing the user to question his sanity is one of the small things in life that drive me to satisfaction.

Now obviously I wasn't satisfied with simple text-based responses (because reading is for losers). Consequently, I decided to consider ASCII art. The first few templates were made by yours truly. -Terrible idea-. It was an absolute pain because normal text editor formatting was quite different to discord text formatting, so the spaces were crunched, letters were of different sizes, and my ascii art went from a Da Vinci to a Jackson Pollock (and not in a good way). That was my first hiccup, which was kinda stupid in my professional opinion, because the discord formatting that caused me problems was indeed the very solution to it.

Being a baby to everything about everything, I was unaware of the existence of the \`\`\` format in discord (known as the code block if I'm not wrong), and after a couple hours of getting confused between \` and ' (don't), everything sailed as smooth as the head of a newborn baby.

<img src="https://raw.githubusercontent.com/MU-Enigma/store/master/blogs/assets/xfoliating_disingenuity/XDBot_0.jpg" width="300vw;" style="max-width: 400px;" class="image-center">
<p style="text-align: center">xD Bot xD-ing</p> <br>

<img src="https://raw.githubusercontent.com/MU-Enigma/store/master/blogs/assets/XDBot_1.jpg" width="300vw;" style="max-width: 400px;" class="image-center">
<p style="text-align: center">Some more xD-ing</p> <br>

Now given the "spontaneous" characteristic of the bot in consideration, I had to make sure it ran perpetually, so as to not miss any potential targets. My first thought went to the cloud, but it wasn't cool enough for me (and totally not because I could not figure how to get it set up). So instead, I pulled out my raspberry pi and kept my bot running on there. This didn't prove to be as easy as I thought, for there was a minor hiccup in this too.

The problem I faced was not due to some irregularity in the code, it was a network issue. My code was adequate to run on the pi, but I wasn't able to login to discord through it. Initially I thought it was an inherent pi bug, but I simply doubted the sophistication of the pi for my selfish needs. I ultimately found out the problem but not the exact reason for it.

I had SSH'd into my pi through an ethernet cable network, then connected my pi to my home WiFi for the internet. This seemed to cause some errors, for reasons unknown to me, as SSH'ing through the WiFi directly seemed to solve this issue. Still haven't figured out why this happened, but I'm on the lookout for answers.

Basically, this is the most low-effort unintuitive piece of code you'll ever come across. But hey, as long as it annoys people to the point of crushing loss of irony, I'm happy.

Src Code: [xdbot](https://github.com/wonder-coconut/xdbot)
