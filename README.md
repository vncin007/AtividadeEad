# AtividadeEad
package EAD;

import java.util.Scanner;

public class Metodos_programa1 {

    static Scanner scanner = new Scanner(System.in);

   private int[] numeros = new int[5];

    public int[] getNumeros(int numeros) {

        this.numeros[0] = numeros;
        return new int[0];
    }

    public static void Pedir_numeros(int [] numeros) {

        System.out.println("Digite 5 números:");
        for (int i = 0; i < 5; i++) {
            System.out.print("Número " + (i + 1) + ": ");
            numeros[i] = scanner.nextInt();
        }
    }

    public static void exibir_matriz (int [] numeros) {
        System.out.println("\nOs números digitados foram:");
        for (int num : numeros) {
            System.out.print(num + " ");
        }
    }

}

package EAD;

public class Metodos_programa10 {
    int [] lista = new int[5];
    int [] lista2 = new int[5];
    int [] lista3 = juntarListas(lista, lista2);

    public static int[] juntarListas(int[] lista, int[] lista2) {
        int[] lista3 = new int[lista.length + lista2.length];

        System.arraycopy(lista, 0, lista3, 0, lista.length);
        System.arraycopy(lista2, 0, lista3, lista.length, lista2.length);

        return lista3;
    }

    public static void Exibir(int [] lista3) {

        for (int num : lista3) {
            System.out.print(num + " ");
        }

    }
}

package EAD;

import java.util.Scanner;

public class Metodos_programa11 {


    public static int[][] preencherMatriz(int linhas, int colunas) {
        Scanner scanner = new Scanner(System.in);

        int[][] matriz = new int[linhas][colunas];
        for (int i = 0; i < linhas; i++) {
            for (int j = 0; j < colunas; j++) {
                System.out.print("Digite o número para a posição [" + i + "][" + j + "]: ");
                matriz[i][j] = scanner.nextInt();
            }
        }
        return matriz;
    }

    public static void exibirMatriz(int[][] matriz) {
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println();
        }
    }
}

package EAD;

public class Metodos_programa12 {

    public static int somar_Elementos_Matriz(int[][] matriz) {
        int soma = 0;
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                soma += matriz[i][j];
            }
        }
        return soma;
    }
}

package EAD;

public class Metodos_programa13 {

    public static int encontrarMaiorNUmMatriz(int[][] matriz) {
        int maior = Integer.MIN_VALUE;
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                if (matriz[i][j] > maior) {
                    maior = matriz[i][j];
                }
            }
        }
        return maior;
    }
}

package EAD;

public class Metodos_programa14 {
    int [][] matriz;

    public int[][] getMatriz(int [][] matriz3x3) {
        this.matriz = matriz3x3;
        return matriz;
    }

    public static int somarDiagonalPrincipal(int[][] matriz) {
        int soma = 0;
        for (int i = 0; i < matriz.length; i++) {
            soma += matriz[i][i];
        }
        return soma;
    }
}

package EAD;

public class Metodos_programa15 {
    int [][] matriz3x3;

    public int[][] getMatriz3x3(int [][] matriz3x3) {
        this.matriz3x3 = matriz3x3;
        return matriz3x3;
    }

    public static int somarDiagonalSecundaria(int[][] matriz3x3) {
        int soma = 0;
        for (int i = 0; i < matriz3x3.length; i++) {
            soma += matriz3x3[i][matriz3x3.length - 1 - i];
        }
        return soma;
    }
}

package EAD;

import java.util.Scanner;

import static EAD.Metodos_programa11.exibirMatriz;

public class Metodos_programa16 {


    public static int[][] gerarMatrizIdentidade(int n) {
        int[][] matriz = new int[n][n];
        for (int i = 0; i < n; i++) {
            matriz[i][i] = 1;
        }
        return matriz;
    }

    public static void exibirMatriz(int[][] matriz) {
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println();
        }
    }
}

package EAD;

import java.util.Scanner;

public class Metodos_programa17 {
    public static int[][] preencherMatriz(int linhas, int colunas) {
        Scanner scanner = new Scanner(System.in);
        int[][] matriz = new int[linhas][colunas];
        for (int i = 0; i < linhas; i++) {
            for (int j = 0; j < colunas; j++) {
                System.out.print("Digite o número para a posição [" + i + "][" + j + "]: ");
                matriz[i][j] = scanner.nextInt();
            }
        }
        return matriz;
    }

