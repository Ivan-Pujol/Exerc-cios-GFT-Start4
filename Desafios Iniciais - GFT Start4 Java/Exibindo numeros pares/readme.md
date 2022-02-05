# Desafios Iniciais - GFT Start #4 Java
<p>
2 / 3 - Exibindo Números Pares<br>

Crie um programa que leia um número e mostre os números pares até esse número, inclusive ele mesmo.<br>

Entrada<br>
Você receberá 1 valor inteiro N, onde N > 0.<br>

Saída<br>
Exiba todos os números pares até o valor de entrada, sendo um em cada linha. <br>

 
Exemplo de Entrada	Exemplo de Saída<br>
6			2<br>
 			4<br>
			6<br>
					
</p>

<p>
import java.io.IOException;<br>
import java.util.Scanner;<br>


public class ProblemasBasicos{<br>
    public static void main(String[] args) throws IOException {<br>
      Scanner input = new Scanner(System.in);<br>
      int total = Integer.parseInt(input.next());<br>
    	for (int i = 2 ; i <=total  ; i++) {<br>
    		if (i%2==0 ) System.out.println(i);<br>
    	}<br>
    }<br>
	
}<br>
</p>
