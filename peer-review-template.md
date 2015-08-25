Development guide

Checkpoint 1: We meet needs using HTML

General HTML principles
There are a few principles which we follow for all HTML we produce. The peer review will check that:

1. HTML5 Document type is used and <html> tag includes an appropriate ‘lang’ attribute2 – typically en-gb
2. HTML validates3
3. The <title> tag is present and follows pattern {h1} | The National Archives
4. HTML is indented to illustrate its structure
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments




HTML5 syntax style
HTML5 has considerably relaxed the syntax rules for HTML. To ensure consistency across projects we have agreed upon a house syntax style. The peer review will check that:

1. Optional tags are used
2. All tags are closed, even where HTML5 might allow them not to be
3. Full attribute syntax is used and all attributes are quoted
4. All tag names and attributes are in lower case
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



There is an appropriate HTML outline
HTML outlines are an important means for navigating pages with assistive technologies. All digital services we produce should have a logical document outline with one <h1> tag, and each subsequent <h*> 'sectioning' the content below it. Because the HTML5 outlining algorithm is not yet implemented in any browsers, we do not rely on HTML5 sectioning elements for outlines.

The peer review will check that:

1. The HTML outline is logical and based on an appropriate <h*> structure
2. All content appears in the correct part of the outline
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments




Appropriate semantics are used
We use HTML elements for their intended purpose, ensuring valid semantics4 wherever possible. We do use HTML5 sectioning element semantics (<section>, <article>, <nav>, <aside>), but do so with care and avoid using them for document outlining (the HTML5 outline5 algorithm is not yet implemented in any user agents).

We use WAI-ARIA landmark roles (application, banner, complementary, contentinfo, form, main, navigation, search) and a traditional document outline for structuring documents. The peer review will check that:

1. There should be one <main> element 
2. HTML5 sectioning elements are used for semantics not structure
3. HTML5 sectioning elements are not over used in place of <div> elements
4. All relevant WAI-ARIA landmarks have been applied
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



HTML is ordered to support user needs
Navigation will typically be before primary content, and secondary content after primary. The peer review will check that:

1. The tab order fits the user goals
2. In-page navigation is facilitated with 'skip to content' and 'back to top' links where appropriate
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Forms
We ensure our forms are accessible6, usable and make best use of HTML5 and ARIA semantics. The peer review will check that:

1. Forms are fully accessible via keyboard alone
2. Forms are logically organised
3. Instructions (such as 'required' fields) and cues are clearly identified to users
4. Where appropriate, <fieldset> is used to group related inputs and <legend> is used to describe these groupings
5. Form elements are appropriately labelled, with labels having a 'for' attribute linking them to the corresponding input (we do not nest inputs in label elements)
6. Appropriate use is made of HTML5 form semantics (i.e. <input type="tel" />) so that user agents can assist users with an appropriate input mechanism
7. Good use is made of appropriate ARIA landmark roles (i.e. <form role="search"><input type="search" /></form>)
8. HTML5 form validation is used, supported by JavaScript validation for older browsers. This is covered in the JavaScript section of this document
9. Error messages are clearly visible and associated (both visually and within the DOM) to the corresponding input
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Tables
All tabular data is placed in HTML <table> elements. We do not use tables for layout and do not repurpose other elements to recreate table-like representations of data. WebAIM provide guidance on ensuring tables are accessible7

The peer review will check that:	

1. All tabular data is in <table> elements
2. A brief descriptive <caption> is provided for tables
3. Table headings are provided in <th> elements with an appropriate scope attribute
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



SVGs are accessible
Where appropriate images should be delivered in SVG format since this offers two significant accessibility benefits: the scalability of the image allows users with less than 20/20 vision to enjoy crisp images when zoomed, and; the inclusion of links within the SVG will allow for keyboard navigation by default. 

Guidance for using SVG includes: 

1. Use inline SVG where possible
2. Provide a title for the SVG in <title> tags and a description within <desc> tags
3. Use the <text> tag for any text to appear in the SVG
4. Use <a> tags for links within the SVG
5. Provide an ARIA role for the SVG
6. Provide a non-SVG alternative. If the SVG is purely graphical, the <title> and <desc> tags may suffice. If the SVG is interactive, an HTML alternative should be considered

Related resources are:

1. Tips for creating accessible SVG, by Leonie Watson http://www.sitepoint.com/tips-accessible-svg/ 

Where SVGs are used, they are used accessibly
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



There is good use of appropriate ARIA roles to support native semantics
While HTML5 provides a range of new semantic elements which are recognised by newer browsers, there is poor support (even in newer browsers) when it comes to reporting these elements to the Accessibility API. This, and the lack of semantics when these elements are polyfilled with JavaScript, makes ARIA an important tool. The HTML5 spec was updated in mid-2014 to indicate compatibility between elements and ARIA roles.

