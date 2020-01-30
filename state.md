### Remember

Answer these on your own, then compare answers as a group

1.  What is state?
  <!-- State is the current state of the component and the props that are being accesed -->

2.  Where do you set initial state?
<!-- Initial state is set in the parent component, and can be accessed from there -->

3.  What method do you use to update state?
<!-- .setState will update this.state{ -->

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.
<!--This is adding 1 to the count of the this.state.questionsAnswered: 0 property, each time the button is clicked.  -->

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Tim Biles</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked

```JSX
import React, {Component} from 'react';

class Student extends Component {
  constructor(props){
    super(props)

    this.state = {
      questionsAsked: 0,
      inputLine: ''
    }
  }

  handleClick = () => {
    this.setState({questionsAsked: this.state.questionsAsked += 1});
  }

  render(){
    return(
      <div>
      <p>Number of Questions Asked</p>
      <p>{this.state.questionsAsked}</p>
      <input onChange/>
      <button onClick={this.handleClick}>Add One Q</button>
      </div>
    )
  }
}
```


6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.



### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?
