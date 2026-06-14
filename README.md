# animal-soundbook

Animal soundbook is a simple website that serves as a visual cue learning aid for children. The website was designed with the intention to make learning animal names and animal sounds a little bit more enjoyable and fun. The app will also serve as an experiment to gauge the interest of children in learning.  

# Features 

The website features a board in a grid that contains images of animals, along with a fun text that defines the sound that the animal makes. At the bottom of the animal card, is a button to play the sound of the animal, so that kids can have an audio feedback to add to the learning experience. The typography of the website is reflected to be more subtle, yet playful, aimed towards children as the main audience. 

# Primary business goals of the website

Animal sounbook is not trying to reinvent the wheel, rather the goal is to take something that exists mainly in static form, and give it an interactive touch that is a bit more interesting than paper books. The website aims to draw in two groups of audiences:
1. Parents of children
2. Children

The home page serves as the primary point of the call to action, where engaging text attempts to draw in the audience to the call-to-action, which is clicking the play me! button and landing on the page where the users see the animal card grid. Drawing the interest of parents mean a likehood of the website being used for their children. When children tend to use the website on a considerable scale, the primary goal of the website has been considered to be fullfilled.

## As users, the following would be expected upon visiting the website:
- I see a pleasant layout with nice contrasting colors.
- I am able to easily find out with a short glance what the webiste is about, and what it can offer.
- Clicking on the let's play button will lead to exactly, or closely what has been described on the home page.


## Typography choices
Upon research, i have found that children are attracted towards bright colours like red, orange and yellow, which utlimately increases a child's attention to detail. Based on this i have decided to go with a sort of a sunburst color #FFD34E for the background of the Bootstrap cards. This color, i feel, contrasts nicely with the color of #FFF2D9, which is basically a cream white color. For the background color of the body, the color #F1C40F has been chosen. For the border of the cards, the color #6CB4EE has been applied for a subtle contrast between the background and the cards, giving a more tactile look to the cards. For the header the color burlywood has been utlized to serve as an element of seperation from the background. The blackfonts are easy to read with this color for header background.