Related resources are: 

1. W3C introduction to ARIA http://www.w3.org/WAI/intro/aria 
2. ARIA authoring guidance http://www.w3.org/TR/wai-aria-practices/
3. WCAG 2.0 Principle 4 http://www.w3.org/TR/WCAG20/#robust 

ARIA roles are provided to support native semantics
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Checkpoint 2: Enhance with CSS

General CSS principles
There are a number of principles which we adopt for all CSS. The peer review will check that:

1. CSS is valid
2. All CSS is placed in external stylesheets
3. Relative units are used where possible
4. ID and class names reflect the purpose of the element in question
5. !important is avoided unless absolutely necessary (which is almost never)
6. CSS and SASS is indented to reflect the hierarchy of rules
7. Styles targeting older IE are placed in IE specific stylesheets that are included using conditional comments
8. Hacks for other browsers are placed in the 'shame.css' file
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



User focus is clearly visible
It is important to ensure interactive elements have a distinct visual appearance when activated. The peer review will check that:

All interactive elements have a clearly differentiated visual appearance when they have focus (this can typically be achieved using :focus) 
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Mobile first responsive design
We adopt a mobile-first approach which includes:

* Beginning from the premise that all content will be available to all users regardless of their screen size, unless there is a clear justification for doing otherwise
* Seeking to avoid duplicating HTML for display at different resolutions
* Recognising that there is no correlation between a user's screen resolution, network speed, device capability or processing power
* Fixing the viewport in older IE, rather than polyfilling media queries

The peer review will check that:

1. A mobile-first approach has been taken when applying media queries
2. We have developed in a way that accommodates devices which have low processing power and/or a slow network
3. The viewport is fixed in older IE
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments


Developer’s satisfaction 
1
2
3
4
5

CSS formatting standards
To ensure consistency across developers and assist with the maintainability of our code base we adopt a number of general CSS code formatting standards. The peer review will check that:

1. Code blocks have consistent indentation to reflect their hierarchy
2. Rules are separated with new lines
3. All rules are closed with a semicolon
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



CSS structure
CSS is structured to reflect a mobile-first approach. Each stylesheet begins with universal rules outside of a media query block. The peer review will check that:

1. @media rules are introduced sequentially, from smallest to largest
2. Overly specific queries that are difficult to test are avoided - i.e. @media tv and (min-width: 700px) and (max-width: 960px) and (orientation: landscape) { ... }
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Print CSS
We need to ensure we have accounted for users printing our content. While modern browsers provide a facility to emulate and debug print from within Developer Tools, we have encountered issues where IE prints differently to other browsers. The peer review will check that:

1. The printed page is well formatted, with legible content
2. The printed page does not include unnecessary components like decorative images and form elements.
3. The printed page includes full hyperlink destinations (appending our domain where they are relative)
4. Print styles are contained within in a @media = print block
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Checkpoint 3: Enhance with JavaScript

General JavaScript principles
There are a few principles which we follow for all JavaScript development. The peer review will check that:

