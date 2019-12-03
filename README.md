
# Speak Norwegian ![Speak Norwegian](favicon-32x32.png)

### Live website: https://paulldev.github.io/milestone-project-1/
### Repository: https://github.com/paulldev/milestone-project-1

  

## Introduction

**Speak Norwegian** is a website designed for people who want to learn norwegian as quickly as possible. You will learn the most commonly used words first, because these are the words that people use most frequently on a daily basis.

Did you know that learning the most frequently used **2000** words of a language will allow you to understand approximately **75%** of most conversations?

This website will give the english word, the norwegian translation, an example sentence to give context, and an audio file for pronounciation.

A lot of traditional language courses will teach you by subject (shopping, clothes, etc). This method will delay your progress because it will take longer for you to be able to talk with native norwegian speakers, unless they want to talk about shopping and clothes! The sooner you can start practicing with native speakers, the quicker you will learn.

  

## UX

### Strategy Plane
> What are you aiming to achieve and for whom?

I want users to be able to learn norwegian from home, without having to travel to a classroom with other students. Users will have the freedom to learn at their own pace and at times that suit their timetable.

### Scope Plane

> Which features (based on information from the strategy plane) do you
> want to include in your design?

 - **Portability:** I want users to be able to use the service from their phone or from their computer. Therefore, the website must be responsive to provide a good user experiences across many devices.
 - **Language content:** Users should be able to start learning content from day one. They should have words, sentences, and the corresponding translations. There should also be audio to help with pronounciation.
  - **Tutor session:** I want users to be able to book a learning session with a tutor is a few clicks.

  

### Structure Plane

> How is the information structured and how is it logically grouped.

 The information should be logically divided into sections. The **navigation bar** will be split into:
	 

 - Home.
 - Start Learning (where the words, translations, and sounds are located).
 - Book A Session (where you can book a learning session with a tutor).
 - Contact Us

 This structure gives good separation to the main things a user would want to do.
 
 The **home page** will repeat and reinforce the navigation sections (Start Learning, Book A Session, Contact Us). It will also contain social media links in the footer.

### Skeleton Plane

> How will our information be represented, and how will the user
> navigate to the information and features?

The information should be represented in such a way that the user can immediately understand the website structure and know where to go.
The user will be able to navigate anywhere, using the navbar. The homepage has several **call-to-action buttons**, which further prompt the user towards "Start Learning" or "Book A Session".

### Surface Plane

> What will our finished product look like?

  The finished product will be a clean, enjoyable, responsive, easy to navigate website, which will get the user started learning norwegian as quickly as possible.
  The colour scheme will mostly use the colours of the norwegian flag (blue, red, and white).

