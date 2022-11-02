https://github.com/x206165/core-code-upskilling-readme/issues/7


import React, {useState} from 'react';

export class Counter extends React.Component {
  constructor(props) {
    // Your state
    super(props);
    this.state = {counter: 0} 
    
    // binding
    this.decrement = this.decrement.bind(this);
    this.increment = this.increment.bind(this);
  }
  
  decrement() {
    console.log(this.state.counter);
    this.state.counter = this.state.counter - 1; 
    console.log(this.state.counter);
  }
  
  increment() {
    this.state.counter = this.state.counter + 1; 
  }
  
  // Your event handlers 
  render() {
    const { counter } = this.state; 
    
    return (
      <div>
        <h1 id="counter">{this.state.counter}</h1>
          <button id="decrement" type="button" onClick={this.decrement}>
            Decrement
          </button>
          <button id="increment" type="button" onClick={this.increment}>
            Increment
          </button>
      </div>
    )
  }
}