    public static int[][] multiplicarMatrizPorEscalar(int[][] matriz, int escalar) {
        int[][] matrizResultante = new int[matriz.length][matriz[0].length];
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                matrizResultante[i][j] = matriz[i][j] * escalar;
            }
        }
        return matrizResultante;
    }

    public static void exibirMatriz(int[][] matriz) {
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println();
        }
    }
}

package EAD;

import java.util.Random;

public class Metodos_programa18 {

    public static int[][] gerarMatrizAleatoria(int linhas, int colunas) {
        Random rand = new Random();
        int[][] matriz = new int[linhas][colunas];
        for (int i = 0; i < linhas; i++) {
            for (int j = 0; j < colunas; j++) {
                matriz[i][j] = rand.nextInt(100);
            }
        }
        return matriz;
    }

    public static double calcularMediaMatriz(int[][] matriz) {
        int soma = 0;
        int totalElementos = matriz.length * matriz[0].length;
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                soma += matriz[i][j];
            }
        }
        return soma / (double) totalElementos;
    }
}

package EAD;

public class Metodos_programa19 {

    public static int[][] transporMatriz(int[][] matriz) {
        int[][] matrizTransposta = new int[matriz[0].length][matriz.length];
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                matrizTransposta[j][i] = matriz[i][j];
            }
        }
        return matrizTransposta;
    }

}

package EAD;

import java.util.Scanner;

public class Metodos_programa2 {
    static Scanner scanner = new Scanner(System.in);


    public static int soma (int [] numeros) {
        int soma = 0;

        for (int num : numeros) {
            soma += num;
        }

        return soma;
    }

    public static void exibir_soma (int soma) {

        System.out.println("soma dos valores : " + soma);

    }

}

package EAD;

public class Metodos_programa20 {

    public static void calcularSomaLinhasColunas(int[][] matriz) {

        for (int i = 0; i < matriz.length; i++) {
            int somaLinha = 0;
            for (int j = 0; j < matriz[i].length; j++) {
                somaLinha += matriz[i][j];
            }
            System.out.println("Soma da linha " + i + ": " + somaLinha);
        }

        for (int j = 0; j < matriz[0].length; j++) {
            int somaColuna = 0;
            for (int i = 0; i < matriz.length; i++) {
                somaColuna += matriz[i][j];
            }
            System.out.println("Soma da coluna " + j + ": " + somaColuna);
        }
    }

}

package EAD;

public class Metodos_programa21 {

    public static void fExibirLista(int[] lista) {
        for (int numero : lista) {
            System.out.println("Elemento: " + numero);
        }
    }
}

package EAD;

public class Metodos_programa23 {

    public static void multiplicarListaPorValor(int[] lista, int valor) {
        for (int numero : lista) {
            System.out.println(numero * valor);
        }
    }
}

package EAD;

public class Metodos_programa25 {

    public static void exibir_Nomes(String[] nomes) {
        for (String nome : nomes) {
            System.out.println("Olá, " + nome + "!");
        }
    }
}

package EAD;

public class Metodos_programa26 {

    public static void matrizExibir(int[][] matriz) {
        for (int[] linha : matriz) {
            for (int elemento : linha) {
                System.out.print(elemento + " ");
            }
            System.out.println();
        }
    }
}

package EAD;

public class Metodos_programa27 {

    public static int calcularSomaMatriz(int[][] matriz) {
        int soma = 0;
        for (int[] linha : matriz) {
            for (int elemento : linha) {
                soma += elemento;
            }
        }
        return soma;
    }
}

package EAD;

import java.util.Random;

public class Metodos_programa28 {

    public static int encontrarMaiorElemento(int[][] matriz) {
        int maior = Integer.MIN_VALUE;
        for (int[] linha : matriz) {
            for (int elemento : linha) {
                if (elemento > maior) {
                    maior = elemento;
                }
            }
        }
        return maior;
    }
}

package EAD;

public class Metodos_programa29 {

