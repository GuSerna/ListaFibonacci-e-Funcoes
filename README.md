# ListaFibonacci-e-Funções
Código em JavaScript, utilizado para gerar uma lista Fibonacci e ordena-la de maneira crescente e decrescente.

    function NumerosFibonacci(valor_inicial,qtd_numeros){
        let penultima = 0
        let ultimo = 1
        let atual = 0
        let numeros = []

        while (numeros.length < qtd_numeros){
            penultima = ultimo 
            ultimo = atual
            atual = penultima + ultimo
            if(atual > valor_inicial){
                numeros.push(atual)
            }
        }
        return numeros

    }

    let fibo = NumerosFibonacci(3,5)

    function OrdenarNumeros(lista, Ordem){

        if (Ordem == 'decrescente'){
            return  lista.reverse();
        }
        
        else if (Ordem == 'crescente') {
            return  lista
        }

          
        }
        
    function GerarEOrdenarNumerosFibo(numero_inicial, qtd, ordem){
       var listaFibo = NumerosFibonacci(numero_inicial, qtd)
       var listaOrdenada = OrdenarNumeros(listaFibo, ordem)
       return listaOrdenada
    }

    console.log(GerarEOrdenarNumerosFibo(0,10,'decrescente'))
