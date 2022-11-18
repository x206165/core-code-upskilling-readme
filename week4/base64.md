https://github.com/x206165/core-code-upskilling-readme/issues/10

function base64toBase10(base64) {
    // Your code here
  //console.log(new Buffer.from(base64, 'base64').toString()); 
  //return new Buffer.from(base64, 'base64').toString('decimal'); 
  
  
  // se almacena el string de los posibles caracteres en la base 64 para tener una referencia de posiciones
  // la posicion permite hacer la conversion de cual es base 64 y su posicion indica el valor base 10
    let base = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/';
  // se hace un split del string a evaluar con '' para obtener todos los caracteres
  // sobre el Array de los caracteres se usa reduce para definir una funcion de pares en el Array, posicion current y siguiente
  // por conversion de base se multiplica el current por la base que tiene para darle formato a cada uno que no sea el ultimo valor
  // luego se obtiene la posicion del siguiente caracter para convertir la equivalencia y se hace lo mismo hasta terminar de recorrer
    return base64.split('').reduce((p, c) => p * 64 + base.indexOf(c), 0);
  
}

