function isPalindrome(line) {
  var desLine = line + "", reverseLine = ""; 
  
  for (var i = 0; i < desLine.length; i++) {
    reverseLine = desLine[i] + reverseLine; 
  }
  
  if (reverseLine == desLine) {
    // son iguales 
    return true;
  } else {
    // no son iguales
    return false; 
  }
  
  
}


https://github.com/x206165/core-code-upskilling-readme/issues/5
