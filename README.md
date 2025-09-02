# lista2_hackerranck

Função kangaroo
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
