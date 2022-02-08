#Desafios Intermediários - GFT Start #4 Java
2 / 3 - Experiências<br>
<br>
Maria acabou de iniciar seu curso de graduação na faculdade de medicina e precisa de sua ajuda para organizar os experimentos de um laboratório o qual ela é responsável. Ela quer saber no final do ano, quantas cobaias foram utilizadas no laboratório e o percentual de cada tipo de cobaia utilizada.<br>
<br>
Este laboratório em especial utiliza três tipos de cobaias: sapos, ratos e coelhos. Para obter estas informações, ela sabe exatamente o número de experimentos que foram realizados, o tipo de cobaia utilizada e a quantidade de cobaias utilizadas em cada experimento.<br>
<br>
Entrada<br>
A primeira linha de entrada contém um valor inteiro N que indica os vários casos de teste que vem a seguir. Cada caso de teste contém um inteiro Quantia (1 ≤ Quantia ≤ 15) que representa a quantidade de cobaias utilizadas e um caractere Tipo ('C', 'R' ou 'S'), indicando o tipo de cobaia (R:Rato S:Sapo C:Coelho).<br>
<br>
Saída<br>
Apresente o total de cobaias utilizadas, o total de cada tipo de cobaia utilizada e o percentual de cada uma em relação ao total de cobaias utilizadas, sendo que o percentual deve ser apresentado com dois dígitos após o ponto.<br>
<br>
 
Exemplo de Entrada	Exemplo de Saída<br>
10<br>
10 C<br>
6 R<br>
15 S<br>
5 C<br>
14 R<br>
9 C<br>
6 R<br>
8 S<br>
5 C<br>
14 R<br>

Total: 92 cobaias<br>
Total de coelhos: 29<br>
Total de ratos: 40<br>
Total de sapos: 23<br>
Percentual de coelhos: 31.52 %<br>
Percentual de ratos: 43.48 %<br>
Percentual de sapos: 25.00 %<br>

=========================CODE=========================

import java.util.Scanner;<br>
<br>
public class Main {<br>
<br>
    public static void main(String[] args) {<br>
        Scanner input =new Scanner(System.in);<br>
        int times = input.nextInt();<br>
        char c;<br>
        int aux;<br>
        int rats=0,rabbits=0,frogs=0, totalAnimals=0;<br>
        while(times>0){<br>
          aux = input.nextInt();<br>
          totalAnimals +=aux;<br>
          c = input.next().charAt(0);<br>
          if (c=='R'){<br>
              rats+=aux;<br>
          }else if (c=='C'){<br>
              rabbits+=aux;<br>
          }else{<br>
              frogs += aux;<br>
          }<br>
          times--;<br>
        }<br>
        Double coelhos = new Double(rabbits);<br>
        Double ratos = new Double(rats);<br>
        Double sapos = new Double(frogs);<br>
        System.out.println("Total: "+totalAnimals+" cobaias");<br>
        System.out.println("Total de coelhos: "+rabbits);<br>
        System.out.println("Total de ratos: "+ rats);<br>
        System.out.println("Total de sapos: "+frogs);<br>
        System.out.printf("Percentual de coelhos: %.2f %%\n",coelhos*100/totalAnimals);<br>
        System.out.printf("Percentual de ratos: %.2f %%\n", (ratos*100/totalAnimals));<br>
        System.out.printf("Percentual de sapos: %.2f %%\n", (sapos*100/totalAnimals));<br>
    }<br>
}<br>