    public static void calcularSomaPorColuna(int[][] matriz) {
        for (int j = 0; j < matriz[0].length; j++) {
            int somaColuna = 0;
            for (int i = 0; i < matriz.length; i++) {
                somaColuna += matriz[i][j];
            }
            System.out.println("Soma da coluna " + j + ": " + somaColuna);
        }
    }
}

package EAD;

import java.util.Scanner;

public class Metodos_programa3 {
    int soma = 0;
    int [] numeros = new int[6];
    int media = media_da_Matriz(soma, numeros);

    public int[] getNumeros(int [] numeros) {
        this.numeros = numeros;
        return numeros;
    }

    public int getSoma(int soma) {
        this.soma = soma;
        return soma;
    }

    public static void Pedir_6numeros(int [] numeros) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite 6 números:");
        for (int i = 0; i < numeros.length; i++) {
            System.out.print("Número " + (i + 1) + ": ");
            numeros[i] = scanner.nextInt();
        }
        scanner.close();
    }

    public static int media_da_Matriz(int soma, int [] numeros) {

        return soma / numeros.length;
    }

    public static void exibir_media (int media) {

        System.out.println("A média dos valores desta matriz é: " + media);

    }
}

package EAD;

public class Metodos_programa30 {
    public static void substituirNegativosPorZero(int[] lista) {
        for (int i = 0; i < lista.length; i++) {
            if (lista[i] < 0) {
                lista[i] = 0;
            }
        }
    }

}

package EAD;
import java.util.Random;

public class Metodos_programa4 {


    private int[] numeros = new int[10];
    private int numer_maior = encontrarMaior(numeros);
    private int numer_menor = encontrarMenor(numeros);


    public int getNumer_maior() {
        return numer_maior;
    }
    public int getNumer_menor() {
        return numer_menor;
    }

    public static void preencher_matriz_comNumero_aleatorio(int [] numeros) {
        Random random = new Random();

        for (int i = 0; i < numeros.length; i++) {
            numeros[i] = random.nextInt(100) + 1;
        }

    }

    public static int encontrarMenor(int[] numeros) {
        int menor = numeros[0];
        for (int num : numeros) {
            if (num < menor) {
                menor = num;
            }
        }
        return menor;
    }

    public static int encontrarMaior(int[] numeros) {
        int maior = numeros[0];
        for (int num : numeros) {
            if (num > maior) {
                maior = num;
            }
        }
        return maior;
    }

    public static void exibir_matriz(int [] numeros) {

        for (int num : numeros) {
            System.out.print(num + " ");
        }

    }


    public static void exibir_maior_menor (int numer_maior, int numer_menor) {
        System.out.println("\nMaior número: " + numer_maior);
        System.out.println("Menor número: " + numer_menor);
    }

}

package EAD;

public class Metodos_programa5 {
    private int n;
    private int [] lista ;
    private  boolean encontrado = procurar_numero_na_lista(n,lista);



    public static boolean procurar_numero_na_lista(int n,int[] lista) {
        boolean encontrado = false;

        for (int num : lista) {
            if (num == n) {
                encontrado = true;
            }else {
                encontrado = false;
            }
        }

        return encontrado;
    }

    public static void encontrado_Naoencontrado(boolean encontrado) {
        if (encontrado) {
            System.out.println("Encontrado na lista");
        }else {
            System.out.println("Não encontrado na lista");
        }

    }

    public boolean isEncontrado() {
        return encontrado;
    }

    public void setEncontrado(boolean encontrado) {
        this.encontrado = encontrado;
    }
}

package EAD;
import java.util.*;
public class Metodos_programa6 {
    int [] lista;

    public int[] getLista(int [] lista) {
        this.lista = lista;
        return lista;
    }

    public static void retirar_impares (int [] lista) {
            List<Integer> novaLista = new ArrayList<>();

            for (int num : lista) {
                if (num % 2 == 0) {
                    novaLista.add(num);
                }
            }

            System.out.println("Lista sem números ímpares: " + novaLista);
        }


}

package EAD;

import java.util.Arrays;
import java.util.Scanner;

public class Metodos_programa7 {

    int[] numeros = new int[8];


