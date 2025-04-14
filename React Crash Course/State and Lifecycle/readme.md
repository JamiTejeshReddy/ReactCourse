State is a built in object that creates and manage their own data
We use useState() hook that lets you add state to functional Components

import React, { useState } from 'react';

const Counter = () => {
// Declare a state variable named count, initialized to 0
const [count, setCount] = useState(0);

    return (
        <div>
            <h1>Count: {count}</h1> {/* Display the current count */}
            <button onClick={() => setCount(count + 1)}>Increment</button> {/* Increment the count */}
        </div>
    );

}

export default Counter;

LIfecycle of a react component refers to the series of methods that are invoked in different stages of components existance

1. Mouning
2. Updating
3. Unmounting

useEffect() hook :

import React, { useState, useEffect } from 'react';

const SimpleCounter = () => {
const [count, setCount] = useState(0);

    useEffect(() => {
        console.log('Component has rendered');

        // Cleanup function to run when the component is unmounted
        return () => {
            console.log('Cleanup before next render or unmount');
        };
    }, [count]); // Effect runs every time 'count' changes

    return (
        <div>
            <h1>Count: {count}</h1>
            <button onClick={() => setCount(count + 1)}>Increment</button>
        </div>
    );

}

export default SimpleCounter;

Importing Hooks: The useState and useEffect hooks are imported from React.

State Declaration: The count state is initialized to 0 using useState.

Using useEffect:

The effect logs a message to the console every time the component renders.
A return function inside the useEffect acts as a cleanup function. It logs a message right before the component is removed from the DOM or just before a change is made.
The second argument, [count], makes the effect run whenever count changes.
Rendering UI: The component displays the current count and includes a button to increment the count.

This example illustrates how to effectively use the useEffect hook to handle side effects related to component lifecycle events, such as rendering and unmounting.
