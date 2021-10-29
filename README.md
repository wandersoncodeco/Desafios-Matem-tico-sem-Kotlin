# Desafios-Matem-tico-sem-Kotlin
Análise de Números
Desafio
Você deve fazer a leitura de 5 valores inteiros. Em seguida mostre quantos valores informados são pares, quantos valores informados são ímpares, quantos valores informados são positivos e quantos valores informados são negativos. Considere que o número zero é positivo, mas não pode ser considerado como positivo ou negativo.

Entrada
Você receberá 5 valores inteiros.

Saída
Exiba a mensagem conforme o exemplo de saída abaixo, sendo uma mensagem por linha e não esquecendo o final de linha após cada uma.
Exemplo de Entrada	
-5
0
-3
-4
12
Exemplo de Saída
3 par(es)
2 impar(es)
1 positivo(s)
3 negativo(s)


fun main(args: Array<String>) {

  val inteiros = mutableListOf<Int>()
   var pares = mutableListOf<Int>()
  	var impares = mutableListOf<Int>()
    var positivos = mutableListOf<Int>()
    var negativos = mutableListOf<Int>()
    
  for (i in 1..5) { inteiros.add(readLine()!!.toInt()) }
  for (i in inteiros) { if ( i % 2 == 0) { pares.add(i) } }
  for (i in inteiros) { if ( i % 2 != 0) { impares.add(i) } }
  for (i in inteiros) { if ( i > 0) { positivos.add(i) } }
  for (i in inteiros) { if ( i < 0) { negativos.add(i) } }
  
  println("${pares.size         } valor(es) par(es)")
  println("${impares.size       } valor(es) impar(es)")
  println("${positivos.size     } valor(es) positivo(s)")
  println("${negativos.size     } valor(es) negativo(s)")


}
