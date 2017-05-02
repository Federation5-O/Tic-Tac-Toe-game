# Tic-Tac-Toe-game

//Bernardo D. Villajuan
//CSC313 ES6 with React
//April 25, 2017

//Template
//from https://facebook.github.io/react/tutorial/tutorial.html#developer-tools
//code editing via https://codepen.io/gaearon/pen/JNYBEZ?editors=0010


// jshint esnext: true

import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';

class Board extends React.Component{
	renderSquare(i) {
		return <Square value={i} />;
	}
	
class Square extends React.Component{
	constructor(){
		super();
		this.state = {
			value: null,
		};
	}	
	
	
	
	render() {
		return(
			<button className="square" onClick={() => this.setState({value: 'X'})}>
				{this.props.value}
			</button>
		);
		
	}

}











