function oddOrEven(array) {
  var i = 0 , contador = 0 ;
  var respuesta = "Not found"; 
  
  
  console.log(array);
  const arrayClean = array.filter(Boolean); 
  console.log(arrayClean);
  console.log(Number.isNaN(arrayClean[0]) + " es valor " + arrayClean[0]);
  
  
  if (Number.isNaN(arrayClean[0]) ||  arrayClean[0] == undefined) {
    contador = 0 ;
  } else {
    contador = arrayClean[i];
  }
  
  
  if(arrayClean.length > 0){
    for ( i = 1 ; i < arrayClean.length ; i++){
      if (!Number.isNaN(arrayClean[i])) contador = contador + arrayClean[i]; 
    }
  }
    
  
  contador = Math.abs(contador); 
  console.log(contador); 
  if(contador%2==0){
    respuesta = "even"; 
  } else {
    respuesta = "odd";
  }
  
  console.log(respuesta); 
  return respuesta; 
  
}


https://github.com/x206165/core-code-upskilling-readme/issues/4


