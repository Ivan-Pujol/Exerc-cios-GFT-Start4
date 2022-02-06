# Desafios Iniciais - GFT Start #4 Java
3 / 3 - Dama
<p>
O jogo de xadrez possui várias peças com movimentos curiosos: uma delas é a dama, que pode se mover qualquer quantidade de casas na mesma linha, na mesma coluna, ou em uma das duas diagonais, conforme exemplifica a figura abaixo:




 
O grande mestre de xadrez Kary Gasparov inventou um novo tipo de problema de xadrez: dada a posição de uma dama em um tabuleiro de xadrez vazio (ou seja, um tabuleiro 8 × 8, com 64 casas), de quantos movimentos, no mínimo, ela precisa para chegar em outra casa do tabuleiro?

Kary achou a solução para alguns desses problemas, mas teve dificuldade com outros, e por isso pediu que você escrevesse um programa que resolve esse tipo de problema.  

Entrada
A entrada contém vários casos de teste. A primeira e única linha de cada caso de teste contém quatro inteiros X1, Y1, X2 e Y2 (1 ≤ X1, Y1, X2, Y2 ≤ 8). A dama começa na casa de coordenadas (X1, Y1), e a casa de destino é a casa de coordenadas(X2, Y2). No tabuleiro, as colunas são numeradas da esquerda para a direita de 1 a 8 e as linhas de cima para baixo também de 1 a 8. As coordenadas de uma casa na linha X e coluna Y são (X, Y ).

O final da entrada é indicado por uma linha contendo quatro zeros.

Saída
Para cada caso de teste da entrada seu programa deve imprimir uma única linha na saída, contendo um número inteiro, indicando o menor número de movimentos necessários para a dama chegar em sua casa de destino.
</p>
 
Exemplo de Entrada	Exemplo de Saída<br>
4 4 6 2				 1<br>
3 5 3 5				 0<br>
5 5 4 3				 2<br>
0 0 0 0<br>



Maratona de Programação da SBC 2008.
================================CODE=====================================

import java.util.Scanner;<br>
<br>
public class Main {<br>
	public static void main(String[] args) {<br>
		Scanner sc = new Scanner(System.in);<br>
				<br>
		int x1,y1,x2,y2;<br>
		//se estiver na mesma linha ou mesma coluna ou mesma diagonal, gasta 1 movimento<br>
		//se estiver em qualquer outra posição, a rainha gastará 2 movimentos!<br>
<br>
	    while(true){<br>
	    	x1 = sc.nextInt();<br>
	    	y1 = sc.nextInt();<br>
	    	x2 = sc.nextInt();<br>
	    	y2 = sc.nextInt();<br>
	    	if(x1 == 0 && y1 == 0 && x2 == 0 && y2 == 0) break; //condição de parada<br>
	    	if(x1==x2&&y1==y2 )		<br>
	    		System.out.println("0");<br>
	        else if(x1==x2||y1==y2)	{<br>
	          //indicação de ("reta") linha ou coluna;<br>
	        	System.out.println("1");<br>
	        }<br>
	    	else if(((x1-x2)+(y1-y2)==0)||((x1-x2)+(y2-y1)==0)){<br>
	    	  //indicação de ("diagonal");<br>
	    		System.out.println("1");<br>
	    	}<br>
	        else <br>
	        	System.out.println("2");	<br>
	    }<br>
		sc.close();<br>
	}<br>
}<br>
<br>
