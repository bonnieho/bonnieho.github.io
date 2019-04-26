# bonnieho.github.io

Published portfolio site: [https://bonnieho.github.io](https://bonnieho.github.io)

## Overview

Well, when this task was originally assigned, there was a lot of confusion in class. I suppose it was in the way that the instructions were written, nevertheless, it was hard to determine whether we were supposed to re-create what the instructor and TAs had given us as an example or if we were supposed to use it as a basis for our own creation. Since it was unclear to me at the time, I simply made a pixel-perfect clone of the example shown to the class - colors, layout, and all. This was my third (and final) attempt from way back in 2017, however, I've recently been inspired to get in and fix it up properly, complete with new project cards.

(image of screenshots of the three pages, laid out horizontally)

- - - 

### Just th' facts...

As this assignment was early in our six-month course, at the point we were asked to complete this exercise, we had only just been introduced to html, css, and Bootstrap 3. Although I could make quick work of the markup and free-form CSS, with course content coming at us like water from a fire hose, I hadn't yet build up a reasonable level of confidence using the Bootstrap grid system yet. So, in the end, no Bootstrap styles were harmed in the making of these three portfolio pages.

#### What the portfolio hopes to showcase

I've been a front-end designer for a *long* time. I've also been a sys admin for IIS servers at various times throughout the years. The coding bootcamp course I completed was a welcomed bridge between those experiences. So, although I've got plenty of examples out there of front-end design work that I've done, the intent here is to bring focus to interactive programming projects that I am capable of (and those that I am most proud of!). 

#### Technical stuff - button pseudoclass rollovers

There isn't anything too fancy here, but in case you're into javascript-free rollovers, I've used CSS pseudoclasses for the hover and active states of the "Connect with me" icon links in the right side bar.

**The CSS:**

```
    section#sidebar .github {
        width: 62px;
        height: 62px;
        background: url("../images/icon_github.png") no-repeat;
        display: inline-block;
        margin-right: 4px;
    }

    section#sidebar .github:hover {
        background: url("../images/icon_github_over.png") no-repeat;
        margin-right: 4px;
    }

    section#sidebar .github:active {
        background: url("../images/icon_github_active.png") no-repeat;
        margin-right: 4px;
    }
```
*(Apologies here - I much prefer to use relative sizes based on the body's base font size in pixels whenever possible. Since I was trying to recreate a pixel-perfect replica of the class assignment example, however, I primarily stuck to pixels for the largest breakpoint at least.)*

**The HTML:** 

```
    <a href="https://bonnieho.github.io/" class="github">
        <span class="link-name">Connect with Bonnie on Git Hub</span>
    </a>
```

*Note that there is not an* `<img />` *container nested inside of the anchor tags. The link is configured for the exact dimensions of the image in the css, then that space is filled with the image as a background-image. The image appears to change on rollover as a different background-image is called on :hover, and then another on mousedown (active).*

*ALSO, I had originally left the link container "empty" (only the background images), but checking the page through a Web Accessibility tool pointed out that this is undesired for users of assistive technology, as there is nothing to describe the link itself to those visitors. Hence, I've included the* `<span>` *container with descriptive text inside of the link and then made the style of the corresponding class equal to* `display:none`. 


#### Technical stuff - "sticky" footer

Again, this is not rocket science, but if you've ever struggled with getting a footer element to "stick" to the bottom of a browser window, here's the **relevant** stuff that I did in the footer styles:

~~~
footer {
    . 
    .
    position: absolute;
    left: 0;
    bottom: 0;
}
~~~

*Note: I originally had a height of 100% on the body element, but this broke the absolute positioning of the footer, so it got commented out.*

- - - 

#### MVPs that I have left

- Rich Link Preview image + README screenshot
- favicon

- maybe add a modal response for submit button action?

WAVE accessibility recommendations:
    * contrast stuff

- - -


(c)2017-2019 __Bonnie Lynne Hoffman__ 

*toward the completion of The University of Texas at Austin Houston Coding Boot Camp Certificate - (June 2017 cohort)*