    public static void pedir_8numeros(int[] numeros) {
        Scanner scanner = new Scanner(System.in);

        for (int i = 0; i < 8; i++) {

            System.out.print("Digite o " + (i + 1) + "º número: ");
            numeros[i] = scanner.nextInt();


        }
    }
    public static void ordenarNumeros(int[] numeros) {
        Arrays.sort(numeros);
    }

    public static void imprimirNumeros(int[] numeros) {
        System.out.print("Números em ordem crescente: ");
        for (int numero : numeros) {
            System.out.print(numero + " ");
        }
        System.out.println();
    }
}

package EAD;
import java.util.*;
import java.util.Scanner;

public class Metodos_programa8 {
    Scanner scanner = new Scanner(System.in);

    String [] nomes = new String[5];

    public String[] getNomes(String [] nomes) {
        this.nomes = nomes;
        return nomes;
    }

    public static String[] pedir_5nomes (String[] nomes) {
        Scanner scanner = new Scanner(System.in);


        for (int i = 0; i < 5; i++) {
            System.out.print("Digite o " + (i + 1) + "º nome: ");
            nomes[i] = scanner.nextLine();
        }

        return nomes;
    }

    public static void Ordem_alfabetica (String[] nomes) {
        Arrays.sort(nomes);

        System.out.println("Nomes em ordem alfabética: ");
        for (String nome : nomes) {
            System.out.println(nome);
        }

    }
}

package EAD;

import java.util.Scanner;

public class Metodos_programa9 {

    int [] numeros = new int[7];

    public int[] getNumeros(int [] numeros) {
        this.numeros = numeros;
        return numeros;
    }

    public static void pedir_7numeros(int[] numeros) {
        Scanner scanner = new Scanner(System.in);

        for (int i = 0; i < 7; i++) {

            System.out.print("Digite o " + (i + 1) + "º número: ");
            numeros[i] = scanner.nextInt();

        }

    }

    public static void lista_inversa (int [] numeros) {
        int inicio = 0;
        int fim = numeros.length - 1;

        while (inicio < fim) {
            int temp = numeros[inicio];
            numeros[inicio] = numeros[fim];
            numeros[fim] = temp;

            inicio++;
            fim--;
        }
    }
    public static void imprimirNum_inverso(int[] numeros) {
        System.out.print("Lista na ordem inversa: ");
        for (int numero : numeros) {
            System.out.print(numero + " ");
        }
        System.out.println();
    }
}

package EAD;

import java.util.Scanner;

public class Programa1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int[] numeros = new int[5];

        Metodos_programa1.Pedir_numeros(numeros);
        Metodos_programa1.exibir_matriz(numeros);

        scanner.close();
    }
}

package EAD;

public class Programa10 {
    public static void main(String[] args) {
        int [] lista = new int[5];
        int [] lista2 = new int[5];

        Metodos_programa1.Pedir_numeros(lista);
        Metodos_programa1.exibir_matriz(lista);
        System.out.println(" ");
        Metodos_programa1.Pedir_numeros(lista2);
        System.out.println(" ");
        int [] lista3 = Metodos_programa10.juntarListas(lista,lista2);
        Metodos_programa10.Exibir(lista3);
    }

}

package EAD;

import static EAD.Metodos_programa11.exibirMatriz;

public class Programa11 {
    public static void main(String[] args) {

        int[][] matriz3x3 = Metodos_programa11.preencherMatriz(3, 3);
        exibirMatriz(matriz3x3);
    }
}

package EAD;

public class Programa12 {
    public static void main(String[] args) {

        int[][] matriz3x3 = Metodos_programa11.preencherMatriz(3, 3);
        int soma = Metodos_programa12.somar_Elementos_Matriz(matriz3x3);
        System.out.println("Soma de todos os elementos da matriz 3x3: " + soma);
    }


}

package EAD;

public class Programa13 {
    public static void main(String[] args) {

        int[][] matriz3x3 = Metodos_programa11.preencherMatriz(3, 3);
        int maiorElemento = Metodos_programa13.encontrarMaiorNUmMatriz(matriz3x3);

        System.out.println("Maior elemento da matriz 3x3: " + maiorElemento);

    }
}

package EAD;

public class Programa14 {
    public static void main(String[] args) {

        int[][] matriz3x3 = Metodos_programa11.preencherMatriz(3,3);
        int somaDiag = Metodos_programa14.somarDiagonalPrincipal(matriz3x3);
        System.out.println("Soma da diagonal principal: " + somaDiag);
    }
}

