# Style Guide

The purpose of this guide is to act as a resource of preferred methods in contributing to curricula. It is not meant as a strict or mandatory set of rules. It should be considered a living document with all suggestions up for review and adjustment based on the needs of the students. All items here are meant as suggestions. 

## Index
coming soon.

## Code Styles

These are basic style recommendations. There are guidlines specifically for code that will be seen for students below. When writing code that will not be seen by students, you should write code in a manner that is most efficient for you. Utilizes the snippits available via the VS code extension and check CAT for any templates you expect but dont come up.

### Student Facing Code

The following suggestions are just that, suggestions. The goal is to create a consistent experience for the students that is both easy to read, efficient to write, and reduces potential bad habbits. 

#### Code From Documentation

When giving code examples where it's likely they will end up referencing the documentation, use the same style/formatting as the documentation less basic code standars like tabs vs spaces, no ending semi-colon and so forth. It is best to add a notation of on the first instance that even though we may have made a previous recommendation, we've chosen to use the same formatting as the documentation so that it will be easier to follow and that the student may make the choice of using the documentation format or the previous recommendation, but that when coding an application, it's best to be consistent throughout the application. 

Example:  

Mongoose uses then chaining throughout it's documentation over the use of async/await syntax. Use `.then` with examples, but notify the students that it's being used because it's what is used in [Mongoose's documentation](https://mongoosejs.com/docs/api.html#document_Document-execPopulate). 

#### Code Snippets

When creating code snippets, there are 2 options, numbered or unnumbered snipets. Use numbered snippets only when it would be valuable to the instructor to point out specific information seen on a particular line.  

When commenting Code Snippets, keep comments similar to that you would use in production. Any explanations needed, do outside of the code snippet as either student facing text or as instructor notes. Console statements should use left arrows to reveal results rather than comments.

#### JavaScript Standards

The prefered standard to use is a variation of [standard.js](https://standardjs.com/) with some basic preferences/deviations. The use of standard.js is to improve legibility of code for students
* DO use tabs instead of spaces.
* Do NOT use semicolons to end statements.
* Prefer single quotes unless using template literals. 
* DO use trailing commas.
* DO use camleCase naming variables.
* DO prefer Async/Await.
* DO prefer function declarations over function expressions.
* DO prefer arrow functions for callbacks and single line functions.
* DO prefer ternary opperator over simple if/else.
* DO use curly braces for multiline control flow.
* DO avoid use of `.this` in non object like code.
* DO prefer `const` over `let` over `var`.
* DO avoid hoisting when possible. 

##### Linting
No linting tool is in place or preffered. But a linting tool is in production that will utilize the above rules. The plugin will be specifically for VScode. Additionally, a snippit library pluggiin following these rules is also under production for use with VScode.

### HackerUSA Facing Code
There is no standard or requirement when creating code that will only be seen by the curriclumn team or instructors. However, recommendation would be to use the same standards as student facing code to allow for a consistent team experience and speed up code reviews so that team members are genearly coding in similar ways. Priority should be placed on readability, then avoiding technical debt, and then efficency of the developer.

## Writing Style
### Student Facing Text
Content that will be read by students should be written succinctly but with a possitive voice. Prefer general/simplified explanations over verbose and provide a simplified example or analogy before given complex computer science terms. Some general guildlines:
* User learner over student
* Avoid passive voice.
* Do use oxford comma.
* Do use <Span keyword> for JS/HTML/CSS/Python keywords.
* Ask thought provoking questions often.
* Prefer linking text over url as text.
* Avoid abberviations for first use on document, include abbreviation in parenthasis on first use. Ex: Node Package Manager(npm).

### Instructor Facing Text
Be as clear/brief as possible. This usually means a neutral tone and use of computer science terms since the instructor should be comfortable with them. Notes should be clear and easy to digest so they can read quickly and convey that information easily to students in their own voice. When using analogies, create at least 2 analogies for instructors to choose from.

## Courses & Topics
Each course will contain multiple topics as well as a primary.manifest.js. Courses are named as follows: abbreviation for Full Stack Development (FSD) followed by course number (03) and then Course subject. Example: FSD03 CSS, SASS, & CSS Frameworks.  

Projects that take place of topics should be titled as the topic number followed by Project- then the project title. Example: 08. Project- Drawing on Canvas  

Each course is then broken down into relevant topics. Topics are named as follows: Topic number (01.), Topic name (JavaScript Basics). Example: 01. JavaScript Basics.

### Instructor Guide.js
The "instructor guide.js" is found within a topic. It should be structured as so: 
* Header with Program & Course Title
* Course Path 
* Lesson Objectives
* Context for Subject Material
* Topic Prioritization
* Lesson Overview

#### Context for Subject Material
Context for Subject Material should throughly layout how the topic is relevant to the learners. It should contain use cases as well as analogies for the instructor to better relate the topic to learners. The more descriptive this section is, the more helpful it will be for instructors to convey the topic importance to the student. 

#### Lesson Overview
Lesson Overviews should map out what lessons will be in the course including the time expected to be spent on the lesson (generally 1 hour). Additionally, the overview should contain a through summary of items to pay attention to for that specific lesson, analogies for conveying the topic importance to learners, as well as any helpfull hints for instructing that specific lesson.  

The lesson overview should also map out what assets are contained within the lesson and expected time spent on eacht lesson.

### Quizzes
Most lessons should include a quiz covering a broad range of information covered through all the lessons of a topic. The exception to this is Project topics which will not contain a quiz. Expect Quizes to be at least 10 multiple choice questions long.  

Quizes do not exist to hold back students. They are mearly general assesments to let the student know if there are topics they should review before continuing on. 

For more complex questions, if feedback would be helpful to the student for clarification on any specific correct or incorrect answer, add it. If more than half of answers contain feedback, add feedback for all answers. 

When righting answers that are jokes/false. Make sure to include a range of topics. Example, don't place 4 gaming references on a quiz. This may alienate students that are not into gaming.

### Lessons 
Lessons are simply folders titled Lesson # (Lesson 1) containg lesson assets. Most lessons will contain the following: ./_assets, Slides, Lesson Companion, and an Activity. In order for lesson items to display properly, they must be added to the course manifest.   

#### Assets
The assets folder contains any media used on the slides, companion, or activity. Prefered naming convention is to use all lowercase letters with dashes instead of spaces; however, it will not be enforced.

#### Slides
Slides are integral to the success of the learner. They should be treated less as a slideshow and more as visuals to go along with a discussion.  

When writing creating slides, it is prefered that basic text slides be avoided. The curriculum engineer should add visuals to improve understanding, increase interest, or add levity to the presentation.  

In general, slides should include speaker notes. Keep in mind that not every instructor or TA will have instructored this topic before or even worked extensively with it. Add notes that will allow the instructor to make analogies; generally at least 2 is best.  

Slides should also thoroughly cover a topic on a conceptual level, allowing the student to understand why a topic is important. Code examples are useful, especially when the anatomy is broken down. Anytime code examples are used, special care should be given to the instructor notes to fully explain what they should focus on with the code snipit. It is especially useful to create code exercises in the lesson companion based on code examples seen in the slide show. Avoid overly complex code examples due to the likelyhood that the code will be too small for the learner to read.

Slides that relate directly lesson companion question should be marked with cueCompanion.

#### Lesson Companion
The Lesson Companion.js file will contain a combination of multiple choice questions and/or code exercises that can be completed during the slideshow presentation. Code exercises should not be overly complex and allow for the learner to maintain attention. 

Make sure to give feedback when it will improve the student's understanding.

#### Activity
The activity is where the most learning will take place for students. Activities should be designed in a way that they are practical and relateable to real world scenarios. For particularly complex activies, code alongs are recommended. Otherwise it is possible to do activities asynchronously where the instructor is considered a support.  

Activities should include starter code (except for when not applicable) via repository with instructions on how to get started with the activity.

For complex topics, it is useful for students to have activities that span over multiple lessons. When creating an activity of this type, provide repositories with complete code as well as 1 branch per part of the activity. The activity should alert the learner to the availability of the branch containing the code up till that point so that the student can continue to follow along should they have fallen behind in a previous part of a continued activity.

## Code Reviews
Coming soon! 