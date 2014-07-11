# Planate

pla•nate [**pley**-neyt]  
***adjective***  
having a flat surface.

Planate is a free theme for subverses on [WhoaVerse](http://whoaverse.com). The style is simplistic, clean, and modern. The theme can be customized *easily*! Here is a preview:

![Preview](http://i.imgur.com/PHPe21Q.png "Preview of theme installed on /v/Nurdoidz")

# How to Install

1. Go to `/v/SubverseName/about/edit`, where `SubverseName` is the name of your subverse.
2. Paste the CSS code inside the 'Custom stylesheet' text box ([minimize the code](http://cssminifier.com) if necessary).
3. Click 'Save' and watch as your subverse is transformed into something beautiful.

If you have any questions or concerns, [head over to /v/Planate](http://whoaverse.com/v/Planate) and we'll take care of you.

# Documentation

## Introduction

This documentation explains how to use the CSS code to customize it for a subverse. It is organized with customization in mind for end-users without headaches. If only color customization is desired, skip to 'Theme Colors and Customization.'

## Layout

The code is organized in ten categories:

![Layout](http://i.imgur.com/vTh4YP0.png)

1. Body
2. Header (red)
3. Sidebar (yellow)
4. Post feed (green)
5. Post page
6. Submit link page
7. Footer (blue)
8. Theme colors and customization
9. Transitions
10. Mobile

### Body

`Body` spans the entire page. Global values and uncategorized styles are organized in this category.

#### Fonts

The global font style is `Arial, sans-serif`. Some headings are styled with `"Segoe UI", Calibri, sans-serif`.

#### Hyperlinks

Most hyperlinks are underlined-on-hover. Exceptions usually occur for headings.

#### Voting Arrows

Voting arrows make up four sprites (each 18x19px) on one image:

![Sprite sheet](http://i.imgur.com/BDutAqr.png)

* Downvote: gray, x(0), y(0)
* Downvoted: blue, x(0), y(19)
* Upvote: gray, x(18), y(0)
* Upvoted: red, x(18), y(19)

#### Shadows

Shadows are applied to boxed-in elements, including: header bar, sidebar, link posts, etc. Unblurred to achieve a 3D, simplistic look.

#### Buttons

There are two different types of buttons. One with a shadow inset and one with a shadow outset. 

### Header

![Header](http://i.imgur.com/o394c2G.png)

* **Red:** top header bar
* **Blue:** subverse name
* **Green:** tab menu
* **Orange:** account information

#### Top Header Bar

The top header bar has a 50% opacity when inactive. It transitions to 100% on-hover. Because of the complications of the bar, all of the colors are locked with the exception of on-hover hyperlinks.

#### Main Header Bar

The main header bar makes up the rest of the header, excluding the banner image. A 50-pixel white background with a shadow is drawn 150 pixels from the top of the page. The logo, subverse name, tab menu, and account information positions are placed accordingly.

Each element has a sort of fade effects, with the account information having a complete invisible-to-opaque transition.

### Sidebar

The sidebar is 300px wide and floats on the right side of the page. There are two custom-functions added to the sidebar.

#### InfoBox

![InfoBox](http://i.imgur.com/f9SvmFw.png)

The InfoBox is a box that has a header and content. It has a faint border and shadow. The box is created by combining a heading 2 style with an immediate block quote:

    ## About Planate

    > Planate is a CSS theme I created to be used by subverses.

#### Custom Button

A custom button can be created by combining a heading 5 style with an immediate hyperlink:

    #####[Get Planate 1.3 now!](https://github.com/Nurdoidz/Planate-WhoaVerse)

This feature is rarely used but has its purpose in some applications.

#### Message the Moderators

This hyperlink has been changed into a button for easy accessibility.

### Post Feed

The post feed is the list of links that makes up most of the page.

#### Expand Icon

The expand icon make up two sprites (each 26x26px) on one image:

![Sprite sheet](http://i.imgur.com/BDutAqr.png)

* Default: x(36), y(0)
* On-hover: x(36), y(26)

The other two icons will be used when the features support it.

### Post Page

The post page is the page with a description of the post link and the comments.

#### Comments

Child comments have alternating backgrounds to make threaded comments easier to follow.

### Submit Link Page

The submit link page is the page that is accessed by navigating to 'start a discussion' and 'share a link' menu options on the header bar.

### Footer

The footer is the block of text on the bottom of the page. Additional theme branding has been added to the footer and it is not recommended to remove this branding.

### Transitions

Fade transitions exist to make the theme slick. Opacity, text color, and border color on some elements are currently in play.

### Mobile

The mobile category organizes all of the code used when the mobile view of the website is used (width<800px). Changes include layout adjustments, disabling of transitions, font size adjustments, and larger hyperlinks.

## Theme Colors and Customization

There are seven main elements to customize:

* Header image
* Background colors
* Border colors
* Hyperlink colors
* Text colors
* Button colors
* Name of subscribers

Each section is heavily annotated to explain which attribute changes what element in the theme. They are categorized to match the main categories in the rest of the code.

To save space, some elements have been grouped together. To change elements individually, each element has been put on its own line so it can be manually changed.

### Header Image

Used to change the banner image of the theme in the header. 

    #header {background: url(http://i.imgur.com/IVAIgeY.png) no-repeat fixed 50% 0;}

There are four values to change:

* `url(IMAGEURL)`, the URL location of the image.
* `no-repeat`, how the banner image is repeated. Possible alternatives: `repeat-x` or `repeat-y`.
* `fixed`, how the banner image scrolls with the page. To make the image scroll normally, delete this.
* `50% 0`, the position of the banner image. `50%` indicates the centering of the image horizontally.

### Changing Individual Values for Grouped Elements

    /* Hyperlink colors */
    .link a,
    .link .title.may-blank,
    .domain a:hover,
    .side a {color: #48E}

In this example, we have four elements grouped together with a `{color: #48E;}` attribute. To change a single element individually, the element must be taken *out* of the list and then tagged with an attribute. Let's use `.domain a:hover,` as an example. First, remove the comma:

    /* Hyperlink colors */
    .link a,
    .link .title.may-blank,
    .domain a:hover
    .side a {color: #48E}

Then, take the line *out* of the group by placing it above (or below) the group:

    /* Hyperlink colors */
    .domain a:hover

    .link a,
    .link .title.may-blank,
    .side a {color: #48E}

Then, assign an individual attribute to the element:

    /* Hyperlink colors */
    .domain a:hover {color: #FFF;}

    .link a,
    .link .title.may-blank,
    .side a {color: #48E}

#### Background Colors

Customization of the background colors of various elements, ranging from the body to the sidebar to block quotes.

#### Border Colors

Customization of the border colors of elements, ranging from post links to comments to code blocks.

#### Hyperlink Colors

Customization of the colors of hyperlinks.

#### Text Colors

Customization of the colors of text on all elements with text.

#### Button Colors

Customization of the colors (including on-hover) of all buttons.

#### Name of Subscribers

Customization of the names given to subscribers on the sidebar. There are two names with two default strings: subscribers with default `"planaters"` and users online with default `"users online"`.
