# country-quiz

The purpose of this website is to create a quiz game based around knowledge of world nations

A link to the live website is [HERE](https://cjcon90.github.io/country-quiz/)

---

## Table of Contents

- [Overview](#Overview)
- [User Experience (UX)](#UX)
  - [User Stories](#Stories)
  - [Design](#Design)
- [Features](#Features)
- [Technologies Used](#Technologies)
- [Testing](#Testing)
- [Bugs & Fixes](#Bugs)
  - [Known Bugs](#Known)
- [Deployment](#Deployment)
- [Credits & Resources](#Credits)

---

<a name="Overview"></a>

## Overview

CountryQuiz is a web app, built using the REST Countries API, that tests users knowledge on country flags, capital city names and country populations; it is focused on being both fun and educational.

It provides varying levels of difficulty depending on which region of the world a user selects and this provides continued enjoyment and learning and encourages repeated playthroughs.

---

<a name="UX"></a>

## User Experience (UX)

<a name="Stories"></a>

### User Stories

- **As a first-time visitor / player**

  - I want to quickly be able to find out how the game works
  - I want to be enticed to play the game by fun visuals and colours
  - I want the layout to be clear and uncluttered so that:
    - I can clearly see where I need to click to input my answers and progress through the game
    - I can clearly track my score is and see how far through the game I am at all times
  - I want to be able to save my score so I can try and beat it on my next play
  - I want to feel rewarded when I get a correct answer or get a new high score

- **As a returning visitor / player**

  - I want to be able to skip any tutorial and go straight into the game
  - I want my previous high score to be saved
  - I was there to be a large pool of questions so that my playing experience is different on each playthrough
  - I want to be able to increase the difficulty and take on new challenges as I get better at the game

- **As the site owner**
  - I want to encourage new users to play the game for the first time
  - I do not want first time players to be confused by the game in any way
  - I want there to be an option for users to share the app through their social media networks
    - I want this option/button be visible after every playthrough so that both first-time players and returning players alike are encouraged to share the app
  - I want the website to be both fun and educational, increasing the likelihood that:
    - users will enjoy the app
    - users will share the app
  - I want the app to work without any errors in terms of the questions asked or the scoring system

<a name="Design"></a>

### Design

#### Imagery

- The main game element of the app is based around the images of country flags on which the user is tested. These images are generated through the REST Countries API, and can represent any country in the world - based on which region or difficulty the user has selected.

- For the landing page of the app, I wanted a single image that would symbolise the subject matter of the game whilst providing a fun visual effect that would excite users to play the game.

- For this I chose an illustration of the earth by [Alfonso de Tomas, sourced on Shutterstock](https://www.shutterstock.com/image-vector/europe-map-africa-russia-asia-north-229383577)
- This image is animated on loading the main menu of the page, growing in size which again brings life into the design of the app.

![img](assets/images/globe-blue-sm.jpg)

#### Colour Scheme

- The main colour scheme for the app was structured around the selected main central image of the earth in space.

  - **Primary Colour** | _Space Cadet_ | #20503C | a dark, soft blue that works very well as a 'night mode' style background colour.

  - **Secondary Colour** | _Android Green_ | #9DBE39 | a bright green that contrasts nicely with the primary dark blue. It's brightness and vibrancy adds a touch of fun to the styling, a requirement as outlined in the user stories.

  - **White Colour** | _Baby Powder_ | #FFFFF6 | a soft white that does not appear sharp or overly bright against the two main app colours.

  - **Black Colour** | _Rich Black FOGRA 29_ | #0E1F2F | a soft black that again does not appear too sharp or overly dark against any of the app colours.

- As the country flags appearing within the app will feature many bright colours throughout, I kept the amount of colours used in the app to a minimum, as too many additional colours would easily risk clashing against the flags or make the game page overwhelming in terms of colour content.

![image](docs/color-palette.png)

#### Typography

- I chose two fonts to use within the document.

  - The default font for areas where legibility was the key factor, such as paragraphs and questions, I chose the popular [Roboto font](https://fonts.google.com/specimen/Roboto#standard-styles) that allows for a natural reading rhythm.

  - For the headings, I wanted a font that was clearly legible but fit with the need of fun visuals, as outlined in the user stories. For this I chose [Racing Sans One](https://fonts.google.com/specimen/Racing+Sans+One), a unique font due to its high contrast sans that creates a fun visual effect.

#### Sound

- There are five sounds implemented within the app which were all sourced from [ZapSplat](https://www.zapsplat.com/)

  1.  [Correct answer](https://www.zapsplat.com/music/bell-chime-notification-high-pitched-metallic-good-for-apps-games-and-other-ui-3/)

  1.  [Wrong Answer](https://www.zapsplat.com/music/game-error-tone-1/)

  1.  [Bonus Points Awarded](https://www.zapsplat.com/music/notification-alert-bell-chime-good-for-alerting-user-of-event-or-message-etc-4/)

  1.  [High Score](https://www.zapsplat.com/music/game-tone-bright-and-warm-synth-win-award-1/)

  1.  [Perfect Score](https://www.zapsplat.com/music/game-tone-bright-warm-and-magical-win-award-or-level-up/)

- The correct and wrong answer sounds were selected to be subtle and short in length as they would be heard multiple times in the app. They were also selected to be easily recognisable in terms of simulating achievement and error.
  - The addition of a unique sound for getting bonus points provides an extra reward to the user, and also makes the in-game sounds less repetitive
- The High Score and Perfect Score sounds were selected to sound somewhat related to each other (both rising melodic tones), with the sound for a perfect score being more complex and higher in tone to also give users an additional feeling of reward, in line with the user stories.

#### Wireframes

- Wireframes were created using Balsamiq
- The website was designed mobile-first

  1.  [Mobile Wireframes](docs/wireframes/wireframe-mobile.pdf)
  2.  [Tablet Wireframes](docs/wireframes/wireframe-tablet.pdf)
  3.  [Desktop Wireframes](docs/wireframes/wireframe-desktop.pdf)

##### Variation from Wireframes

- The wireframes were initally created with a scrolling image of all the country flags acting as the header background.
- When applying this in practice, the end result looked dated and garish so I changed the primary menu design to a single image of a globe, and placed it behind the main menu buttons rather than behind the title.

---

<a name="Features"></a>

## Features

#### Navigation

- Clear navigation to go straight into playing the game on first loading the app
  - Important for returning users who do not need any explanation on the rules.
- Clear navigation to the 'About' section on first loading the app
  - Important for first-time players
- All link text throughout the app is styled in a way that differentiates it from all non-interactive text
- All link and interactive buttons have additional styles when the user hover over or interact with them
- Any disabled buttons are clearly styled so users are not drawn to click on them
- Page auto-focuses to the text input on each question, to create less clicks for the user to progress through the game
- At the end of game user is presented with a list of navigation options
  - Repeat the game under the current region / difficulty settings
  - Play again but choose different region / difficulty settings
  - Exit the game and return to the main menu
    - This is useful for players who need to revisit the About section for any extra clarity

#### About Section

- The About section explains the game to new players:
  - The subject of the game
  - What questions are asked
  - How the region / difficulty selectors work
  - How points & bonus points are scored
  - Where the data comes from
  - How to report any inaccurate data
- Following the explanation there is a link to continue into the game without having to go back to the main menu

#### Game Mode Selection

- Any countries that do not have a population or a capital city name are automatically filtered out before any selection
- Users are given 6 filters for what region they want to play with:
  1.  Africa
  2.  Asia
  3.  Americas
  4.  Europe
  5.  Oceania
  6.  The World
- Users are then given a choice of 4 difficulties, that will filter the remaining countries based on population
  1.  Easy (20,000,000+ population)
  2.  Medium (5,000,000+ population)
  3.  Hard (150,000+ population)
  4.  Expert ()
      - The specific population numbers that determine the difficulty are not given in the app's About section, as this could reveal some of the in-game answers for the user.
      - 'Easy' and 'Medium' mode are disabled for Oceania, as there is not enough countries with a population of 5,000,000+

#### Game Functionality

- A random 5 countries are selected based on the user's chosen filters
- 3 questions are asked for each country
  - What is the country's name (based on the shown flag)
  - What is the countries capital city
  - What is the country's population
    - To generate the population options, an array of 5 populations is generated in the format: `[0.5x, 0.75x, 1x, 1.25x, 1.5x]`
    - Three options are then sliced from this array, so the options always contain the actual population, and appear in ascending order
- Each correct answer is worth 5 points
	- Players earn a bonus 5 points for answering all questions correctly on an individual country
- If a user gets an answer incorrect, the correct answer is displayed on screen.
- The user's progress in the game is displayed showing how many countries they have answered out of 5
- The user's score is always visible and updated as they progress through the game
- For text input questions, the user's keyboard is auto-focused to reduce necessary clicks and increase ease of play
	- Text answers can also be inputted via the Enter key, to make it easier for desktop players
	- For mobile players, the page automatically scrolls to the bottom on input of text, to prevent 'Submit' and 'Next' buttons being hidden by soft keyboard  

#### End Game Screen

- The user's final score and high score are displayed
- `localStorage()` is used to keep track of a user's high score
- If a user gets a new high score, they are notified with text and sound
- If a user scores 100/100, the text will display "Perfect Score", and a different tone will play
- There are navigation buttons as outlined above
- There is an option for the user to share their score with a link to the game in both Twitter and Facebook
  - The shared link will display: "_I just scored ${score} points in the Country Quiz Challenge! Can you do better? [https://cjcon90.github.io/country-quiz/](https://cjcon90.github.io/country-quiz/)_"

<a name="Technologies"></a>
## Technologies Used

### Languages Used

- HTML5
- CSS3
- JavaScript

### Frameworks, Libraries and Programs Used

- [Sass](https://sass-lang.com/) - Technology to organise and compile CSS from separate .scss files, and make use of Sass variables and functionalities
- [Node Package Manager](https://www.npmjs.com/) - Used to install the following packages through the Node.js runtime environment:
	- [Node-Sass](https://www.npmjs.com/package/node-sass) - to natively compile SCSS files to CSS
	- [Live Server](https://www.npmjs.com/package/live-server) - to launch a development server and view live changes to project
	- [npm-run-all](https://www.npmjs.com/package/npm-run-all) -  to run node-sass and live-server concurrently with a single command
	- [PostCSS CLI](https://www.npmjs.com/package/postcss-cli) - a tool to install CSS tools and plugins, such as:
		- [Autoprefixer](https://www.npmjs.com/package/autoprefixer) - a Post CSS plugin to parse CSS and adds vendor prefixes
- [Font Awesome](https://fontawesome.com/) - Used to add facebook and twitter icons
- [Google Fonts](https://fonts.google.com/) - Used to import Racing Sans One and Roboto fonts for use in project
- [VSCode](https://code.visualstudio.com/) - Chosen IDE for writing code
- [Balsamiq](https://balsamiq.com/) - For creating wireframes
- [ImageMagick](https://imagemagick.org/index.php) - For resizing images through command line
- [Shutterstock](https://www.shutterstock.com/home) - For sourcing primary 'globe' image
- [ZapSplat](https://www.zapsplat.com/) - For sourcing game sounds

## Testing

### Functionality Testing

- **Home Page / Main Menu**
	- Both links lead to correct destination
	- Both links give visual feedback when hovered over or pressed
	- It is possible to navigate to both links via the Tab key
	- The main manu animation is centered, with the globe falling behind the main menu buttons in all the tested viewports
	- The main menu screen starts with a blank screen of the primary color with none of the elements on the page visible before coming into view via their animation

- **About Section**
	- All links lead to correct destination
	- All links give visual feedback when hovered over or pressed
	- It is possible to navigate to all linksvia the Tab key
	- All external links open in a new tab
	- The 'mailto' link opens an email to cjcon90@pm.me in the user's default email application
	- The "How to Play" header stays at the top of page on all devices, taking up 100% of viewport width
	- Vertical overflow in the about section text scrolls to ensure that the web page height = 100% of the viewport height on all devices.

- **Region/DIfficulty Selectors**
	- I added a list of console outputs throughout the game to ensure that the game was functioning as expected:
		- Region selection:
			- ``console.log(`\nRegion selected: ${regionSetting}`)`` 
			- ``console.log(`Countries After Region Select: ${countryList.length}`);``
		- Difficulty selection & minimum population:
			- ``console.log(`\nDifficulty selected: ${difficultySetting}`);`` 
			- ``difficultySetting === "expert" ? console.log(`Minimum population: none`) : console.log(`Minimum population: ${difficulty[difficultySetting].toLocaleString()}`);``
			- ``console.log("Countries After Difficulty Select: " + countryList.length);``
		- Details of final countries selected
			- ``console.log("\nRandom 5 countries selected for game:");`` 
			- ``for (country of selectedCountries) {console.log(`name: ${country.name}, capital: ${country.capital}, population: ${country.population.toLocaleString()}`);}`` 
		- Population testing: ensuring that actual population is featured in answer options and placed at a random index
			- ``console.log(`\nPopulation options: ${popOptions}`);``
			- ``console.logconsole.log(`Actual population: ${answers[2]}`);``
			- ``console.log(`Actual Population is in options? ${popOptions.includes(answers[2]) ? "Yes" : "No"}`);``
			- ``console.log(`Actual Population is in options? ${popOptions.includes(answers[2]) ? "Yes" : "No"}`);``
		- Correct answer testing
			- ``console.log({ currentAnswer }, answer.toString());``
			- `if(isCorrect)`
				- ``console.log(`${streak}/3 on country`);``
				- `if (streak === 3)`
					- ``console.log(`Score +10!`);``
				- `else`
					- ``console.log(`Score +5!`);``
		- Final score testing
			- ``console.log(`Final score: ${score}`);``
- **Game counters**
	- Progress counter updates successfully
		- Shows progress as n/5 countries, and increments after each completed population question
	- Score counter updates successfully and is accurate to expected game score 
- **Country Flag**
	- Flag is always visible
	- Flag is always accurate to the country being tested
	- Entire flag is visible on all viewports
	- Image properties adjust accordingly to make Nepal fit on all viewports (and reverts afterwards):
```javascript
// if the country is Nepal then set the flag object-fit to contain, to compensate for unique aspect ratio
  if (answers[0][0] === "nepal") {
    flag.setAttribute("style", "object-fit: contain; border: none; box-shadow: none; height: 100%");
  } else {
    // else set the object-fit to cover
    flag.setAttribute("style", "object-fit: cover; border: solid 0.2rem $color-white; box-shadow: 0 0 .8rem rgba(0,0,0,.5); height: auto;");
  }
```

- **Question Text**
	-  Every third question asks "What is the name of this country?"
	-  The following question will ask "What is the capital of (country)?", with the country name being capitalised and accurate to the country being asked
	-  The following question will ask "What is the population of (country)?", with the country name being capitalised and accurate to the country being asked

- **Text Input**
	- For the country name and capital city questions, a text input is visible
	- The text input is auto focused so the user can begin inputting text without having to click on the input
	- The text input gives visual feedback that it is currently active
	- On desktops, users can input their answer via the Enter key
	- Typing in the text input will scroll to the bottom of the page so that the Submit and Next buttons are not hidden behind mobile soft keyboard
	- Population selection buttons are not visible when the text input is shown

- **Population Buttons**
	- Population buttons appear for the population question for each country
	- Text input is not visible when population buttons are shown
	- Button gives visual feedback when selected
	- Selected button corresponds to answer given when "Submit" button is pressed
	- User can change their mind, and selecting another button will change their stored answer
	- Buttons always feature three different options to select
	- The correct answer ia always featured in the options
	- Options are given in ascending order
	- The correct answer randomly appears as the 1st, 2nd or 3rd option
	- Populations are clearly legible and thousands/millions are separated by commas
	- Populations fit within their buttons, and buttons fit within the page, on all viewports

- **Answer Text**
	- Text is invisible until user submits answer
	- Text disappears when user moves to next question
	- Text displays "CORRECT" or "WRONG" depending on whether user is correct or incorrect
	- Text displays as green is user is correct
	- Text displays as red if user is incorrect
	- if user is incorrect, a subparagraph will display "The correct answer is (answer)"
	- The displayed answer is correct for the question being asked

- **Submit/Next Buttons**
	- Buttons give visual feedback when hovered over or pressed
	- On question load, submit button is enabled and next button is disabled
	- When a user submits an answer (whether via submit button or Enter key):
		- The submit button is disabled
		- The next button is enabled
		- The next button is auto-focused
	- On pressing the Next button:
		- The Next button is disabled
		- The Submit button is enabled
		- The next question is loaded
		- If all questions have been asked, the final score modal appears
- **End Game Screen/Modal**
	- Animations (modal appering from left and background blur) work on all devices
	- End Game Scores
		- High Score is recorded in the browser from previous sessions
		- High Score is reset to zero when playing in incognito mode or a new browser
		- Beating the previous high score successfully plays a sound and shows "New High Score" text in all browsers
		- Getting a score of 100 successfully plays a separate sound and shows "Perfect Score" text ina all browsers
	- Links & Buttons  
		- All links/buttons give feedback when pressed or hovered over
		- *Play Again* button repeats the quiz with 5 random countries and brings user to Q1
		- Change Region / Difficulty and Exit Game buttons bring user to game menu or main menu accordingly
		- Facebook and twitter buttons both successfully bring user to the respective social media website with a pre-prepared post, featuring a link to the app
			- On mobiles, this successfully opens a post in the default facebook/twitter app (if installed) 

### Validators

#### HTML5

Tested with [W3C Markup Validation Service](https://validator.w3.org/)

- 1 error (in 4 locations throughout app): **Section lacks heading**
	- Not relevant as game sections do not require heading in this use case

#### CSS

Tested with [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/validator)

- **Error: Value Error : height Parse Error 100)** 
	- This is related to the body height of `height: calc(var(--vh, 1vh) * 100);` which fixes viewport width issues on mobile browsers.
	- Code was sourced from [this CSS Tricks article](https://css-tricks.com/the-trick-to-viewport-units-on-mobile)
	- I also included a fallback of `height: 100vh;` within the code for browsers that do not support Custom Properties 
- **Error: Property backdrop-filter doesn't exist : none**
- **Error: Property backdrop-filter doesn't exist : blur(2px)**
	- These errors are related to my endgame modal animation, whereby the background underneath the modal is blurred
	- use of `backdrop-filter` is following guidance in [Mozilla Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter)
	- Despite errors, the animation works on all tested browsers. other than Firefox
	- [CanIUse.com](https://caniuse.com/?search=backdrop-filter) confirmed that backdrop-filter is not yet supported in Firefox, [is currently under consideration](https://platform-status.mozilla.org/#css-backdrop-filter)
- **Webkit Errors**
	- Any code with `-webkit` prefix (inserted by auto-prefixer) fails in CSS validation  

#### JavaScript

Tested with JSHint NPM Package](https://www.npmjs.com/package/jshint)

- Installed JSSHint **globally** using: `npm install -g jshint`
- To specify my JS document as ECMAScript version 6, I followed [this StackOverflow Post](https://stackoverflow.com/a/40620967), I added a `.jshintrc` file in the root of my app wiht the rule:
```javascript
{
  "esversion": 6
}
```
##### app.js
- No errors
##### game.js
- **Error: Function declarations should not be placed in blocks. Use a function expression or move the statement to the top of the outer function.**
	- This error is in relation to the `submitFunc()` and `inputFunc()` functions that are both found within the `submitAnswer()` function
	- The reason these functions are used *inside* the larger submitAnswer() function is that I needed them to access the `answer` and `answerInput` variables, but also needed to keep both functions free of arguments, so that I could easily remove them using `removeEventListener` 
	- Attempts to remove these functions brought bugs such as either the text input or submit button stacking answers from previous questions.

### Usability

- Web page was extensively tested in various browsers:
	- Google Chrome (desktop | Linux)
	- Firefox (desktop | Linux)
	- Samsung Internet (mobile | Android)
	- Chrome (mobile | Android)
	- Brave (mobile | Android)
- Responsiveness was tested extensively in both [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools) and [Responsive Design Checker](https://responsivedesignchecker.com/)
- Devices tested within DevTools were:
	- ![docs/devtool-sizes.png](docs/devtool-sizes.png)
	- Custom viewport sizes I created for testing purposes were:
		- 4k: 3840 x 2160
		- Macbook Pro 15: 2880 x 1800
		- Small laptop: 1366 x 768

        