package EAD;

public class Programa15 {
    public static void main(String[] args) {

        int[][] matriz3x3 = Metodos_programa11.preencherMatriz(3,3);
        int somaDiagonalSecundaria = Metodos_programa15.somarDiagonalSecundaria(matriz3x3);
        System.out.println("Soma da diagonal secundária: " + somaDiagonalSecundaria);

    }
}

package EAD;

import java.util.Scanner;

public class Programa16 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Digite o tamanho da matriz identidade: ");
        int n = scanner.nextInt();
        int[][] matrizIdentidade = Metodos_programa16.gerarMatrizIdentidade(n);
        Metodos_programa16.exibirMatriz(matrizIdentidade);
    }
}

package EAD;

import java.util.Scanner;

public class Programa17 {
    public static void main(String[] args) {
        int[][] matriz3x3 = Metodos_programa17.preencherMatriz(3, 3);
        Scanner scanner = new Scanner(System.in);
        System.out.print("Digite o número escalar: ");
        int escalar = scanner.nextInt();

        int[][] matrizEscalar = Metodos_programa17.multiplicarMatrizPorEscalar(matriz3x3, escalar);
        Metodos_programa17.exibirMatriz(matrizEscalar);
    }
}

package EAD;

public class Programa18 {
    public static void main(String[] args) {
        int[][] matriz4x4 = Metodos_programa18.gerarMatrizAleatoria(4, 4);
        double media = Metodos_programa18.calcularMediaMatriz(matriz4x4);
        System.out.println("Média de todos os elementos da matriz 4x4: " + media);
    }
}

package EAD;

public class Programa19 {
    public static void main(String[] args) {
        int[][] matriz3x3 = Metodos_programa11.preencherMatriz(3, 3);
        int[][] matrizTransposta = Metodos_programa19.transporMatriz(matriz3x3);
        Metodos_programa17.exibirMatriz(matrizTransposta);
    }
}

package EAD;

public class Programa2 {
    public static void main(String[] args) {

        int[] numeros = new int[5];

        Metodos_programa1.Pedir_numeros(numeros);
        int soma = Metodos_programa2.soma(numeros);
        Metodos_programa2.exibir_soma(soma);

    }

}

package EAD;

public class Programa20 {
    public static void main(String[] args) {
        int[][] matriz4x4 = Metodos_programa18.gerarMatrizAleatoria(4, 4);
        Metodos_programa11.exibirMatriz(matriz4x4);
        Metodos_programa20.calcularSomaLinhasColunas(matriz4x4);
    }
}

package EAD;

public class Programa21 {
    public static void main(String[] args) {

        int[] numeros = {1, 2, 3, 4, 5};
        Metodos_programa21.fExibirLista(numeros);

    }
}

package EAD;

public class Programa22 {
    public static void main(String[] args) {
        int [] num = new int[5];

        Metodos_programa4.preencher_matriz_comNumero_aleatorio(num);
        Metodos_programa4.exibir_matriz(num);
        int soma = Metodos_programa2.soma(num);
        Metodos_programa2.exibir_soma(soma);

    }
}

package EAD;

import java.util.Scanner;

public class Programa23 {
    public static void main(String[] args) {
        int[] numeros = {1, 2, 3, 4, 5};
        Scanner scanner = new Scanner(System.in);
        System.out.print("Digite um valor para multiplicar: ");
        int valor = scanner.nextInt();
        Metodos_programa23.multiplicarListaPorValor(numeros, valor);
    }
}

package EAD;

public class Programa24 {
    public static void main(String[] args) {

        int [] lista = new int[10];
        Metodos_programa4.preencher_matriz_comNumero_aleatorio(lista);
        Metodos_programa4.exibir_matriz(lista);
        System.out.println(" ");
        Metodos_programa6.retirar_impares(lista);


    }
}

package EAD;

public class Programa25 {
    public static void main(String[] args) {
        String[] nomes = {"Isaque", "Joabe", "Abner", "Rodrigues", "Avelar"};
        Metodos_programa25.exibir_Nomes(nomes);

    }
}

package EAD;

