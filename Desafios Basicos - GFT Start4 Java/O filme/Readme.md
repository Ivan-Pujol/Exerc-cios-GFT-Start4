# Desafios Básicos - GFT Start #4 Java
2 / 3 - O Filme
<p>
Bem-vindo à 3ạ Maratona de Programação Júnior da UFFS. Esperamos sinceramente que as próximas horas sejam muito produtivas para você, que você faça muitos balões e que, acima de tudo, você se divirta! Lembre que você sempre pode pedir esclarecimento quando não entender direito a descrição de um problema. Lembre também que às 17:30 os juízes automáticos serão desligados e a competição entrará em modo blind, de modo que todas as submissões neste período só começarão a ser julgadas às 18:10. Por favor, fique conosco até o fim da competição, trabalhando nas soluções dos problemas até o último minuto, pois, enquanto a competição ainda está ocorrendo, sempre há esperança!

E foi esperança que motivou a Vovó Zazá, uma senhora de 72 anos, a realizar seu sonho de começar um curso universitário. Ela está fascinada com tudo o que diz respeito à Universidade: com as aulas, com a biblioteca, com os projetos de pesquisa e extensão, com o restaurante universitário, mas especialmente com a carteirinha de estudante que ela pode utilizar para pagar meia entrada no cinema. Semana passada, Vovó Zazá e seus colegas de turma foram ao cinema assistir a um filme, mas ficaram estarrecidos com o aumento do preço do ingresso. Revoltados, eles decidiram fazer uma manifestação contra o sistema capitalista opressor, agendada para amanhã na Praça General Bertaso. Vovó Zazá quer colaborar com o movimento fazendo um cartaz com a seguinte palavra de ordem:

QUE ABSURDO! O PREÇO DO CINEMA SUBIU … % !!

Mas ela não é muito boa em Matemática, e está solicitando sua ajuda para calcular a porcentagem de que precisa para completar o cartaz.

Entrada
A única linha da entrada consiste de dois valores A e B (0.00 < A ≤ B ≤ 1000.00), os quais, fornecidos com exatos dois dígitos após o ponto separador decimal, representam respectivamente o valor antigo e o valor novo do ingresso do cinema.

Saída
A única linha da saída deve consistir unicamente de um valor, que represente como uma porcentagem o aumento do valor do ingresso. O valor deve ser acompanhado do símbolo % e conter exatos dois dígitos após o ponto separador decimal.

</p> 
Exemplos de Entrada	Exemplos de Saída <br>
20.00 30.00     >>>> 50.00%<br>
50.00 100.00    >>>> 100.00%<br>
10.00 10.00     >>>> 0.00%<br>

3ạ Maratona de Programação Júnior da UFFS<br>

=========================CODE========================

import java.io.IOException;<br>
import java.util.Scanner;<br>
<br>
public class DIO {<br>
	<br>
    public static void main(String[] args) throws IOException {<br>
    	Scanner leitor = new Scanner(System.in);<br>
    	double a = leitor.nextDouble();<br>
    	double b = leitor.nextDouble();<br>
    	//Escreva aqui a sua lógica<br>		
    	double result  = (b-a)/a*100;<br>
    	System.out.printf("%.2f",result);<br>
    	System.out.println("%");<br>
      <br>
    }<br>
	<br>
}<br>