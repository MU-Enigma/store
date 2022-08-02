---
title:  "Enigmatic Webslinger"
date:   "Aug 22"
author: "Anirudh Chimpidi"
---
# Design

Frontend always intrigues me, and this case was no different. We just had a meeting about what to do next for enigma, and one of the topics as I expected was about the Enigma website. At that point of time, the club website was a Hugo template, and the meeting to a point was considering to use yet another Hugo template to go ahead with (primarily because of the very blogging structure you see now). And there I was, unsatisfied with the choices, so, I proposed to work the site from scratch.

After some discussion, and me kind of being able to convince them to setup the main site and blogging stuff, we came to a conclusion that the Enigma site would undergo a revamp from scratch. The next question was, what would it look like? Well, for that part I suggested we could go with the designs available on the Hugo templates, or just any other design from other sites, or better make our own. I was confident about this because I had been doing sites for a while now, and the framework I use, Vue.js, is very powerful.

It was Rahul, who was really keen on site designs and suggested some quite interesting ones. At that point in time, I was trying something of my own on Figma and also suggested a concept. Rahul, who then had some more ideas about space and stars as a template and presented his version which was really good. But after some deliberation we did come to a conclusion, that kind of a design would rather suit a hackathon kind of theme not really a Club website as a whole. Moving ahead a few days and taking ideas from other club sites and templates there was another design, but there was a problem; it was a flashy light themed site ...

![Early Designs](https://raw.githubusercontent.com/MU-Enigma/store/master/blogs/assets/enigmatic_webslinger/pre-design.png)
### Early Designs of the website

Well, that was kinda our thing to criticize anything with a light theme lol. Anyway, keeping these jokes aside, we did come to our final design. The next part was where all the fun (and pain) began.

# Implementation

I decided to go with [Vue](https://vuejs.org/), a frontend JS webdev framework, along with a non bundling framework, [Vite](https://vitejs.dev/) to speed things up. For the side note, I used [TailwindCSS](https://tailwindcss.com/) as the CSS framework (makes your life so much easy). This, might sound a lot for people who are not aware, but these frameworks are quite easy to use, and I have been using them for my other project (topic for some other day, maybe?) for a while now. But all this was for the main site itself, the blog part was still a mystery. And just like that I was actually able to complete the main site stuff in like 2 days, and still wondering how to go ahead with blogs.

Rounak and me came up with an idea to fetch APIs and load up blogs on the site, kinda like our own implementation. I was able to setup markdown to html parsing as well and we all thought success was assured, except when I realised the parsing only happens when the markdown files are called as Vue components, which won't be possible on live site with API calls. So, what now? I moved to using Jekyll, my only option left; the blog site as a separate page from the main site, away from Vue and Tailwind back to vanilla trinity.

I took a deep breath, and set myself up for that, and to my surprise I was able to mimic the exact components in vanilla html and css just like the main site, precisely. Now, everything sorted out and running on local servers, it was time for the main deal: deploying on GitHub Pages (since we did not decide on the domain part yet).

# Deploy

The steps to deploy a jekyll site via GH pages were meant to be on the main domain, i.e., mu-enigma.github.io would host the site, while what we wanted was mu-enigma.github.io/blogs. It was after some numerous experiments with the entry point and path changes was I able to set it up and running the way we wanted it to be, only to see it break routing paths on local testing (which to be honest, was not a big deal).

On the contrary, deploying a Vue app on GH pages was the exact opposite to Jekyll, but apparently, and as you'd expect, it was much easier to setup and deploy, without breaking local testing routes.

Now, with everything setup and ready to deploy, we needed some automation to build and deploy the site everytime a change was pushed; come in GitHub Actions to the rescue! We were lucky enough to find an automation workflow for Vue apps with support for Vite plugin for the main site, and as for blogs, Jekyll is very well integrated to GH pages so nothing to worry about.

With all that said and done, we were able to deploy the brand new Engima site just a day before our new semester began, just like we had planned for; a whole week of work to assure success. There are still a few more things WIP which will be released very soon to the site: we're not done yet, I'm not done yet.
