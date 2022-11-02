https://github.com/x206165/core-code-upskilling-readme/issues/6


function well(x){
  var ideasContador = 0; 
  
  console.log("x contiene " + x);
  
  var goodIdeasArray = x.filter(
    element => element == "good"
  );
  
  console.log("goodIdeasArray contiene " + goodIdeasArray);
  
  if (goodIdeasArray.length == 0) return "Fail!";
  
  if (goodIdeasArray.length <= 2) {
    return "Publish!";
  } else {
    return "I smell a series!";
  }  

}

