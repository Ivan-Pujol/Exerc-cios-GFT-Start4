#Desafios Básicos - GFT Start #4 Java
3 / 3 - Visita na Feira
Desafio
Você está na feira com a sua sacola e parou em uma banca. O feirante lhe entregou pimentões amarelos e vermelhos. Agora iremos somar os pimetões amarelos e vermelhos para descobrir o total de pimentões na sacola.  Você receberá 2 inteiros que devem ser lidos e armazenados nas variáveis A (pimentões amarelos) e B (pimentões vermelhos). Faça a soma de A e B atribuindo o seu resultado na variável X (total de pimentões). Apresente X como descrito na mensagem de exemplo abaixo. Não apresente outra mensagem além da mensagem especificada.

Entrada
A entrada contém 2 valores inteiros, separados por um espaço.

Saída
Imprimir a mensagem "X = " (sendo a letra X maiúscula) seguido pelo valor da variável X e pelo final de linha. Assegure que exista um espaço antes e depois do sinal de igualdade.

 
Exemplos de Entrada	Exemplos de Saída
11 7			>>>> X = 18 <br>
-11 6			>>>> X = -5 <br>
11 -2			>>>> X = 9 <br>

=========================CODE=========================
import java.util.Scanner;<br>

<br>
public class Main {<br>
  public static void main(String[] args){<br>
    <br>
    Scanner leitor = new Scanner(System.in);<br>
    <br>
    
    int a = leitor.nextInt();<br>
    int b = leitor.nextInt();<br>
    <br>
  int x = a + b;//digite o seu código<br>
  System.out.println("X = "+x);<br>
  }<br>
}<br>