I have sourced the color hex codes from here: [The 20 Best Kids Color Palettes with Hex Codes & AI Design Examples] (https://www.media.io/color-palette/kids-color-palette.html)



## Manual testing

**Expected: The page that displays the bootstrap grid with animal tiles should be responsive and have images that scale properly. The buttons to play the animal sounds should play the sound made by the animal**.

Test conducted: 
- Resize the browser window manually by clicking and dragging the window to different breakpoints, and inspect whether the grid properly displays the cards according to the column units specified for each of the columns. In addition, inspect whether the card images on the bootstrap grid scale properly in terms of width on different breakpoints by applying the same technique. 
- Play each of the animal sounds on the animal card grid by clicking the button and ensure that the sound is heard.

Testing result: 
- Upon first viewing the interactive soundbook page of the website, it has been found that the main section pops up above the header, which seems to be an issue with the bootstrap grid itself. 
- The bootstrap cards do display in a grid with the column layout specified with the classes, but appears to not fit properly within its' container. The primary issue is that the cards spill out of the container and the out of the row.
- The buttons don't have the level of interactivity as being proposed to the user. 

Fixes
- Applying margin to the top  of the section, along with applying a z-index value of 0 on the section in the page with the animal tile grid, and a z-index value of 4 on the navbar solved the issue of content overflow. 
- An audio element has been nested inside the h3 heading of the card body in the bootstrap card. The audio element was resized to fit inside the h3, and will serve as the means to play the sound of the animal in the animal tile grid. It was attempted to play the sounds with a small javascript snippet, but that proved to be out of the scope of the project due to the complexity of getting the script to play all the sounds of the animal, instead of just one. For this reason, the script snippet was removed from the bottom of the body, and the audio element was implemented in its place. The audio elements does the job nicely, and was not too difficult to set up. 
- The controls of the audio element has been hidden with a span nested inside the bootstrap card title, and changing the background color of the span to the background of the audio element, which is whitesmoke.

**Expected: The navbar should have nav links that are centered and positioned in the right place, as expected of most websites that users come across. Users are used to the main nav links used to navigate websites on the right side, and the main home link with the logo or wesbite brand to be on the left side, and spaced properly against the left. The navbar should be responsive with font sizes resizing according to the screen width, and collapse on mobile screen sizes in order to allow users to see the nav links by clicking on the burger menu. All links should appear on the navbar accross all pages.**

Testing result - On mobile screen sizes of 320px, it has been found that the navbar simply overflows to the top of it. The font sizes don't scale according to screen width, and the nav links are not spaced and placed accordingly. The main nav links are in the middle of the nav element instead of the right. The brand link is not spaced against the left. Clicking on the hamburger menu does not perform any action. Therefore, it is non functional on mobile screen sizes. The nav link for the signup page does not show up on the home page and the contact page. The nav links are too big on mobile and tablet screen sizes.

Fixes - Upon examining the pages, it has been found that the nav-link for the signup page was missing. Issue has been resolved by placing the respective link in the pages. The nav links have been vertically centered by applying the vertical-alignment property, and the main nav links have been moved to the right of the navbar by applying the align-items property. The navbar brand link has also been centered by using the vertical-alignment property as used for the nav links, and in addition, a margin of 40px has been applied to move the brand link away from the horizontal start axis of the navbar. The brand link being too close to the start axis was logged as being an issue of distraction for the user. The same applies for the nav links being in the center instead of the right. Font size of the nav links and the brand link up until the 768px breakpoint is too big, and has been reduced to 26px. Upon a closer look, it has been determined that the cdn links to bootstrap in the link tags on the head of all pages except the soundbook.html page were pointed to bootstrap version 5.3.3. This version of bootstrap causes issues when attempting to collapse the navbar. placing the cdn link to bootstrap 5.3.8 solved the issue of the navbar hamburger button not triggering the dropdown for the nav links on mobile screen sizes. The button now successfully triggers the drop down menu and shows the nav links.

**Expected: The images and text on the home page should resize and fit in their columns fluidly, so as to represent responsive design. This should be according to the respective breakpoints accross various devices. The images should have an aspect ratio similar or close to that of each other, so that they are able to be resized nicely.**

* Testing result: 

- Sizing of the images and their description text on the home page is garbled and does not represent the proper layout expected of responsive sizing on mobile screens. Font sizes do not resize accordingly to fit in their columns when the browser window is resized to smaller widths, making the text distracting to read, as well as obtrusive and oversized. 
- Font sizing is not uniform across different screen widths. 
- The first image next to the description text is too high and not too wide. This makes it look non-uniform as compared to the aspect ratio of the other image below on the third column. 
- There seems to be no indication as to whether the content of the columns belong within a particular boundary. This makes the text and image simply blend and mix into the background, which would be deemed as not being so accessible to the user in terms of visual clarity. 
- When the images scale down in size, they occupy the start of the vertical axis, which in turn gives the appearance of a gap existing on the bottom of the column. This makes the text look disproportionate as compared to the scaled down image on certain breakpoints.
- There is extra space on top of the columns for image descriptions on the home page, which further pushes the text down from the images.  

Fixes: 
- The first image of the column next to the description text has been changed to another image that has a aspect ratio more closely matching that of the second image. This has made the scaling more smoother and uniform.
- The default font size for the body, along with the navbar brand link and the nav links has been changed to 1.6rem for a more uniform sizing of the text in relation to the screen sizes. 
- The font size of the description paragraphs on the home page has been changed to 1em for more responsive sizing.
- A background color of #ffa9 has been applied to the row for a more subtle touch to the content of the row. A gap of 30px on the row seperates the content from each other, as well as a padding of 30px to the top and bottom and 10px on the left and right makes it look a bit better. There is now a clear distinction between the main background and the row.
- The columns of the row in the home page has been centered by applying the property and value align-content:center. This gives a more clean and consistent look to the content on laptop and desktop screen sizes, as well as negate the need for an excessive margin on top of the image description heading to push it down.
- On the breakpoint between 768 and 992px, the columns has been placed accordingly to line with the text by using the align-content property. On the fourth column, which is the column for the description text of the second image a margin of 90px has been added to push down the description text to be level with the image.  
- A margin of 20px to the top of both the description columns for the images on the home page has been removed from the .description-column style declaration. It is not applicable anymore, as the property row-gap does the work of spacing apart the columns on the row. At this point, the extra spacing needed to be removed. 

**Expected: The nav links should collapse into the hamburger menu at a particular breakpoint in order to prevent the nav links from leaning against the navbar brand link. The nav links collapse down from under the main brand link, so that the user can easily associate the website name with the content. The links are clearly visible with nice contrasting between the navbar background and the nav links.**
**Testing result**
- The collapse menu triggers at the wrong breakpoint, therefore making the links close in together at the medium breakpoint, and only triggers at 320px screen size.
- The white background of the navbar is not so nicely contrasted with the color of the nav links
- The nav links drop down from under the navabar brand link, but its stretched to the full width of its container #navbarSupportedContent, making the active class apply the border to the full width. This display is not desirable.
**Fixes**
- The nav element of all pages had a class of .navbar-expand-sm. This was the wrong class, making it trigger the navbar hamburger menu only at the small screen(320px) size. This has been changed to .navbar-expand-md to collapse at the 768px breakpoint.
- Width of the nav links have been reduced by setting the property and value width:fit-content. Background color of aliceblue has been applied to the #navbarSupportedContent container to contrast the nav links better for viewability.

**Expected: The call to action button on the home page should be resize accordingly when the mobile and tablet screen breakpoint has been triggered**
**Testing result**
- Button is same size as it is in the other breakpoints for larger screens. 
**fix**
- The font size of the button has been reduced to 20px to better fit the small viewport of mobile devices. The font size compliments readability due to the font family being applied globally.

**Expected: The footer links are positioned properly, centered on the middle of the footer. On mobile breakpoint, three main footer links deemed neccessary for the user are visible. On screen sizes bigger than 768px, the sign up link is displayed. The footer links all open their respective relevant links, such as, home opens home page, about opens about page, and so on.**

**Test conducted**
- Click all the links and verify whether the link navigates to the proper corresponding page.
- Inspect the footer and determine whether the href attributes of the footer links are correct.


**Testing result**
- The footer links are off-center and all links try to fit along the footer, which is not the desired outcome. They are also not properly visible on screen size of 320px for mobile, which makes it difficult to see the footer links. 
- The footer links all navigate to the wrong pages. None of them take the user to the correct page.

**Fix**
- The footer links have been centered vertically by using the property align-items:center, and horizontally by using the text-align property. The hierarchy of the links on the footer were not in a fashion that users can easily navigate through the website. 
- The hierarchy has been changed to be first Home, then About and at last Contact for the mobile breakpoint. On screen sizes larger than 768px, the sign up link shows up. On mobile screens, the display of the sign up link is hidden. 
- The href attribute of the footer links have been corrected to navigate to the proper links when the user clicks on them.
- The href attributes of the footer links all had absolute paths to the html documents. This is wrong, and can cause conflicts with page navigation on the deployed site. This has been rectified by ammending the href attribute to point to the relative paths of the documents.


**Expected: The description column on the about page should be readable on all screen widths and be sized accordingly with respect to the screen breakpoints**

**Testing result**
The about paragraph was found to be squashed in from top to bottom. Upon reviewing the page structure, it was found that the paragraph was contained in column of 6 units, which is not neccessary. An inline style was found applying margin to the top of the section. 

**Fixes** 
- The bootstrap column was unneccessarily divided into two columns, where it seemed evident that perhaps the second column was not meant to have any content. The column class was changed to .col-lg-12  from col-6 to take up the full width of a single column. As it is a description paragraph, one column is more suited to it. The column is now responsive, making it easier to read the text content. 
- An inline style applying margin to the top was moved to the main stylesheet, as there is no need to explicitly enforce higher specificity just to apply this style.


**Expected: The section with the Animal tile grid is responsive and contains the animal tiles within it without spilling over the boundaries of the section. The grid is centered and contains tiles of the appropriate dimensions in terms of height and width.**

**Test conducted**
- Resize the browser window and determine whether the bootstrap grid has a proper layout, in terms of the tiles displaying according to the column classes being applied, as well as responsively resizing according to the screen width. 
- Inspect the individual breakpoints for mobile, tablet, laptop and desktop screens with the dev tools of the browser to assure that the content of the grid is resized properly, in addition to ensuring that the grid is properly spaced and aligned along the body.

**Testing result**
The testing made it clear that the bootstrap grid was spilling its' content out of the container. Upon viewing the soundbook page, the entire container seemed to be out of place, as if it was forced to be positioned out of the normal position flow. Attempting to increase the width of the container resulted in it actually shrinking the content. It was clear there was a mess up either in the bootstrap grid, or the main container. 

**Fixes** 
- Upon inspection, it was found that there was an extra div in the bootstrap row that caused the bootstrap grid to break and display the cards properly. The div was removed and that resulted the grid containing the cards within the row, and not spilling out of it.
- The container class was used in the section element. Upon googling the issue, it was found out that it is not the best practice to apply the container class on a section, but to rather nest a div inside the section and apply the container class on it. Removing the container class from the section itself proved to be fruitful, as the grid right then displayed properly, placed along the center of the body. Placing the row inside of the container made the grid display exactly as the way it was meant to be displayed, clean with spacing. 


## Further fixes

- Many redundant styles, inlcuding media queries, were found on the main stylesheet. The styles had minimal, or no effect on the elements, or were duplications of media queries that could have been consolidated into one single media query line. These styles were removed

- The animal tile grid section section overflows on top of the navbar on the page to play the animal sounds. Setting a z-index property to the value of 3 solved the issue. Furthermore, this property was also found to be placed at the media query breakpoint of 992px for both the #main and .navbar element, when it was not required to be there at all. The property was moved to the .navbar style declaration as a global declaration for all the pages. There is absolutely no need for a media query declaration just to do this.

- The property and value align-self:center applied to the images on the home screen are redundant now, because of other properties present to align and space the content on particular breakpoints. It, along with the .description-column style declaration for the columns has been removed.

- A .col-6 style declaration was found in the stylesheet, but this class does not exist anymore. This redundant style declaration has been removed.

- The bootstrap row on the soundbook page has sharp edges that just does not seem to fit in with the view of the webpage. The borders have been rounded to look smoother and look more elegant. This overall affects the look of the page and seems better. The bootstrap row on the soundbook page has been given a custom class name of animal-tile-row, so as to not apply the style to all other pages across the website. On screen sizes up to 575px, a media query has been added to disable the border radius, as the display of the row is better without it, allowing the row to blend in with the background.

- An unused id of id="home" has been found on one of the footer links. This is not at all now neccessary, and therefore has been removed.

- The text for the a tag of the sign up page was missing from the tag on the footer across all pages. The text has been added to all the tags of the respective link. This was probably erased while ammending the href attributes of the links.

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