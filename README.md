<script>
var saldo = parseInt(prompt("Informe o saldo inicial"));
document.write("Saldo inicial: " + saldo + "<br>");
var encerrar = "n";

while (encerrar === "n") {
  var tipo = parseInt(prompt("Informe o tipo de operação (1 para entrada, 2 para saída)"));
  var quantidade = parseInt(prompt("Informe a quantidade"));

  if (tipo === 1) {
    saldo += quantidade;
    document.write("Entrada: " + quantidade + "<br>");
  } else if (tipo === 2) {
    if (saldo >= quantidade) {
      saldo -= quantidade;
      document.write("Saída: " + quantidade + "<br>");
    } else {
      document.write("Saldo insuficiente" + "<br>");
      alert("Saldo insuficiente");
    }
  } else {
    document.write("Tipo de operação inválido" + "<br>");
  }

  document.write("Saldo: " + saldo + "<br>");
  encerrar = prompt("Deseja encerrar? (s/n)");
}

document.write("Sistema encerrado" + "<br>");
</script>