public class Programa26 {
    public static void main(String[] args) {
        int[][] matriz3x3 = {
                {1, 2, 3},
                {4, 5, 6},
                {7, 8, 9}
        };

        Metodos_programa26.matrizExibir(matriz3x3);

    }
}

package EAD;

public class Programa27 {
    public static void main(String[] args) {

        int[][] matriz4x4 = {
                {1, 2, 3, 4},
                {5, 6, 7, 8},
                {9, 10, 11, 12},
                {13, 14, 15, 16}
        };
        int soma = Metodos_programa27.calcularSomaMatriz(matriz4x4);
        System.out.println("Soma de todos os elementos da matriz 4x4: " + soma);
    }
}

package EAD;

public class Programa28 {
    public static void main(String[] args) {
        int[][] matriz3x3 = Metodos_programa18.gerarMatrizAleatoria(3, 3);
        int maiorElemento = Metodos_programa28.encontrarMaiorElemento(matriz3x3);
        System.out.println("O maior elemento da matriz 3x3 é: " + maiorElemento);
    }
}

package EAD;

public class Programa29 {
    public static void main(String[] args) {

        int[][] matriz4x4 = Metodos_programa18.gerarMatrizAleatoria(4, 4);
        Metodos_programa29.calcularSomaPorColuna(matriz4x4);
    }
}

package EAD;

public class Programa3 {
    public static void main(String[] args) {

        int [] numeros = new int[6];

        Metodos_programa3.Pedir_6numeros(numeros);
        int soma  = Metodos_programa2.soma(numeros);
        int media = Metodos_programa3.media_da_Matriz(soma,numeros);
        Metodos_programa3.exibir_media(media);
    }
}

package EAD;

public class Programa30 {
    public static void main(String[] args) {
        int[] numeros = {-5, 3, -2, 4, -7, 6};
        Metodos_programa30.substituirNegativosPorZero(numeros);
        Metodos_programa1.exibir_matriz(numeros);
    }
}

package EAD;

public class Programa4 {
    public static void main(String[] args) {
        int[] numeros = new int[10];

        Metodos_programa4.preencher_matriz_comNumero_aleatorio(numeros);
        int numMaior = Metodos_programa4.encontrarMaior(numeros);
        int numMenor = Metodos_programa4.encontrarMenor(numeros);
        Metodos_programa4.exibir_matriz(numeros);
        Metodos_programa4.exibir_maior_menor(numMaior,numMenor);

    }
}

package EAD;

import java.util.Scanner;

public class Programa5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int [] lista = new int[10];

        Metodos_programa4.preencher_matriz_comNumero_aleatorio(lista);
        Metodos_programa4.exibir_matriz(lista);
        System.out.println(" ");
        System.out.println("Digite um número:");
        int n = sc.nextInt();
        boolean encontrado = Metodos_programa5.procurar_numero_na_lista(n,lista);
        Metodos_programa5.encontrado_Naoencontrado(encontrado);


    }
}

package EAD;

public class Programa6 {
    public static void main(String[] args) {
        int [] lista = new int[10];

        Metodos_programa4.preencher_matriz_comNumero_aleatorio(lista);
        Metodos_programa1.exibir_matriz(lista);
        System.out.println(" ");
        Metodos_programa6.retirar_impares(lista);
    }
}

package EAD;

public class Programa7 {
    public static void main(String[] args) {
        int [] num = new int[8];

       Metodos_programa7.pedir_8numeros(num);
       Metodos_programa1.exibir_matriz(num);
        System.out.println(" ");
       Metodos_programa7.ordenarNumeros(num);
       Metodos_programa7.imprimirNumeros(num);

    }
}

package EAD;

public class Programa8 {
    public static void main(String[] args) {
        String [] nomes = new String[5];

        Metodos_programa8.pedir_5nomes(nomes);
        Metodos_programa8.Ordem_alfabetica(nomes);

    }
}

package EAD;

public class Programa9 {
    public static void main(String[] args) {
        int [] numeros = new int[7];

        Metodos_programa9.pedir_7numeros(numeros);
        Metodos_programa1.exibir_matriz(numeros);
        System.out.println(" ");
        Metodos_programa9.lista_inversa(numeros);
        Metodos_programa9.imprimirNum_inverso(numeros);
    }

}
