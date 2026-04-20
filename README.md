# treinoWhile
Códigos que visavam praticar laços de repetição, um pra tabuada, outro pra registro de produtos e o último para sistema bancárioara 

//TABUADA
let number = parseInt(prompt("Número: "));
let i = 0
while(i<=10){
    console.log(number*i++)
}

//REGISTRADOR DE PRODUTOS
let valor = 0
let maiorValor = 0
let n = -1
let total = 0
let quantidade = 0
while(valor!=n){
    valor = parseFloat(prompt("Valor: "));
    if(valor != -1){
        quantidade++
        total = total + valor
    }
    valor > maiorValor? maiorValor = valor: maiorValor
}
console.log("Quantidade: ", (quantidade))
console.log("Total: ", (total.toFixed(2)))
console.log("Maior valor :",(maiorValor.toFixed(2)))

//SISTEMA BANCÁRIO
let operaçao = 4
let saldo = 1000
let n = 0
let valor = 0
let totalOp = 0
while(operaçao != n){
    operaçao = prompt("=== MENU ===\n 1- Depósito\n 2- Saque\n 3- Consulta \n 0- Sair\n")
    switch(operaçao){
        case "1":
            valor = parseFloat(prompt("Escolha: 1\n Valor do depósito: "));
            saldo = saldo + valor
            console.log("Depósito realizado. Saldo atual: ",(saldo.toFixed(2))) ;
            totalOp++
            break;
        case "2":
           valor = parseFloat(prompt("Escolha: 2\n Valor do saque: "));
                if (valor <= saldo) {
                    saldo = saldo - valor; 
                    totalOp++
                    console.log("Saque realizado. Saldo restante: ",(saldo.toFixed(2)));
                } else {
                        console.log("Saldo insuficiente!");
                }
            break;
        case "3":
            console.log("Escolha: 3\n Saldo: ",(saldo.toFixed(2)))
            totalOp++
            break;
        case "0":
            break;
        default:
            console.log("ERROR: operação inválida.")
            break;
    }
}
console.log("Escolha: 0\n Saldo final: ",(saldo.toFixed(2)),"\n Total de operações: ",(totalOp))
