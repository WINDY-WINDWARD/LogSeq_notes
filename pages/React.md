- # UNIT 3
	- ## React Native
		- React Native uses the React library for the web and runs in JavaScriptCore
		  it sends Batched asynchronous messages to the native API of android or ios
		- ### Advantages
		  collapsed:: true
			- <ins>Cross-Platform:</ins>  React follows a principle of write once and run everywhere
			- <ins>Performance:</ins>  Code written in react native is compiled into native code. which enables it for all operating systems to provide closer native appearance
			- <ins>Community:</ins> React native has a large community of passionate developers who are constantly adding new features and fixing bugs
			- <ins>Hot Reloading:</ins> making a few changes in your app's code is immediately visible.
			- <ins>Faster Development:</ins> ability to develop apps quickly and deploy everywhere. using a single code-base
			- <ins>JavaScript:</ins> JavaScript a very popular language is the main language to develop the applications in react-native
		- ### Disadvantages
		  collapsed:: true
			- <ins>Still very new</ins>
			- <ins>Learning is Tough</ins>
			- <ins>lacks security robustness</ins>
			- <ins>takes time to initialize</ins>
		- ## Essential components of React Native
			- ### View:
			  basic built-in component used to build UI of Mobile apps. view is similar to the div in html. it is a content area where you can display your content.
			- ### States:
			  it is used to control the components. The variable data can be stored in the state. it is mutable means a state can change the value at any time.
			- ### Props:
			  props are used to pass data to the different components. It is immutable means props cannot change the value. it Provides a connection b/w the container component and presentation component.
			- ### Style:
			  it is an essential component in the web or mobile, which makes the application attractive. React Native does not require any special language or syntax.
			- ### Text:
			  this component displays text in the app. It uses the basic component textInput to take text input from the user
			- ### ScrollView:
			  it is a scrolling container used to host multiple views. It can be used to render the large list or content in view with a scroll bar
		- ## Threads used in React Native
			- React Native UI Thread (Main Thread)
			  collapsed:: true
				- for layout of the mobile app
			- React native javascript Thread
			  collapsed:: true
				- the thread running business logic
			- React Native modules Thread
			  collapsed:: true
				- use to access platform specific API's
			- React Native render Thread
			  collapsed:: true
				- draw the UI elements using OpenGL
		- ## Example Program
			- STATE
				- ```
				  import React, {Component} from 'react';
				  import {Text,View} from 'react-native';
				  
				  export default class App extends Component {
				  
				  	state = { 
				      	myState: 'Hello world'}
				     	
				      updateState = () => this.setState({myState:'Karthik'})
				      
				      render(){
				      	return(<View>
				          	<Text onPress={this.updateState}> {this.state.myState} </Text>
				              
				          </View>);
				      }
				  }
				  ```
				-