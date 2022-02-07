# Desafios Intermediários - GFT Start #4 Java
1 / 3 - Área Direita<br>
Desafio<br>
Leia um caractere maiúsculo, que indica uma operação que deve ser realizada e uma matriz M[12][12]. Em seguida, calcule e mostre a soma ou a média considerando somente aqueles elementos que estão na área direita da matriz, conforme ilustrado abaixo (área verde).<br>
<br>
 


Entrada<br>
A primeira linha de entrada contem um único caractere Maiúsculo O ('S' ou 'M'), indicando a operação (Soma ou Média) que deverá ser realizada com os elementos da matriz. Seguem os 144 valores de ponto flutuante que compõem a matriz.<br>
<br>
Saída<br>
Imprima o resultado solicitado (a soma ou média), com 1 casa após o ponto decimal.<br>
<br>
 
Exemplo de Entrada	Exemplo de Saída<br>
S<br>
1.0<br>
330.0<br>
-3.5<br>
2.5<br>
4.1<br>
...<br>

111.4<br>

=========================CODE=========================
import java.io.IOException;<br>
import java.util.Scanner;<br>
<br>
public class Dio {<br>
  <br>
    /*<br>
      - Diagonal principal: x == y;<br>
      - Diagonal secundária: x + y == valor máximo de y;<br>
    */<br>
	
    public static void main(String[] args) throws IOException {<br>
        Scanner leitor = new Scanner(System.in);<br>
        double soma = 0;<br>
        //char letra = leitor.next().toUpperCase().charAt(0);<br>
        String letra = leitor.nextLine();<br>
        double[][] M = new double[12][12];<br>
        for (int i=0; i < M.length; i++) {<br>
        	for (int j=0; j < M[i].length; j++) {<br>
        		M[i][j] = leitor.nextDouble();<br>
        	}<br>
        }<br>
<br>
        for (int i=0; i < M.length; i++) {<br>
          for (int j=0; j< M.length; j++) {<br>
            if(i<6){<br>
              if (i+j>(M.length)-1){<br>
        		  soma += M[i][j];<br>
        		  }  <br>
            }else{<br>
              if (j>=i+1){<br>
        		  soma += M[i][j];<br>
        		  } <br>
            }<br>
        		 <br> 
        	}<br>
        }<br>
<br>
        if (letra.equals("M")){<br>
          soma /= 30;<br>
        } <br>
    	System.out.println(String.format("%.1f", soma));<br>
    }<br>
	<br>
}<br>