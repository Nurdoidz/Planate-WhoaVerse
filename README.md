# Planate

pla•nate [**pley**-neyt]  
***adjective***  
having a flat surface.

Planate is a free theme for subverses on [WhoaVerse](http://whoaverse.com). The style is simplistic, clean, and modern. The theme can be customized *easily* with colors! Here is a preview:

![Preview](http://i.imgur.com/WokywTI.png "Preview of theme installed on /v/Nurdoidz")

# How to Install

1. Go to /v/SubverseName/about/edit, where 'SubverseName' is the name of your subverse.
2. Paste the CSS code inside the 'Custom stylesheet' text box ([minimize the code](http://cssminifier.com) if necessary).
3. Click 'Save' and watch as your subverse is transformed into something beautiful.

If you have any questions or concerns, [head over to /v/Planate](http://whoaverse.com/v/Planate) and we'll take care of you.

# Documentation

## Quick-Customize Colors

The theme colors can be customized easily by editing the code in the "Theme colors and customization" section in the CSS file. There are five elements to customize: "Header image", "Background colors", "Notification/information box color", "Link colors", and "Button colors".

**Warning:** A fail-safe has not yet been implemented, so it is imperative not to delete any values here (instead, change them!).

### HEADER IMAGE

**Description:** Changes the header image.

**Code:**

    #header {
        background: url(http://i.imgur.com/IVAIgeY.png) no-repeat fixed 50% 0;
    }

**What to Edit**

To change the header image, edit the URL location of `url(http://i.imgur.com/IVAIgeY.png)` to the desired image's location. Delete `fixed` if it is undesirable for the image to remain static while scrolling.

### BACKGROUND COLORS

**Description:** Changes the main background colors.

**Code:**

    /* Outer (darker) */
    body,#sr-header-area,#header-bottom-right 
        {background-color: #EEE;}
    
    /* Boxes (lighter) */
    .side,.link,.commentarea .sitetable,.comment .expand:hover,.tabmenu,.well,#header:after
        {background-color: #FFF;}


**What to Edit**

To change the background colors, edit the values for each `background-color:`identifier. The 'Outer' determines the color of the entire page's background. The 'Boxes' determines the color of the post boxes, comments, sidebar and header bar.

### NOTIFICATION/INFORMATION BOX COLOR

**Description:** Changes the color of table headers.

**Code:**

    .alert-info,.info th,thead>tr>td.info,/* ... */.table>tfoot>tr.info>th {
        background-color: #48E;
        border: 0;
        border-radius: 0;
    }

**What to Edit**

Tables are not common but they exist. To change the background color of the header cells, edit the values for the `background-color:` identifier.

### LINK COLORS

**Description:** Changes the color of most hyperlinks.

**Code:**

    .link a,a,.link .title.may-blank,/* ... */#header-bottom-right a:hover
        {color: #48E;}
        
        /* On-hover */
        a:hover,.link a:hover,.link .title.may-blank:hover 
            {color: #59F;}

**What to Edit**

To change the color of most hyperlinks, edit the values for the `color:` identifiers.

### BUTTON COLORS

**Description:** Changes the color of buttons.

**Code:**

    .btn-default,.btn-whoaverse,.btn-whoaverse-default,/* ... */.titlebox h5 a {
        color: #FFF !important;
        background-color: #48E;
    }
        /* On-hover */
        .btn-default:hover,.btn-whoaverse:hover,/* ... */.titlebox h5 a:hover
            {background-color: #59F;}

**What to Edit**

There are three values to change: (1) the text color of the button, (2) the color of the button, and (3) the color of the button when hovered over by the mouse cursor. To change each value, edit:

1. `color: #FFF`
2. `background-color: #48E;`
3. `background-color: #59F;`

It's important not to remove `!important` from the first value.
