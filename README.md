# animal-soundbook

Animal soundbook is a simple website that serves as a visual cue learning aid for children. The website was designed with the intention to make learning animal names and animal sounds a little bit more enjoyable and fun. The app will also serve as an experiment to gauge the interest of children in learning.  

# Features 

The website features a board in a grid that contains images of animals, along with a fun text that defines the sound that the animal makes. At the bottom of the animal card, is a button to play the sound of the animal, so that kids can have an audio feedback to add to the learning experience. The typography of the website is reflected to be more subtle, yet playful, aimed towards children as the main audience. 

# Primary business goals of the website

Animal sounbook is not trying to reinvent the wheel, rather the goal is to take something that exists mainly in static form, and give it an interactive touch that is a bit more interesting than paper books. The website aims to draw in two groups of audiences:
1. Parents of children
2. Children

The home page serves as the primary point of the call to action, where engaging text attempts to draw in the audience to the call-to-action, which is clicking the play me! button and landing on the page where the users see the animal card grid. Drawing the interest of parents mean a likehood of the website being used for their children. When children tend to be using the website on a considerable scale, the primary goal of the website is fullfilled.

## As users, the following would be expected upon visiting the website:
- I see a pleasant layout with nice contrasting colors.
- I am able to easily find out with a short glance what the webiste is about, and what it can offer.
- Clicking on the let's play button will lead to exactly, or closely what has been described on the home page.


## Typography choices
Upon research, i have found that children are attracted towards bright colours like red, orange and yellow, which utlimately increases a child's attention to detail. Based on this i have decided to go with a sort of a sunburst color #FFD34E for the background of the Bootstrap cards. This color, i feel, contrasts nicely with the color of #FFF2D9, which is basically a cream white color. For the background color of the body, the color #F1C40F has been chosen. For the border of the cards, the color #6CB4EE has been applied for a subtle contrast between the background and the cards, giving a more tactile look to the cards. For the header the color burlywood has been utlized to serve as an element of seperation from the background. The blackfonts are easy to read with this color for header background.

I have sourced the color hex codes from here: [The 20 Best Kids Color Palettes with Hex Codes & AI Design Examples] (https://www.media.io/color-palette/kids-color-palette.html)

## Initial issues faced

One of the bootstrap cards seem to have unequal heights based on the size of the images. There seems to be a single factor controlling the height of the images. The desirable outcome is for the images on the card to be of equal height irrespective of the breakpoint. 

Issue has been fixed by placing a media query at the 992px breakpoint and applying a minimum height of 200px to the particular card that had unequal height.

## Manual testing

* Expected: The page that displays the bootstrap grid with animal tiles should be responsive and have images that scale properly. The buttons to play the animal sounds should play the sound made by the animal.  

Testing result - Upon first viewing the interactive soundbook page of the website, it has been found that the main section pops up above the header, which is a spacing issue. The buttons don't have the level of interactivity as being proposed to the user. 

Fixes - Applying margin to the top  of the section, along with applying a z-index value of 0 on the section in the page with the animal tile grid, and a z-index value of 4 on the navbar solved the issue of content overflow. 

* Expected: The navbar should have nav links that are centered and positioned in the right place, as expected of most websites that users come across. Users are used to the main nav links used to navigate websites on the right side, and the main home link with the logo or wesbite brand to be on the left side, and spaced properly against the left. The navbar should be responsive with font sizes resizing according to the screen width, and collapse on mobile screen sizes in order to allow users to see the nav links by clicking on the burger menu. All links should appear on the navbar accross all pages.

Testing result - On mobile screen sizes of 320px, it has been found that the navbar simply overflows to the top of it. The font sizes don't scale according to screen width, and the nav links are not spaced and placed accordingly. The main nav links are in the middle of the nav element instead of the right. The brand link is not spaced against the left. Clicking on the hamburger menu does not perform any action. Therefore, it is non functional on mobile screen sizes. The nav link for the signup page does not show up on the home page and the contact page. 

Fixes - Upon examining the pages, it has been found that the nav-link for the signup page was missing. Issue has been resolved by placing the respective link in the pages. The nav links have been vertically centered by applying the vertical-alignment property, and the main nav links have been moved to the right of the navbar by applying the align-items property. The navbar brand link has also been centered by using the vertical-alignment property as used for the nav links, and in addition, a margin of 40px has been applied to move the brand link away from the horizontal start axis of the navbar. The brand link being too close to the start axis was logged as being an issue of distraction for the user. The same applies for the nav links being in the center instead of the right. 

* Problem 4 - Sizing of the images and their description text on the home page is garbled and does not represent the proper layout expected of responsive sizing on mobile screens. An issue with the Bootstrap grid.

Solution - Inspect the Bootstrap classes and ensure that they have been applied properly.

Fix - The problem has been fixed by changing the column classes to col-md-6 from col-6 on the bootstrap grid on the  home page. 

* Problem 5 - On the 768px breakpoint for tablet screens, the nav links appear closer together in relation to the navbar-brand home link. 

Solution - Resize the nav links, along with the home link, and apply proper spacing between them.

Fix - 

* Problem 6 - The footer links are not centered and positioned in the right place, and is not properly visible on screen size of 320px for mobile.

Solution - Resize the footer links, and position them to be on the center of the footer.

Fix - 

Problem 7 - The navbar does not collapse on mobile screen sizes. 

Solution - Examine the nav element and ensure that all classes to collapse the navbar on mobile screens has been properly applied. 

Fix - 

## How to view the project

Simply go to the link below to see the delpoyed site:
[Animal Soundbook] (https://anadil90.github.io/animal-soundbook/index.html)

## User stories:

![user story 1](./user%20stories/Screenshot%20from%202026-05-29%2001-20-33.png)

![user story 2](./user%20stories/Screenshot%20from%202026-05-29%2001-23-05.png)

![user story 3](./user%20stories/Screenshot%20from%202026-05-29%2001-24-52.png)
This user story was a could have, but could not be implemented due to the scope of the project. This is better suited for javascript, where interactivity is key. A workaround to that would have involved more time, particularly in sourcing actual proper sound files in the form of wavs.

![user story 4](./user%20stories/Screenshot%20from%202026-05-29%2003-28-51.png)


## Automatic testing

HTML validation: 

testing the pages showed that they were mostly clean, except for warning messages on the contact and signup pages.

### home page
![home page test](./testing/Screenshot%20from%202026-05-29%2003-12-44.png)

![about page test](./testing/Screenshot%20from%202026-05-29%2003-13-44.png)

![contact page test](./testing/Screenshot%20from%202026-05-29%2003-20-07.png)

![signup page test](./testing/Screenshot%20from%202026-05-29%2003-20-35.png)

## Lighthouse testing

![lighthouse test](./Lighthouse%20testing/Screenshot%20from%202026-05-29%2004-07-49.png)
The test revealed that a few things can be done to improve page load speed, but on the accessibility side, it seems to fear good.

## wireframes

The wireframe showed here initially was the designed being opted for. Thw wireframe helped to draw out the rough sketch in terms of what the website can look like. It was drawn by hand on a magnetic ink sketch board.
![wireframe](./wireframe/wireframe%20sketch.jpeg)

## known issues
There seems to be a bug on the contact page where the nav link for the sign up page doesen't show up on the home page,
but does show up when navigating to the about page. The issue could not be resolved and isolated. 

# collaboration
I am open to collaborate with you. Feel free to go to the repo and clone
![repo](https://github.com/Anadil90/animal-soundbook)