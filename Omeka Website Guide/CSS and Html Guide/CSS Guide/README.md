# CASPIANA CSS Editor Guide

In this guide I will include all the CSS I used to customize CASPIANA’s Omeka website. I will try to explain some of the formatting so that future research assistants can quickly edit or reformat aspects of the website. I am not super proficient in CSS so this should not be considered an exhaustive guide, but it may prove useful to people who have no CSS background whatsoever. 

To begin with you should refer to W3schools for general CSS syntax. In general, however, CSS involves specifying an object on the website, selecting it, and then editing by including some code in brackets {}. Depending on your browser, you can use Developers Tools to help find the location of different parts of the website. Right click on a page and look for the “Inspect” tab. Click on that and you should be able to explore the page’s CSS and HTML. 

The CSS I have included in the CSS Editor Plugin of the Omeka site is divided into different portions that customize the site for desktop, tablet, tablet landscape, mobile, and mobile landscape views. The first portion of the CSS code is for desktop and it applies to all versions below it, unless specifically changed for a mobile version. The way to target mobile version specifically is to use this code: 

@media all and (max-width:900px){

}

Here “max-width: “indicates the pixel width of a device and all CSS code should be inserted within the main brackets. Again, all code cascades down, so if you format font size for the Desktop version, it will automatically apply to all versions. Once you change that font size for the Tablet version, all versions below it will be affected, etc. 

The CSS code for the website is listed below. I will use a hashtag and the color orange to mark lines where I am writing comments. If you were to copy paste code from this document into the editor, do not copy anything that starts with a # or is in orange. 

Desktop Version (Also Tablet landscape version)
---

* The code below simply removes the underlines from hyperlinks. 

a:link {
text-decoration:none
}

# This removes the non-interactive map that is used for mobile versions of the website so that only the interactive version is included in the desktop version. 

img#Mobile-map {
position:absolute;
left:-1000px
}


# This increases the padding for the header and allows the header image to stand out a little more. 

header {
padding:30px
}

# This removes a small “Proudly powered by Omeka” citation in the bottom right of the footer. I include this in mobile versions to create a buffer for the footer, but on the desktop version the Davis Center Logo is sufficient. 

div#footer-content.center-div p {
display: none
}

# This just makes the footer have a grey background. 

footer {
background-color:#F8F8F8
}

# Simple pages in Omeka have some odd formatting in the top left that looks odd when you center the title. This removes that formatting. 

p#simple-pages-breadcrumbs {
display:none
}

# This targets the side bar on each Exhibit page. First, it gives it a grey background. Second, it center aligns the text. Third, it sets the font size. Fourth, it simply means that it takes up 20% of the page. 

nav#exhibit-pages {
background-color:#F8F8F8;
text-align:center;
font-size:17px;
width:20%
}

# This targets the content of each Exhibit page by making it left aligned and making it take up 75% of the page. This code and the code above are what format the overall look of Exhibit pages. 

#exhibit-blocks, .exhibits #content #primary {
float:left;
width:75%
}




# This sets the font size of the navigation links in the footer and makes their font “PT Sans”. 

nav {
font-size:16px;
font-family:'PT Sans'
}

# This sets the font size of the navigation links in the header and makes their font “PT Sans”. 

#primary-nav li {
font-size:16px;
font-family:'PT Sans'
}

# This sets the font size of paragraph text everywhere and makes their font “PT Serif”. 

p {
font-size:16px;
font-family:'PT Serif'
}

# This sets the font size of h1 text everywhere and makes their font “PT Sans”. 

h1 {
font-size:32px;
font-family:'PT Sans'
}

# This sets the font size of h2 text everywhere and makes their font “PT Sans”. 

h2 {
font-size:24px;
font-family:'PT Sans'
}

# This sets the font size of h3 text everywhere and makes their font “PT Sans”. 

h3 {
font-size:22px;
font-family:'PT Sans'
}

# This sets the font size of h4 text everywhere and makes their font “PT Sans”. 

