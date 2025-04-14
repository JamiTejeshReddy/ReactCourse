Condiitonal Rendering allows you to render different UI elemetns based on certian conditions

import React from 'react';

const ConditionalGreeting = ({ isLoggedIn }) => {
if (isLoggedIn) {
return <h1>Welcome back!</h1>; // Render when the user is logged in
} else {
return <h1>Please sign up.</h1>; // Render when the user is not logged in
}
}

export default ConditionalGreeting;

using ternary :

import React from 'react';

const ConditionalGreeting = ({ isLoggedIn }) => {
return (
<h1>
{isLoggedIn ? 'Welcome back!' : 'Please sign up.'}
</h1>
);
}

export default ConditionalGreeting;

Logical And :
import React from 'react';

const Notification = ({ showNotification }) => {
return (
<div>
{showNotification && <p>You have a new message!</p>}
</div>
);
}

export default Notification;

With multiple conditions:
import React from 'react';

const UserStatus = ({ isLoggedIn, isAdmin }) => {
return (
<div>
{isLoggedIn && <p>Welcome back!</p>}
{isLoggedIn && !isAdmin && <p>You are a regular user.</p>}
{isLoggedIn && isAdmin && <p>Welcome, Admin!</p>}
{!isLoggedIn && <p>Please sign up.</p>}
</div>
);
}

export default UserStatus;
