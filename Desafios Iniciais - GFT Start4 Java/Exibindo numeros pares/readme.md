# Desafios Iniciais - GFT Start #4 Java
<p>
2 / 3 - Exibindo Números Pares

Crie um programa que leia um número e mostre os números pares até esse número, inclusive ele mesmo.

Entrada
Você receberá 1 valor inteiro N, onde N > 0.

Saída
Exiba todos os números pares até o valor de entrada, sendo um em cada linha. 

 
Exemplo de Entrada	Exemplo de Saída
6					2
					4
					6
					
</p>

<p>
import java.io.IOException;
import java.util.Scanner;


public class ProblemasBasicos{
    public static void main(String[] args) throws IOException {
      Scanner input = new Scanner(System.in);
      int total = Integer.parseInt(input.next());
    	for (int i = 2 ; i <=total  ; i++) {
    		if (i%2==0 ) System.out.println(i);
    	}
    }
	
}
</p>