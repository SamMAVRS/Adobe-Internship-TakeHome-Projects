# Adobe Internship Take-Home Projects

## Introduction
As a requirement for whether or not I would be considered for an Adobe Internship, I was tasked with creating the three websites I am showcasing here. Each project had a specific set of parameters in mind but in terms of creativity, I was allowed to flex however which way I liked within the time constraints.<br/><br/>
So of course I was going to have a little fun with it.
<br/>
[Project One – Personal Website](#project-one--personal-website)<br/>
[Project Two – Blog Website](#project-two--blog-website)<br/>
[Project Three – Business Website](#project-three--business-website)
<br/><br/><br/>

## Project Parameters and Purpose
The projects were to gauge my understanding of web development; specifically with JavaScript, HTML, and CSS. This was in partnership with the bootcamp, General Assembly. All code had to be imbedded into a single HTML file and then uploaded to the G.A. servers. All three projects were simple one page websites. The only changes I made to the showcase for Github was to include a public folder with the image assets I used, and the G.A. servers didn’t allow the “+” and “%” symbol to be uploaded onto their servers.
<br/><br/>
I have included a preview image of the final product for each project as reference.
<br/><br/><br/><br/><br/><br/>

## Project One – Personal Website
[Personal Website Index](./P1__Personal_Website/index.html)<br/>
[Personal Website Preview](./P1__Personal_Website/PersonalWebsitePreview.png)

### <ins>Goal:</ins>
Build a personal website. Simulate a contact form. Button press opens a modal.
<br/><br/>

### <ins>Post-Mortem:</ins>
I went into this project with the idea of an elegant Pikachu. Everything had to reflect something that a top hat wearing person that drinks tea at “Tea Time” would love. Everything from the choice of a slim font to a dark background like something from an art gallery. The modal was to represent a successful send receipt for the user if this was for an email or other type of form. This works on a one page site but if the backend was something I had to consider, for security reasons, I would have gone another route. One that involved cookies and limiters to combat bot spamming.
<br/><br/>

### <ins>NOTE:</ins>
The handler for user input was my workaround to the inability to use a “+” and “%” constraint. The solution is inspired by a Linked-List.
<br/>

```javascript
    let count = 0;

    function handleMessage() {
        if (inputValue.value.length === 0) {

            if (count === 0) {
                count = 1;
                btn.innerHTML = "TYPE A MESSAGE";
                return count;
            }

            if (count === 1) {
                count = 2;
                btn.innerHTML = "TYPE THE THING";
                return count;
            }

            if (count === 2) {
                count = 3;
                btn.innerHTML = "THE THING IS EMPTY";
                return count;
            }

            if (count === 3) {
                count = 4;
                btn.innerHTML = "NEED TO DO THE THING";
                return count;
            }

            if (count > 3) {
                btn.innerHTML = "ok then...";
            }
            count = 5;
            return count;
        }



        if (inputValue.value.length > 0) {
            modalBox.className = 'modal__shown';

            // RESET
            count = 0;
            btn.innerHTML = 'PRESS ME';
            inputValue.value = '';
        }
        return;
    }
```
<br/><br/><br/><br/><br/><br/>

## Project Two – Blog Website
[Blog Website Index](./P2__Blog_theme/index.html)<br/>
[Blog Website Preview](./P2__Blog_theme/BlogWebsitePreview.png)

### <ins>Goal:</ins>
Build a Blog website. Have a Like button to simulate user interaction.
<br/><br/>

### <ins>Post-Mortem:</ins>
I had a lot of fun with this one. As someone who likes to write short stories, this had me floored. I had this be a continuation of the Personal Website and have each blog post be about the “Elegant Pikachu”. For the Like aspect, I decided to make the box housing the Likes and Counter kind of like a loading bar. As the number got bigger, the bar on the left would move to the right. This of course will run into the JavaScript number limit after the many presses. Feel free to try to get there.
<br/><br/>

### <ins>NOTE:</ins>
Because of the scope of this project in particular, there are too many pain points where not having a “+” symbol would result in spaghetti code and work arounds that are not up to my personal standards let alone JavaScript. This is a representation of what I would have really done.
<br/><br/><br/><br/><br/><br/>

## Project Three – Business Website
[Business Website Index](./P3__Business_Website/index.html)<br/>
[Business Website Preview](./P3__Business_Website/BusinessWebsitePreview.png)

### <ins>Goal:</ins>
Build a business website. Include jQuery to open and close a description for each product offering.
<br/><br/>

### <ins>Post-Mortem:</ins>
The style of this website was inspired by a Cyberpunk aesthetic. NovaTechnica is a fictional corporation of the future. I wanted the font and the design to be something you would see from Weyland-Yutani and an 80s idea of the future.<br/><br/>
When considering the panel movements, coming from game development, user feedback was critical for me. I had each panel popping up and down feel like it had weight behind them. As if the user themselves were pulling the panels up with their mouse. This delay to open also allows for a seamless transition for the text to show up as if it was happening so quickly that the text seemed blurry. This hides the opacity trick from 0% to 100%. For the user, it just seems like the text is losing its light as it resets.
<br/><br/>

### <ins>NOTE:</ins>
Because of the experience I had in the last two projects with the symbol constraints, I opted to be as direct as possible with the implementation and not do any computation that would require a “+” or “%”. 
<br/><br/><br/><br/><br/><br/>

## Disclaimer
Because of the time constraints I was not able to properly debug the issue with the symbols but I suspected some sort of security program working in the background. Previewing the written code worked properly on General Assembly’s website but once the files were uploaded, all “+” and “%” symbols were deleted.
<br/><br/><br/>
