https://github.com/x206165/core-code-upskilling-readme/issues/11


function high(x){
  var xList = x.split(" "); 
  var alfabetList = "abcdefghijklmnopqrstuvwxyz".split("");
  var pActualList = [];
  var i = 0, j = 0, k = 0, pesoActual = 0, pesoTmp = 0, posicionPesoRes = 0; 
  // i es posicion de palabra actual, j es posicion de letra en palabra actual, k es posicion en alfabeto 
  var palabraActual = ""; 
  
  console.log(xList);
  console.log(alfabetList); 
  
  for ( i = 0 ; i < xList.length ; i++) {
    // recorrer lista de palabras 
    palabraActual = xList[i];
    console.log(palabraActual); 
    pesoTmp = 0;
    for (j = 0 ; j < palabraActual.length ; j++){
      // recorrer longitud de palabra actual para comparar con valores del alfabeto 
      pActualList = palabraActual.split("");
       
      //console.log(pActualList); 
        for ( k = 0; k < alfabetList.length ; k++) {
          // recorrer alfabeto y calcular peso de palabra
          // validar si la letra esta presente
          if (pActualList[j] === alfabetList[k]){
            // la letra es la misma 
            pesoTmp = pesoTmp + k + 1; 
            break; 
          }
        }
        
      if ( pesoActual < pesoTmp) {
        pesoActual = pesoTmp; 
        posicionPesoRes = xList[i]; 
        
        console.log(pesoActual);
        console.log(posicionPesoRes);
      }
      
    }
  }
  
  return posicionPesoRes; 
}
