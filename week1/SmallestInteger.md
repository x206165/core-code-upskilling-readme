
class SmallestIntegerFinder {
  findSmallestInt(args) {
    var minorVal = args[0]; 
    for(var i = 1 ; i < args.length ; i++){
      if(minorVal > args[i]) minorVal = args[i]; 
    }
    return minorVal; 
  }
}


https://github.com/x206165/core-code-upskilling-readme/issues/3

