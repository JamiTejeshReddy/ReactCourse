JSX: it stands for JavaScript XML. syntax extension is similar to HTML

JSX elemetns are converted into react elements which are JS objects
const element = <h1>Hello, world !</h1>
const element = React.createElement('h1',null,'Hello, World!')

Creating simple component
import React from 'react'
function HelloWorld(){
return (
<div>
<h1>Hello, world!</h1>
</div>
)
}export default HelloWorld

To render this component:
import React from 'react'
import ReactDOM from 'react-dom';
import HelloWorld from './HelloWOrld';
ReactDOM.createRoot(document.getElementById('root')).render(
<React.StrictMode>
<App />
</React.StrictMode>
)
