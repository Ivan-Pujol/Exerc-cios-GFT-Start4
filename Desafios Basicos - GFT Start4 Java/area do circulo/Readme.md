# Desafios Básicos - GFT Start #4 Java
1 / 3 - Área do Círculo<br>
<br>
A fórmula para calcular a área de uma circunferência é: area = π . raio2. Considerando para este problema que π = 3.14159:<br>
<br>
- Efetue o cálculo da área, elevando o valor de raio ao quadrado e multiplicando por π.<br>
<br>
Entrada<br>
A entrada contém um valor de ponto flutuante (dupla precisão), no caso, a variável raio.<br>
<br>
Saída<br>
Apresentar a mensagem "A=" seguido pelo valor da variável area, conforme exemplo abaixo, com 4 casas após o ponto decimal. Utilize variáveis de dupla precisão (double). Como todos os problemas, não esqueça de imprimir o fim de linha após o resultado, caso contrário, você receberá "Presentation Error".<br>
<br> 
Exemplos de Entrada	 Exemplos de Saída<br>
          2.00 >>>>>> A=12.5664<br>
		100.64 >>>>>> A=31819.3103<br>
		150.00 >>>>>> A=70685.7750<br>
<br>
==========================CODE==========================
import java.util.Scanner; <br>
<br>
public class Classe{<br>
	public static void main(String[] args){<br>
		Scanner scan = new Scanner(System.in);<br>
<br>
		 //declare suas variaveis do tipo double<br>
		 double area =0;<br>
		 double raio = scan.nextDouble();<br>
<br>
                  //continue a solucao<br>
<br>
		area = 3.14159 * (Math.pow(raio,2));<br>
<br>
		System.out.printf("A=%.4f\n", area);<br>
	}<br>
}<br>