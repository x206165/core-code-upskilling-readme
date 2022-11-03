const React = require("react");

class WishlistForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: '',
      wish: '', 
      priority: 1
    }
    
    this.handleChange = this.handleChange.bind(this);
    //this.handleSubmit = this.handleSubmit.bind(this);
    
  }
  
  handleChange(event) {
    console.log("event name : " + event.target.name);
    console.log("state name : " + this.state.name);
    console.log("event wish : " + event.target.wish);
    
    const target = event.target;
    const name = target.name; 
    
    console.log("recent target name : " + name);
    
    this.setState({[name]: event.target.name});
    //this.setState({[wish]: event.target.wish});
  }
  
  handleSubmit(event){
    alert('Submitted');
    props.send(this.state); 
    event.preventDefault(); 
  }
  
  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Child name: 
          <textarea id="name" value={this.state.name} onChange={this.handleChange} />
        </label> 
        <label>
          Wish: 
          <textarea id="wish" value={this.state.wish} onChange={this.handleChange} />
        </label>
        <select id="priority">
            <option value='1'>1</option>
            <option value='2'>2</option>
            <option value='3'>3</option>
            <option value='4'>4</option>
            <option value='5'>5</option>
        </select> 
  
        <input type="submit" value="Submit" />
      </form>
    );
  }
};



https://github.com/x206165/core-code-upskilling-readme/issues/8

