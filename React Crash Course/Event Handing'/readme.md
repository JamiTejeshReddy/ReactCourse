It refers to process of capturing user actions and responding to them within our applications
import React from 'react';

const MultiEventHandler = () => {
const handleClick = () => {
alert('Button clicked!');
};

    const handleMouseOver = () => {
        console.log('Mouse is over the button!');
    };

    return (
        <button onClick={handleClick} onMouseOver={handleMouseOver}>
            Hover over and click me!
        </button>
    );

}

export default MultiEventHandler;
