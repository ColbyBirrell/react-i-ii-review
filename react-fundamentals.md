### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
<!-- a javascript library -->

2.  What is create-react-app?
<!-- a tool from FB that helps create the webpack and other components of react  -->

3.  What is Component Based Architecture?
<!-- uses component to update and display dynamic information on the page -->

4.  What is JSX?
<!-- a coding language, that combines the best of JS and html -->

5.  What is the virtual DOM?
<!-- a middle man dom for helping decide if the real DOM needs to be updated -->

6.  What is unidirectional (one-way) data flow?
<!-- data flows down from the parent components, but not up to the parent from the child -->

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
<!-- compiles oll of the backend that you need to run the react app in your browser, from your compiled code -->

8.  Explain what this code does:
<!-- this imports the react files and scripts that you need to run the app, and will export the component to the other components -->
```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.
<!-- the data is passed in a props variable, from the render return section of the component -->

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?
<!-- the codebase is from a source you cannot control, but it makes the initialization of the app much easier -->

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue
<!-- JSX uses JS and HTML, will be easier to understand, and easier to map the components of the page render -->

14. Compare and contrast one-way data flow with two-way data binding.
<!-- oneway data is better due to the fact that you know where the data is coming from, and that makes debugging easier, and will save the hassle of trying to find the source of a bug in two areas, vs just one. -->
