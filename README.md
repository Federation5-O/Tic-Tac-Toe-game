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
	constructor(){
		super();
		this.state = {
			squares: Array(9).fill(null),
		};
	}

	renderSquare(i) {
		return <Square value={i} />;
	}
	
	render(){
		return (
			<div>
				<div className="status">{status}</div>
				<div className="board-row">
					{this.renderSquare(0)}
					{this.renderSquare(1)}
					{this.renderSquare(2)}
				</div>
				<div className="board-row">
					{this.renderSquare(3)}
					{this.renderSquare(4)}
					{this.renderSquare(5)}
				</div>
				<div className="board-row">
					{this.renderSquare(6)}
					{this.renderSquare(7)}
					{this.renderSquare(8)}
				</div>
			</div>
    );
  }
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






























