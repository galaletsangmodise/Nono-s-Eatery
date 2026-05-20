Nono’s Eatery Project Report

Table of Contents: 

Project Overview 

Design Decisions  

Pages and Content 

Technical Approach 

File Structure 

Challenges Faced

Future Improvements 

Project Overview

Nono’s Eatery is a three-page restaurant website designed to bring a traditional South African eatery online. The goal was to build a clean, professional web presence that tells the story and identity of the restaurant authentically and showcases the menu with vivid food photography and warm descriptions. Makeing it easy for customers to find contact information and place orders. 

Design Decisions

1. Every page uses semantic elements (`<nav>`, `<section>`, `<footer>`).
2.  All three pages use the same navigation bar and footer structure. This creates consistency across the site and users always know where they are and how to move around. The nav links include an anchor (`index.html#menu`) that jumps directly to the menu section from any page.
3. Dishes are described using Setswana names alongside English ones and the language throughout is warm, story-driven and unapologetically South African. 
4. The homepage (`index.html`) was structured so that after the hero/welcome banner, the menu is immediately accessible. A hero call-to-action button (“View Our Menu”) anchors directly to the `#menu` section.
5. The contact page serves two distinct purposes of finding the restaurant and reaching out so it was split into two contact cards side by side. One card lists all the social and contact details. The other is a form for direct messages. 
6. On the About page, the restaurant’s core philosophy is presented as a `<blockquote>`. A blockquote signals that this is a notable, set apart statement.

Pages and Content

index.html - Homepage 
Contains: 
Navigation bar with links to all pages and a direct anchor to the menu 
Hero section with a welcome heading and tagline 
Menu section (`id="menu"`) displaying four dishes in a grid layout

about.html — About Us
Contains: 
Navigation bar
About section with the restaurants story
An image banner (`div.about-image-banner`) styled via CSS for visual impact 
Footer

contact.html - Contact The action page.
Contains: 
Navigation bar
How to Order section  
Two contact cardw
Footer

Technical Approach 

HTML structure each page follows the same structural pattern 

Page-specific content like </section> <footer> <!-- Shared footer --> </footer> </body> </html>. 

Navigation with anchor links the menu link on non-homepage pages uses `href="index.html#menu"`, it navigates to the homepage and then scrolls directly to the menu section. This is achieved by giving the menu section the id attribute `id="menu"`. 

Form Structure (contact.html) The contact form uses standard HTML5 form elements with the `required` attribute for basic client-side validation. 

All styling is handled by a single external `style.css` file linked in every page’s `<head>`. 

Flex/grid wrapper for the two contact cards.

Images are stored in an `/images/` folder and referenced via relative paths in the `src` attribute. Each image has a descriptive `alt` attribute written to be accessible.

File Structure 

nonos-eatery/ │

  ├── index.html Homepage with hero and menu
  
  ├── about.html Restaurant story  
  
  ├── contact.html  Contact info 
  
  ├── style.css  All styles  
  
  └── images/  

Challenges Faced 

Firstly making sure the website actually sounds and feels like Nono’s Eatery and not like a generic restaurant template. Getting the tone right in the menu descriptions and the About page took intentional effort. Cross-Page Navigation with anchors linking the menu nav item to `index.html#menu` from other pages (instead of just `#menu`) required understanding how anchor links work across separate HTML files. A plain `#menu` link from `about.html` would search for a menu section on the About page and find nothing.
Keeping three pages consistent, the navigation and footer have to be manually repeated across all three files. Any update to the nav (adding a new page, for example) means updating all three files.  
Contact page layout fitting two distinct sections (contact details + a form) on one page in a way that felt balanced and readable without it looking cluttered required careful thought about the layout and card structure. 

Future Improvements 

Backend for the contact form which is currently `action="#"` means the form doesn’t actually send anywhere. A future version would connect to a form service.
Online ordering flow, the “Place Order” button currently has no destination. A full ordering system with a cart and payment gateway would be the natural next step.
Responsive mobile design will add media queries to ensure the menu grid and contact cards stack cleanly on smaller screens. 
