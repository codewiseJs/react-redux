[![Build Status](https://travis-ci.com/cococolacode/react-redux.svg?branch=master)](https://travis-ci.com/cococolacode/react-redux)

### Getting Started
To learn redux we must first understand what state is. <br>
 **_what is a state?_** <br>
*The simple answer is, It's a place where the data comes from.*<br>
 *In other words, “state” is what allows you to create components that are dynamic and interactive.*<br>
*Example*
``` javascript
Class MyClass extends React.Component { 
   this.state = { value : "my-new-value" }; 
  render(){
  return <div>{ths.state.value}</div>;// this will return the my-new-value
 }
}
```
**_What is redux?_**<br>
*Redux is a predictable state container for JavaScript apps.*<br>
**_Merits_**<br>
 * _It helps apps to scale by providing a way to manage state through a unidirectional data flow model._
 * _redux devTools is awosome._<br>
 ### Redux flow
 All data in redux application follows the same lifecycle patterns which  make the app logics more predicable and easy to learn.<br>
 * store
 * actions
 * reducers<br>
 
### Installation 
``` terminal 
npm install --save react-redux redux
```
> *redux --> for creating store*<br>
> *React Redux requires React 16.8.3 or later.*

 **Let's learn how to create our store**
 ``` javascript
 //importing createStore from redux
 import {createStore} from 'redux';
 
 function reducer(){
 return 'this is a stae'
 }
 const store = createStore(reducer); //passing reducer function as a argument to createStore.
 console.log(store); // output: this is a state, since the reduce 'this is a state'. 
 ```
 We have successfully created our first store.<br>
 *Now, to dispatch an action, let's create an action, which is basically just an object with a type and a payload*
 ``` javascript
 const action = {
     type:'changeState',
      payload:{
        newState:'my new state', 
      }
 }
 ```
 *to dispatch or send an action,* 
 ``` javascript 
 store.dispatch(action )
 ```
 Next, let's learn how our reducer reads an action to update a store state.
 reducer have two parameters - _initial state of a reducer and the action_. It listens to every single action that is send.So, there needs to be figuring out what to do differently for each action. For now, let's just print our action.
```javascript
 reducer(state,action){
 console.log(action);
 return 'This is a state'
}
 ```
 _It should prints the action type and payload in console as below._<br>
 ![redux](https://user-images.githubusercontent.com/47861774/57584969-3e2c0480-7501-11e9-8770-a39dc0c4c996.png)
 


