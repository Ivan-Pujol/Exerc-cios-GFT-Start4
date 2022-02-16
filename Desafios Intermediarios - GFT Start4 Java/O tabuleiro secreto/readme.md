import java.io.BufferedReader;<br>
import java.io.IOException;<br>
import java.io.InputStreamReader;<br>
import java.util.HashMap;<br>
import java.util.Map;<br>
 <br>
public class TabuleiroSecreto {<br>
    public static void main(String[] args) throws IOException {<br>
      BufferedReader br = new BufferedReader(new InputStreamReader(System.in));<br>
        String[] nq = br.readLine().split(" ");<br>
        int tamTab = Integer.parseInt(nq[0]);<br>
        int numOp = Integer.parseInt(nq[1]);<br>
        int[][] matriz = new int[tamTab][tamTab];<br>
        <br>
        for (int i = 0; i < tamTab ; i++) {<br>
            for (int j = 0; j < tamTab; j++) {<br>
                matriz[i][j] = 0;<br>
            }<br>
        }<br>
        <br>
        for (int i = 0; i < numOp; i++) {<br>
            String[] operacao = br.readLine().split(" ");<br>
            int tipoOp = Integer.parseInt(operacao[0]);<br>
            int linha = Integer.parseInt(operacao[1]);<br>
            int valor = 0;<br>
            <br>
            if(operacao.length == 3) {<br>
                valor = Integer.parseInt(operacao[2]);<br>
            }<br>
            <br>
            switch (tipoOp) {<br>
                case 1: atribuiLinhaX(linha, valor, matriz); break;<br>
                case 2: atribuiColunaX(linha, valor, matriz); break;<br>
                case 3: imprimirFrequenteLinhaX(linha, matriz); break;<br>
                case 4: imprimirFrequenteColunaX(linha, matriz); break;<br>
            }<br>
        }<br>
    }<br>
    <br>
    private static void imprimirFrequenteColunaX(int col,<br>
                                                 int[][] matriz) {<br>
        Map<Integer, Integer> map = new HashMap<>();<br>
        map.put(matriz[0][col-1], 1);<br>
    <br>
        for (int i = 1; i < matriz.length; i++) {<br>
            if(map.containsKey(matriz[i][col-1])){<br>
                map.put(matriz[i][col-1], map.get(matriz[i][col-1])+1);<br>
            } else {<br>
                map.put(matriz[i][col-1], 1);<br>
            }<br>
        }<br>
    <br>
        var key = map.entrySet().stream().max((entry1, entry2) -> entry1.getValue() > entry2.getValue() ? 1 : -1).get().getKey();<br>
        <br>
        if(map.get(key) == 1){<br>
            key = map.entrySet().stream().max((entry1, entry2) -> entry1.getKey() > entry2.getKey() ? 1 : -1).get().getKey();<br>
        }<br>
        <br>
        System.out.println(key);<br>
    }<br>
    <br>
    private static void imprimirFrequenteLinhaX(int linha,<br>
                                                int[][] matriz) {<br>
        Map<Integer, Integer> map = new HashMap<>();<br>
        map.put(matriz[linha-1][0], 1);<br>
        <br>
        for (int i = 1; i < matriz.length; i++) {<br>
            if(map.containsKey(matriz[linha-1][i])){<br>
                map.put(matriz[linha-1][i], map.get(matriz[linha-1][i])+1);<br>
            } else {<br>
                map.put(matriz[linha-1][i], 1);<br>
            }<br>
        }<br>
    <br>
        var key = map.entrySet().stream().max((entry1, entry2) -> entry1.getValue() > entry2.getValue() ? 1 : -1).get().getKey();<br>
        <br>
        if(map.get(key) == 1){<br>
            key = map.entrySet().stream().max((entry1, entry2) -> entry1.getKey() > entry2.getKey() ? 1 : -1).get().getKey();<br>
        }<br>
        <br>
        System.out.println(key);<br>
    }<br>
    <br>
    private static void atribuiColunaX(int col,<br>
                                       int valor,<br>
                                       int[][] matriz) {<br>
        for (int i = 0; i < matriz.length; i++) {<br>
            matriz[i][col-1] = valor;<br>
        }<br>
    }<br>
    <br>
    private static void atribuiLinhaX(int linha,<br>
                                      int valor,<br>
                                      int[][] matriz) {<br>
        for (int i = 0; i < matriz.length; i++) {<br>
            matriz[linha-1][i] = valor;<br>
        }<br>
    }<br>
}<br>