## Features
#### Overview
The website heavily relies on Bootstrap. I wanted to show knowledge about many Bootstrap features, but only if they fitted into the design of the website. I used the official documentation (https://getbootstrap.com/docs/4.1/getting-started/introduction/) for inspiration, tutorials, code snippets, class references. I made a consious effort to make everything as responsive as possible, using mostly relative units, and utilizing the Bootstrap grid system.
Where appropriate, I overrode classes to attain my desired results. DevTools was extensively used for this purpose. 
#### Home page > Navigation bar
The navigation is located at the top of each page and uses Bootstrap's navbar. I wanted the navbar to be collapsable on smaller devices.
Since white text is the main font colour throughout the website, I decided that a dark themed navbar was most suitable. This dark colour at the top of the page is matched with the dark background of the footer. The entire home page is nicely sandwiched between these two dark elements.
I added a red line hover effect (Hover.css https://ianlunn.github.io/Hover/) to the menu items to introduce a subtle use of colour from the norwegian flag (red). Although red is a striking colour, I used it sparingly because it also has negative meanings (warning, danger, delete, etc). I had to override the hvr-underline-from-center class to achieve the desired effect.
After experimenting with different menu alignments, I decided to align it on the right side of the navbar.
I added icons (from Font Awesome) to each menu item to add visual meaning beside the text.
#### Homepage > Carousel
I initially used a Jumbotron for this area, but later decided that a carousel would be a better and more stylish option. This allowed me to break up my introduction into three very simple sections:
* Read
* Repeat
* Remember

I initially considered using a background carousel image with overlayed text. This would have been easier to implement, but more difficult to avoid clashes between my text colour and the image colours. I settled for white text with a blue background. This provided good contrast.
The circular images are there to provide a visual meaning to each slide. The icons (from Font Awesome) that are beside each carousel item heading, also provide visual meaning. 
I wanted the carousel to take up the full screen height using 100vh, but I found that 85vh worked best on most devices.
The implemented responsiveness stops the text moving behind the carousel arrows.
#### Homepage > Tutors
I used Bootstrap cards to represent each tutor that was available to book a session with. After much experimentation, I achieved the effect I was looking for: cards that didn't get squashed, and moved to the next line (centered), as I tested for responsiveness.
I also used a fixed background (https://www.w3schools.com/cssref/pr_background-attachment.asp). The image has a mixture of red, white, and blue (the colours of the norwegian flag) and people talking (like a user talking with a tutor).
#### Homepage > Connect With Us
This section contains links to our social media. They just link to the homepages of each social media website.
The images are Font Awesome icons which were custom styled. I got the relevant colour hex codes from https://brandpalettes.com/.
Each icons has a hover effect from the hover.css library (https://ianlunn.github.io/Hover/).
The Connect With Us section will only appear on the homepage, not on the other pages. This is a deliberate decision.

#### Start Learning page
This section contains a brief description and the list of our words to learn. There are just three words to show how the list would work. There would be too much code duplication, and too much time used, to add more words.
Each english word/sentence is represented by a blue background. Each norwegian translation is represented by a red background. Once again, this ties into the colours found in the norwegian flag.
I originally wanted the audio played by clicking a speaker icon, but I found that too difficult without using javascript. Instead, I settled for using the **audio** element. This was too large, so I applied minimal styling to reduce the size (https://catswhocode.com/html-audio-tag/)
When moving to smaller devices, the column containing the chevron will disappear and the word > translation will be vertical instead of horizontal. This was my preferred way for dealing with this complex layout. The background colours also help separate the two different languages as they sit on top of each other.
#### Book A Session page
This section starts with a brief description, followed by a form that the user has to fill out to book a tutor session.
Keeping everything centered was challenging because of the way the labels behaved. Eventually I had to use fixed widths on my labels and corresponding elements and that enabled me to keep everything centered (including the labels).
I didn't like the original date picker element, so I found a better one that matched my other elements styling better (https://codepen.io/maheshambure21/pen/VYJQYG) 
#### Contact Us page
Keeping with my website centered theme, this contact form is centered and responsive.
I wanted to use Font Awesome icons to label each input. I got inspiration from the official documentation (https://getbootstrap.com/docs/4.0/components/input-group/).
## Future features to implement

* Put all the words, sentences, translations, and audio files into a database (instead of a long list). Using a database will allow us to have a dynamic website which will save each user's progress. It will also allow us to have a dynamic area where you can learn a single word each time, instead of scrolling through a long list of words.


## Technologies used

| Name | Type | Site url | Why use it? |

| :------ |:------- | :---- |

| HTML5 | Language | https://www.w3.org/TR/html52/ | To structure the website |

| CSS3 | Language | https://www.w3.org/Style/CSS/Overview.en.html | To style and layout the website |

| Bootstrap | Framework | https://getbootstrap.com/ | To make layout easier |

| Font awesome | Toolkit | https://fontawesome.com/ | To use vector icons and social logos |

| Hover.css | Library | https://ianlunn.github.io/Hover/ | To use hover effects |

| Real favicon generator | Tool | https://realfavicongenerator.net | To generate favicons from an image |

| Croppola | Tool | https://croppola.com/ | To crop my images |

| Reduce Images | Tool | https://www.reduceimages.com/ | To reduce the size of my images |

| Audacity | Software | https://www.audacityteam.org/ | To record audio and create audio files |
| Favicon Generator | Tool | https://realfavicongenerator.net | To general favicons for website |

  

## Testing

 - All links were manually tested. From the home page, each link was tested. From the 'Start Learning' page, each link was tested, etc.
- All menu items, links and buttons were individually tested for hover events and click events.
- All input fields that are 'required' were tested. Email addresses were tested for invalid addresses.
- Developer Tools was extensively used during development to test that all elements were behaving as expected.

## Deployment

All development was done locally using vscode as the IDE. Regular commits were made locally, which were then pushed to GitHub.

The project is hosted on **GitHub Pages** at the following url: https://paulldev.github.io/milestone-project-1/
The project **repository** is located at the following url:
https://github.com/paulldev/milestone-project-1
  

## Credits

### Media
All media is royalty free and found on .

Images for the **carousel** were downloaded from:
* https://unsplash.com/photos/mmWqrsjZ4Lw (read.jpg)
* https://unsplash.com/photos/PgGSbbkAVWM (repeat.jpg)
* https://unsplash.com/photos/AndE50aaHn4 (remember.jpg)

Images of **tutors** were downloaded from:
* https://www.pexels.com/photo/adult-beard-boy-casual-220453/
* https://www.pexels.com/photo/women-s-white-and-black-button-up-collared-shirt-774909/
* https://www.pexels.com/photo/man-wearing-black-zip-up-jacket-near-beach-smiling-at-the-photo-736716/

* The speech bubble logo was made using **Gimp**. The outline of the speech bubble was taken from an image of unknown origin, and the center area was made by me in Gimp.

  
## Acknowledgements

Special thanks to my mentor, Aaron Sinnott. I appreciated his insight, advice, and his time.