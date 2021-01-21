---
layout: post
title:      "Functional VS Class Component"
date:       2021-01-21 01:48:14 -0500
permalink:  functional_vs_class_component
---

Separating concerns is crucial part of having organized code. React fits right into that as it helps us to divide up our app into multiple components, which can be either Functional(stateless)  or Class component(satefull). In my React Redux app I used Functional components for when I don’t have to keep track of state, although technically we can do that using hooks, or when there is a need to only return JSX, simply used to present the data received through props. I have made separate directory for container components which are mostly class components so that it has full access to states and lifecycle methods. 
```
Example for Class Component:

import React, { Component } from “react”
import { connect } from “react-redux”
import { fetchDiets } from “react”
import DietItem from “..actions/index”

class DietList extends Component {
 componetDidMount(){
  this.props.fetchDiets() 
  }
 render() {
	Const diets = this.props.diets.map((diet,i) => <DietItem key{i} diet= {diet} />)
 return (
 <div>
 <h1> Here are all the Diets </h1>
 {diets} 
 </div>
 );
 }
 Const mapStateProps = state =>{
  return{
   diets: state.diets
  }
}
export default connect(mapStateToProps,{fetchDiets})(Dietlist)
```

In this example I made a use of  ES6 class and extend the Component class in React. Used React lifecycle methods inside class components " componentDidMount". Passed props down to class components and access them with this.props.

```
Example for Functional Component:
import React from “react”
import { connect } from “react-redux”
const DietItem =({diet}){
 
  return (
    <div>
        <h1>{diet.diet_type}</h1>
         <p> {diet.start_weight}</P>
         <p> {diet.weight_lost}</P>                  
    
    </div>
 );
 }
 export default DietItem

```

  For this example it accepted and used props, and returned JSX.


In conclusion, using Functional components is the better way to keep your code clean and easy to read. But for the sake of separating your concern keep Container components as a Class component which is a Parent app that send data to other components. Where as Functional components can be the Child Components which receives data exclusively through prop.

