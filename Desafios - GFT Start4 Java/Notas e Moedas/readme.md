#Desafios - GFT Start #4 Java
2 / 3 - Notas e Moedas<br>
<br>
Leia um valor de ponto flutuante com duas casas decimais. Este valor representa um valor monetário. A seguir, calcule o menor número de notas e moedas possíveis no qual o valor pode ser decomposto. As notas consideradas são de 100, 50, 20, 10, 5, 2. As moedas possíveis são de 1, 0.50, 0.25, 0.10, 0.05 e 0.01. A seguir mostre a relação de notas necessárias.<br>
<br>
Entrada<br>
O arquivo de entrada contém um valor de ponto flutuante N (0 ≤ N ≤ 1000000.00).<br>
<br>
Saída<br>
Imprima a quantidade mínima de notas e moedas necessárias para trocar o valor inicial, conforme exemplo fornecido.<br>
<br>
Obs: Utilize ponto (.) para separar a parte decimal.<br>
<br> 
Exemplo de Entrada	Exemplo de Saída<br>
576.73<br>

NOTAS:<br>
5 nota(s) de R$ 100.00<br>
1 nota(s) de R$ 50.00<br>
1 nota(s) de R$ 20.00<br>
0 nota(s) de R$ 10.00<br>
1 nota(s) de R$ 5.00<br>
0 nota(s) de R$ 2.00<br>
<br>
MOEDAS:<br>
<br>
1 moeda(s) de R$ 1.00<br>
1 moeda(s) de R$ 0.50<br>
0 moeda(s) de R$ 0.25<br>
2 moeda(s) de R$ 0.10<br>
0 moeda(s) de R$ 0.05<br>
3 moeda(s) de R$ 0.01<br>
<br>
4.00<br>

NOTAS:<br>
0 nota(s) de R$ 100.00<br>
0 nota(s) de R$ 50.00<br>
0 nota(s) de R$ 20.00<br>
0 nota(s) de R$ 10.00<br>
0 nota(s) de R$ 5.00<br>
2 nota(s) de R$ 2.00<br>
MOEDAS:<br>
0 moeda(s) de R$ 1.00<br>
0 moeda(s) de R$ 0.50<br>
0 moeda(s) de R$ 0.25<br>
0 moeda(s) de R$ 0.10<br>
0 moeda(s) de R$ 0.05<br>
0 moeda(s) de R$ 0.01<br>
<br>
91.01<br>
<br>
NOTAS:<br>
0 nota(s) de R$ 100.00<br>
1 nota(s) de R$ 50.00<br>
2 nota(s) de R$ 20.00<br>
0 nota(s) de R$ 10.00<br>
0 nota(s) de R$ 5.00<br>
0 nota(s) de R$ 2.00<br>
MOEDAS:<br>
1 moeda(s) de R$ 1.00<br>

0 moeda(s) de R$ 0.50<br>
0 moeda(s) de R$ 0.25<br>
0 moeda(s) de R$ 0.10<br>
0 moeda(s) de R$ 0.05<br>
1 moeda(s) de R$ 0.01<br>

=========================CODE=========================
import java.util.Scanner;<br>
<br>
public class Main {<br>
<br>
	public static void main(String[] args) {<br>
<br>
		Scanner sc = new Scanner(System.in);<br>
<br>
		double N;<br>
		int quociente, resto, nota, moeda;<br>
<br>
		N = sc.nextDouble();<br>
<br>
		resto = (int) (N * 100.0 + 0.5);<br>
<br>
		System.out.println("NOTAS:");<br>
<br>
		nota = 100;<br>
		quociente = resto / (nota * 100);<br>
		System.out.println(quociente + " nota(s) de R$ " + nota + ".00");<br>
		resto = resto % (nota * 100);<br>
<br>
		nota = 50;<br>
		quociente = resto / (nota * 100);<br>
		System.out.println(quociente + " nota(s) de R$ " + nota + ".00");<br>
		resto = resto % (nota * 100);<br>
<br>
		nota = 20;<br>
		quociente = resto / (nota * 100);<br>
		System.out.println(quociente + " nota(s) de R$ " + nota + ".00");<br>
		resto = resto % (nota * 100);<br>
		<br>
		nota = 10;<br>
		quociente = resto / (nota * 100);<br>
		System.out.println(quociente + " nota(s) de R$ " + nota + ".00");<br>
		resto = resto % (nota * 100);<br>
		<br>
		nota = 5;<br>
		quociente = resto / (nota * 100);<br>
		System.out.println(quociente + " nota(s) de R$ " + nota + ".00");<br>
		resto = resto % (nota * 100);<br>
		<br>
		nota = 2;<br>
		quociente = resto / (nota * 100);<br>
		System.out.println(quociente + " nota(s) de R$ " + nota + ".00");<br>
		resto = resto % (nota * 100);<br>
<br>
<br>
		System.out.println("MOEDAS:");<br>
<br>
<br>
		moeda = 100;<br>
		quociente = resto / moeda;<br>
		System.out.println(quociente + " moeda(s) de R$ 1.00");<br>
		resto = resto % moeda;<br>
<br>
		moeda = 50;<br>
		quociente = resto / moeda;<br>
		System.out.println(quociente + " moeda(s) de R$ 0.50");<br>
		resto = resto % moeda;<br>
<br>
    moeda = 25;<br>
		quociente = resto / moeda;<br>
		System.out.println(quociente + " moeda(s) de R$ 0.25");<br>
		resto = resto % moeda;<br>
		<br>
		moeda = 10;<br>
		quociente = resto / moeda;<br>
		System.out.println(quociente + " moeda(s) de R$ 0.10");<br>
		resto = resto % moeda;<br>
		<br>
		moeda = 5;<br>
		quociente = resto / moeda;<br>
		System.out.println(quociente + " moeda(s) de R$ 0.05");<br>
		resto = resto % moeda;<br>
		<br>
		moeda = 1;<br>
		quociente = resto / moeda;<br>
		System.out.println(quociente + " moeda(s) de R$ 0.01");<br>
		resto = resto % moeda;<br>
<br>
		sc.close();<br>
	}<br>
}<br>