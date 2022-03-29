# Frontend Mentor - Equalizer landing page solution

This is a solution to the [Equalizer landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/equalizer-landing-page-7VJ4gp3DE). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](screenshots/mobile.png.jpg)
![](screenshots/tablet.png.jpg)
![](screenshots/desktop.png.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://fem-equalizer-landing-page.vercel.app/](https://fem-equalizer-landing-page.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- BEM
- SASS
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

I learned a lot building this challenge and managed to bring together a lot of different things I have been working on improving:

- Positioning - I have a greater understanding of when to use relative and absolute positioning and I also learned a great tip on how to find an elements nearest relatively positioned ancestor which I used to debug an issue I was having at one point. [Link to the article with this tip](https://css-irl.info/finding-an-elements-nearest-relative-positioned-ancestor/)

- SVG - I haven’t worked a great deal with SVGs and was having an issue changing the color of the social media links on the hover state. I had initially added the SVG icons as img tags but this wasn't allowing me to change the fill color. I quickly realized that I needed to add the SVGs directly to the HTML itself and then came across a great stack overflow thread that gave me a simple solution on how to change the fill color on hover. By adding the code below to the svg tag I could then change the color property via the CSS as I had been trying to do before without success. [Here's the link to the thread](https://stackoverflow.com/questions/22252472/how-to-change-the-color-of-an-svg-element):

```html
<path>fill="currentColor"</path>
```

- Accessibility - I realized at a point that my social media links weren't really accessible. After a bit of research, I was able to make them accessible for screen readers by hiding the icon and replacing it with text that the screen reader would read out instead allowing those using screen readers to know where these links would take them.

- Background images - In this challenge I learned how to offset background images. To offset the background pattern at the top right of the screen on tablet devices I used the following code:

```css
body {
  background-image: url(../assets/bg-pattern-1.svg),
    url(../assets/bg-main-tablet.png);
  background-position: top -30px right -30px, top -220px right -100px;
  background-size: 266px 400px, auto;
}
```

I have added 2 background images to the body here, the pattern at the top right of the screen is 'bg-pattern-1.svg', so as the first url present in the background-image property, it will also be the first set of values in the background-position property that will apply to it. In order to offset this image I had to use a combination of keywords and negative values. The keyword immediately before the negative value is where the image will be offset FROM, so 'top -30px' means it will be pulled up 30px from the top of the page. And 'right -30px' means the image will be pulled 30px away from the right edge. There is a small bit about this in the 'Backgrounds' section of web.dev's 'Learn CSS!' course [https://web.dev/learn/css/backgrounds/](https://web.dev/learn/css/backgrounds/).

- clamp() - I used this for the first time in this project. Took a bit of research to try to understand it (I will link a couple of good resources I used for this below in my Useful Resources section). Looking forward to implementing this useful CSS function more in future projects.

- SASS - I started using mixins (and functions within those) during this challenge to help with making media queries easier to write. Saw this technique in a course by Jonas Schmedtmann that I have been doing. I also broke my SASS down into partials for this challenge for the first time.

### Continued development

Areas that I would like to focus on in future projects are:

- Accessibility - Ideally I would like to start thinking about this earlier in my build process, rather than at the end.

- Tailwind.css - I'm quite keen to give this framework a try soon.

- NPM - I haven't used this yet in any FEM challenges, but would like to so that I can get used to using it.

### Useful resources

- [Jonas Schmedtmann Advanced CSS And SASS Course](https://www.udemy.com/course/advanced-css-and-sass/) - I highly recommend Jonas' courses, very in depth, but not overwhelmingly so.
- [https://a11y-101.com/](https://a11y-101.com/) - I found this website very helpful to understand how to make your website more accessible. Especially good at explaining why or why not to do things certain way.
- [https://web.dev/min-max-clamp/](https://web.dev/min-max-clamp/) - A great article that helped me to understand the CSS clamp() Function (and min() and max() functions).
- [https://ishadeed.com/article/css-min-max-clamp/](https://ishadeed.com/article/css-min-max-clamp/) - Another article about CSS clamp() Function (and min() and max() functions) that I used to understand how it works.

## Author

- Frontend Mentor - [@claire-ca](https://www.frontendmentor.io/profile/claire-ca)
