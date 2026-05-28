# animal-soundbook

## Animal soundbook is a simple website that serves as a visual cue learning aid for children. The website was designed with the intention to make learning animal names and animal sounds a little bit more enjoyable and fun. The app will also serve as an experiment to gauge the interest of children in learning.  

# Features 

## The website features a board in a grid that contains images of animals, along with a fun text that defines the sound that the animal makes. At the bottom of the animal card, is a button to play the sound of the animal, so that kids can have an audio feedback to add to the learning experience. The typography of the website is reflected to be more subtle, yet playful, aimed towards children as the main audience. 

# Primary business goals of the website

## Animal sounbook is not trying to reinvent the wheel, rather the goal is to take something that exists mainly in static form, and give it an interactive touch that is a bit more interesting than paper books. The website aims to draw in two groups of audiences:
1. Parents of children
2. Children

## The home page serves as the primary point of the call to action, where engaging text attempts to draw in the audience to the call-to-action, which is clicking the play me! button and landing on the page where the users see the animal card grid. Drawing the interest of parents mean a likehood of the website being used for their children. When children tend to be using the website on a considerable scale, the primary goal of the website is fullfilled.

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

Upon first viewing the interactive soundbook page of the website, it has been found that the main section in the page is placed above the footer, which is a spacing issue.