1. JavaScript is well commented to aid maintainability
2. JavaScript is well formatted with consistent indentation
3. JavaScript does not cause any errors (including tests across older IE which do not support ECMAScript 5)
4. JavaScript is externalised into .js files. We do not place JavaScript in <script> tags or use native8 inline event handling (i.e. <a href="#" onclick="triggerAlert('Bad practice!'); return false;">Joe</a>
5. JavaScript is minified and concatenated where possible
6. JavaScript dependent elements are created with JavaScript. For example, if a <button> is used to perform a JavaScript action only, that button should be created with JavaScript
7. Server-side processing is used to ensure JavaScript is loaded only where needed
Are these checks relevant to this specific project? (If not, provide a comment and proceed to next item)

Developer(s) comments



Reviewer comments



Please speak to the Lead Front-end Developer if you need guidance on meeting any of these requirements.

jQuery or AngularJS are used for DOM abstraction
jQuery provides an excellent means of managing the complexity of DOM manipulation across browsers and devices. Attempting to manipulate the DOM without jQuery needlessly exposes us to a large number of cross-browser bugs and inconsistencies.

We therefore use only jQuery or similarly 'battle tested' framework (such as AngularJS) for managing interaction with the DOM.

jQueryUI is the primary source for custom widgets
It is essential that we consider the implications for users of assistive technologies when reviewing third-party plugins that provide non-standard user interface elements. This will include:

* Ensuring that suitable ARIA role and state management is provided
* Ensuring the plug-in does not make the DOM inaccessible (the overwhelming majority of assistive technology users are likely to have JavaScript enabled)
* We should not use plug-ins that do not provide suitable ARIA role and state management, unless they are available for open source contribution and we have the skills and resources to extend them in line with the WAI-ARIA authoring practices9.

For this reason, jQueryUI presents a good tool as its authors have worked hard to include the necessary ARIA role and state management in the library components. Nonetheless, we should test the accessibility of custom widgets before they are used.

JavaScript form validation
We provide JavaScript validation for user agents that do not support HTML5.

When working outside of .NET MVC:

* jQuery validate or AngularJS is used to provide client-side validation
* When using jQuery validate, feature detection is used to determine the need for JavaScript validation and it is applied only when necessary
* In all cases there is appropriate server-side validation in place

When working with .NET MVC: the MVC framework provides mechanisms to manage client- and server-side validation in tandem. When working with .NET MVC it is important that we rely upon these since it will be substantially easier to implement and maintain. A Systems Architect or a Senior Developer can advise on a suitable approach when working with .NET.

Our JavaScript library is used for common patterns
We have a library of common utilities that cover a range of common UI patterns used across our digital services. The peer review will check that:

* Where possible, we have made use of tna-definitions.js, tna-bindings.js, and tna-run-on-page-load.js rather than reinventing code that already exists.
* Where appropriate, we have packaged any new patterns into reusable components that are included in tna-definitions.js

Checkpoint 5: pre-release checks
Release version is WCAG 2.0 compliant at AA
The peer review will:

1. Check compliance with the Web Content Accessibility Guidelines (WCAG 2.0) using the W3C Quick Reference10 
2. Ensure the site remains accessible in the event that JavaScript and CSS are not available
3. Reviewing ‘Alphabet of Accessibility Issues’11 to consider how the implementation will meet the needs of personas described.

Is the release version:
1. WCAG compliant at AA, including appropriate use and management of ARIA roles and states
2. Accessible and usable without JavaScript and/or CSS

Developer(s) comments



Reviewer comments


Developer’s satisfaction 
1
2
3
4
5

Testing user goals across browsers, devices and contexts
The service should be tested on:

1. all supported desktop browsers (the current list is available from Webmaster) 
2. on a representative range of touch screen devices. 
3. a slow network connection (there are developer tools to assist with this)
4. [Where appropriate] in the Reading Rooms and on IE within the IN domain

While issues remain, iterate.

Is the site/application usable across browsers, devices and contexts

Developer(s) comments



Reviewer comments


Developer’s satisfaction
1
2
3
4
5

Lessons learned
Everything we build provides opportunities to for improvement to our processes and approach. By documenting the lessons learned and considering their implications for this development guide, we can understand the root cause of any problems as well as any opportunities for improvement.
Questions to consider
* What worked well either for this project or for the team?
* What didn't work well?
* What surprises did the team have to deal with?
* What would you do differently if given the chance to begin this project again
Key lessons

Having considered these questions, what are the key lessons to take forward for future projects?



Revision history

Date
Changes applied
Version 1.0
Review before being added to Objective
Version 1.1
Addition of ‘Alphabet of Accessibility Issues’ to the ‘Ensuring our HTML and CSS is WCAG 2.0 compliant at AA’ section
Version 1.2
Addition of SVG section providing guidance on ensuring SVG usage is accessible
Version 1.3
Changes to content and processes in order to make this a more usable tool for Designer/Developers. This included: removing redundancy (there is now only one check for WCAG2.0 compliance, rather than three); removing sections that are more related to design than development (like the ‘We know what we’re building’ section); a number of editorial changes to reflect the new approach which requires formal testing only at the end of the process.
Version 1.4
Added need for <html> tag to have an appropriate lang attribute. Added link to the improved (but still experimental) W3C validation tool.
Updated section on activatable elements.
Version 1.5
Updating section on using jQuery UI to provide link to W3C guidance on WAI-ARIA authoring
Version 1.6
Changed font & line spacing (MC)
Version 1.7
Updates to several sections following Design Team review on 15 April.
Version 1.8
Reviewed in response to changes to the Digital by Default Service Standard. Minor amendment made to the ‘lessons learned’ process to make it more streamlined. 

1 Whether employees of The National Archives, contractors or suppliers
2 In recent years there has been a reduction in the use of ‘lang’ but it provides a number of accessibility and usability advantages
3 W3C validation tools include http://validator.w3.org/ or the newer, but still experimental http://validator.w3.org/nu/ 
4 W3C element semantics http://www.w3.org/html/wg/drafts/html/master/semantics.html#semantics 
5 HTML5 outlines http://html5doctor.com/outlines/ 
6 WebAIM guide to creating accessible forms http://webaim.org/techniques/forms/ 
7 http://webaim.org/techniques/tables/data 
8 This does not apply to the use of AngularJS bindings and directives
9 The W3C authoring guidelines can be found at: http://rawgit.com/w3c/aria-in-html/master/index.html 
10 http://www.w3.org/WAI/WCAG20/quickref/Overview.php 
11 https://the-pastry-box-project.net/anne-gibson/2014-July-31 



