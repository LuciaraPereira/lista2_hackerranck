# lista2_hackerranck #

### Função 1 -  gradingStudents ###

function gradingStudents(grades) {

    const resultado = []; 
    
    for (let i = 0; i < grades.length; i++) {
        let nota;
        let resto = 0;

        if (grades[i] < 38) {
            nota = grades[i];
        } else {
            resto = grades[i] % 5;

            if (5 - resto < 3) {
                nota = grades[i] + (5 - resto);
            } else {
                nota = grades[i];
            }
        }

        resultado.push(nota);
    }

    return resultado;
    
}


### Função 2 - birthdayCakeCandles ####

function birthdayCakeCandles(candles) {

    let alta=0;
    let totalV = 0;
    for(let i = 0; i < candles.length; i++){
        if(candles[i] > alta){
            alta = candles[i];
        }
    }
    
    for (let c = 0; c < candles.length; c++){
          if(candles[c] === alta){
                totalV++;
            }
    }
    return totalV;
    
}

### Função 3 - kangaroo ###
function kangaroo(x1, v1, x2, v2) {

     if (v1 === v2) {
        return x1 === x2 ? "YES" : "NO";
    }
    
    const numerador = x2 - x1;
    const denominador = v1 - v2;
    
    if (denominador === 0) return "NO";

    if (numerador % denominador === 0 && (numerador / denominador) >= 0) {
        return "YES";
    }
    return "NO";
    
}
