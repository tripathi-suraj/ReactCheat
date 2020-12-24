## React Cheat Sheet

In react the basic block are components there are two type of components stateless i.e functional component and statefull component i.e. class component

### Functional Component or Stateless
Functional component are basically javascript function,there are no buiilt in way to preserve state of variable that's why it's stateless but not problem React now introduced hooks special function using of hooks we can manage state.

```
import React from "react";
function Greet(props){
    props.name="Immute"; 
    console.log(props);
    return <h1>Hello Greet! {props.name} {props.lastname}</h1>;
}
export default Greet; 
```
or we can define functional component using ES6
```
const Greet2=(prop)=>{ 
    console.log(prop);
    return (
        <div>
        <h1>Hello {prop.name} {prop.firstname}</h1>         
            {prop.children}
        </div>
    )
}
export default Greet2
```
or
we can write like this
```
export default Greet2=(props)=><h1>Hello :{props.name}</h1>
```
### Class Component

```
import React, { Component } from "react";
class Welcome extends Component{
constructor(props) {
        super(props)
        this.state = {
             name:'Example'
        }
    }
    render(){
        return (
            <div>
                <h1>Welcome Class {this.props.name}</h1>
            </div>
        )
    }
}
export default Welcome
```

### Props and State

In React there is question that how component will communicate to each other so for this  there are props and state .
