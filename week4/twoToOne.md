function longest(s1, s2) {
  // your code
  console.log(s1);
  console.log(s2);
  
  var modelArray = "abcdefghijklmnopqrstuvwxyz".split(''); 
  var resultArray = []; 
  var count = 0; 
  
  for (var i = 0; i < modelArray.length ; i++){
    // iterate over the modelArray to check every letter 
    if(s1.includes(modelArray[i]) || s2.includes(modelArray[i])) {
      count = resultArray.push(modelArray[i]);
      console.log(count);
    }
  }
  
  return resultArray.join(''); 
  
}


https://github.com/x206165/core-code-upskilling-readme/issues/9