h4 {
font-size:18px;
font-family:'PT Sans'
}
# This sets the font size of h5 text everywhere and makes their font “PT Sans”. 

h5 {
font-size:18px;
font-family:'PT Sans'
}

# This centers the title of every simple page. 

.simple-page h1 {
text-align:center
}




# Tablet Version (Vertical)

@media all and (max-width:1000px) {

# This brings the non-interactive map that is used for mobile versions of the website back so that only the non-interactive version is included in mobile versions. 

img#Mobile-map {
display:inline;
position:relative;
left:0
}

# This removes the interactive map that is used for the desktop versions of the website so that only the non-interactive version is included in mobile versions. 

img#Desktop-map {
position:absolute;
left:-1000px
}

# This sets the font size of h4 text for tablets and makes the font “PT Sans”. 

h4 {
font-size:16px;
font-family:'PT Sans'
}




# This reintroduces the small “Powered by Omeka” text in the bottom-left of the footer. This creates a better buffer for the end of the page.  

div#footer-content.center-div p {
font-size:6px
}

# This sets the font size of h1 text for tablets and makes the font “PT Sans”. 

h1 {
font-size:20px;
font-family:'PT Sans'
}

# This sets the font size of h3 text for tablet versions and makes its font “PT Sans”. 

h3 {
font-size:16px;
font-family:'PT Sans'
}

# This sets the font size of the navigation links in the header for tablets and makes their font “PT Sans”. 

#primary-nav li {
font-size:14px;
font-family:'PT Sans'
}

# This targets the side bar on each Exhibit page for tablet versions. First, it gives it a grey background. Second, it center aligns the text. Third, it sets the font size. Fourth, it simply means that it takes up 15% of the page

nav#exhibit-pages {
background-color:#F8F8F8;
text-align:center;
font-size:17px;
width:15%
}

# This targets the content of each Exhibit page for tablets by making it left aligned and making it take up 80% of the page. This code and the code above are what format the overall look of Exhibit pages. 

#exhibit-blocks, .exhibits #content #primary {
float:left;
display:inline;
width:80%
}
}
# Phone Version (Landscape)

@media all and (max-width:700px) {

# This targets the side bar on each Exhibit page for the landscape versions on phones (although after this code the sidebar takes up the whole screen instead). First, it gives it a grey background. Second, it makes the navigation links take up the entire screen on phones. Third, it center aligns the navigation text. 

nav#exhibit-pages {
background-color:#F8F8F8;
width:100%;
text-align:center
}

# This centers the website logo for phone (landscape) version. 

header div#site-title {
text-align:center
}

# This creates enough padding for the footer so the Davis Center logo is in line with text. 

footer {
padding:25px
}

# This targets the content of each Exhibit page for phones by making it take up 105% of the page (which is necessary to make things looked aligned with the navigation links). This code and the code above are what format the overall look of Exhibit pages. 

#exhibit-blocks, .exhibits #content #primary {
width:105%
}
}



# Phone Version (Vertical)

@media all and (max-width:640px) {

# This sets the font size of h4 text for phones (vertical) and makes the font “PT Sans”. 

h4 {
font-size:11px;
font-family:'PT Sans'
}
# This removes the small “Proudly powered by Omeka” citation in the bottom right of the footer. 

div#footer-content.center-div p {
display:none
}

# This creates enough padding for the footer so the Davis Center logo is in line with text. 

footer {
padding:15px
}

# This sets the font size of h1 text for phones (vertical) and makes the font “PT Sans”. 

h1 {
font-size:20px;
font-family:'PT Sans'
}

# This sets the font size of paragraph text for phones (vertical) and makes the font “PT Serif”. 

p {
font-size:12px;
font-family:'PT Serif'
}

# This sets the font size of the navigation links in the header for mobile (vertical) versions and makes their font “PT Sans”. 

#primary-nav li {
font-size:14px;
font-family:'PT Sans'
}
}
