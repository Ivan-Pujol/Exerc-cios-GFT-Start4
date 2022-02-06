#Desafios - GFT Start #4 Java
1 / 3 - Exibindo Números Pares<br>
Desafios<br>
Crie um programa que leia um número e mostre os números pares até esse número, inclusive ele mesmo.<br>
<br>
Entrada<br>
Você receberá 1 valor inteiro N, onde N > 0.<br>
<br>
Saída<br>
Exiba todos os números pares até o valor de entrada, sendo um em cada linha. <br>

 <br>
Exemplo de Entrada	Exemplo de Saída<br>
6				>>>> 2<br>
				>>>> 4<br>
				>>>> 6<br>
<br>
=========================CODE=========================
import java.io.IOException;<br>
import java.util.Scanner;<br>
<br>

public class ProblemasBasicos{<br>
    public static void main(String[] args) throws IOException {<br>
      Scanner input = new Scanner(System.in);<br>
      int total = Integer.parseInt(input.next());<br>
    	for (int i = 2 ; i <=total  ; i++) {<br>
    		if (i%2==0 ) System.out.println(i);<br>
    	}<br>
    }<br>
	<br>
}<br>

