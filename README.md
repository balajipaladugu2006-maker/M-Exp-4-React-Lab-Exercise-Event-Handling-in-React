# Exp-4-React-Lab-Exercise-Event-Handling-in-React
## NAME : Paladugu Venkata Balaji
## REG NO : 2305001024
## Aim
To create React applications that demonstrate event handling using onClick, onChange, and onSubmit events to handle user interactions, update data, and perform form submissions.

## Objectives
1. To understand event handling in React.
2. To implement button click events using onClick.
3. To create interactive applications using useState().
4. To show and hide messages using conditional rendering.
5. To handle input field changes using onChange.
6. To handle form submissions using onSubmit.
7. To retrieve user input using event.target.value.
8. To prevent page refresh using event.preventDefault().
# Program

## Exercise 1 – Counter
App.jsx
~~~python 
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  function increase() {
    setCount(count + 1);
  }

  function decrease() {
    setCount(count - 1);
  }

  return (
    <div>
      <h1>Counter</h1>

      <button onClick={increase}>+</button>

      <h2>Count: {count}</h2>

      <button onClick={decrease}>-</button>
    </div>
  );
}

export default App;
~~~
## Exercise 2 – Show / Hide Message
App.jsx
~~~python 
import { useState } from "react";

function App() {
  const [show, setShow] = useState(false);

  function handleClick() {
    setShow(!show);
  }

  return (
    <div>
      <h1>Show / Hide Message</h1>

      <button onClick={handleClick}>
        {show ? "Hide Message" : "Show Message"}
      </button>

      {show && (
        <h2>Welcome to React!</h2>
      )}
    </div>
  );
}

export default App;
~~~
## Exercise 3 – Student Registration Form
App.jsx
~~~python
import { useState } from "react";

function App() {
  const [name, setName] = useState("");
  const [regNo, setRegNo] = useState("");
  const [department, setDepartment] = useState("");
  const [submitted, setSubmitted] = useState(false);

  function handleSubmit(event) {
    event.preventDefault();
    setSubmitted(true);
  }

  return (
    <div>
      <h1>Student Registration</h1>

      <form onSubmit={handleSubmit}>
        <input
          type="text"
          placeholder="Student Name"
          value={name}
          onChange={(event) => setName(event.target.value)}
          required
        />

        <br /><br />

        <input
          type="text"
          placeholder="Register Number"
          value={regNo}
          onChange={(event) => setRegNo(event.target.value)}
          required
        />

        <br /><br />

        <input
          type="text"
          placeholder="Department"
          value={department}
          onChange={(event) => setDepartment(event.target.value)}
          required
        />

        <br /><br />

        <button type="submit">Register</button>
      </form>

      {submitted && (
        <div>
          <h2>Student Details</h2>
          <p>Name: {name}</p>
          <p>Register No: {regNo}</p>
          <p>Department: {department}</p>
        </div>
      )}
    </div>
  );
}

export default App;
~~~
## Output
## Exercise 1 – Counter
<img width="377" height="276" alt="image" src="https://github.com/user-attachments/assets/61cdb92e-938d-4ce9-bb47-e1aeed21437e" />

## Exercise 2 – Show / Hide Message
Show Message:
<img width="528" height="245" alt="image" src="https://github.com/user-attachments/assets/e7a93907-8b5b-44d7-bc94-4d371eb0ff75" />

Hide Message:
<img width="672" height="243" alt="image" src="https://github.com/user-attachments/assets/6a5bf24d-b22b-414c-b77f-8046732e7134" />

## Exercise 3 – Student Registration Form
<img width="1357" height="611" alt="image" src="https://github.com/user-attachments/assets/012e890b-5f0b-4776-8aa8-c23fe053bbd2" />

## Result
Thus, React event handling was successfully implemented through three exercises: Counter using onClick, Show / Hide Message using onClick and conditional rendering, and Student Registration Form using onChange and onSubmit events. The applications demonstrated handling user interactions and dynamically updating the user interface.
