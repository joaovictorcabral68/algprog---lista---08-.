# 1.
```java
import java.util.Scanner;

public class Main {

    public static void imprimirPadrao(int n) {

        for (int i = 1; i <= n; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print(i + " ");
            }

            System.out.println();
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite o valor de n: ");
        int n = sc.nextInt();

        imprimirPadrao(n);

        sc.close();
    }
}

```

# 2.

import java.util.Scanner;

public class Main {

    public static void imprimirPadrao(int n) {

        for (int i = 1; i <= n; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }

            System.out.println();
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite o valor de n: ");
        int n = sc.nextInt();

        imprimirPadrao(n);

        sc.close();
    }
}

# 3.

```java

import java.util.Scanner;

public class Main {

    public static int somar(int a, int b, int c) {
        return a + b + c;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite o primeiro número: ");
        int n1 = sc.nextInt();

        System.out.print("Digite o segundo número: ");
        int n2 = sc.nextInt();

        System.out.print("Digite o terceiro número: ");
        int n3 = sc.nextInt();

        int resultado = somar(n1, n2, n3);

        System.out.println("Soma dos três números: " + resultado);

        sc.close();
    }
}

```

# 4.

```java

import java.util.Scanner;

public class Main {

    public static char verificarNumero(int n) {

        if (n > 0) {
            return 'P';
        } else {
            return 'N';
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite um número: ");
        int numero = sc.nextInt();

        char resultado = verificarNumero(numero);

        System.out.println("Resultado: " + resultado);

        sc.close();
    }
}

```

# 5.

```java

import java.util.Scanner;

public class Main {

    public static double somaImposto(double taxaImposto, double custo) {
        return custo + (custo * taxaImposto / 100);
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite o custo do item: ");
        double custo = sc.nextDouble();

        System.out.print("Digite a taxa de imposto (%): ");
        double taxa = sc.nextDouble();

        double custoFinal = somaImposto(taxa, custo);

        System.out.println("Custo com imposto: " + custoFinal);

        sc.close();
    }
}

```

# 6.

```java

import java.util.Scanner;

public class Main {

    // Função de conversão
    public static void converterHora(int hora24, int minuto) {

        char periodo;
        int hora12;

        if (hora24 == 0) {
            hora12 = 12;
            periodo = 'A';
        }
        else if (hora24 == 12) {
            hora12 = 12;
            periodo = 'P';
        }
        else if (hora24 > 12) {
            hora12 = hora24 - 12;
            periodo = 'P';
        }
        else {
            hora12 = hora24;
            periodo = 'A';
        }

        imprimirHora(hora12, minuto, periodo);
    }

    // Função de saída
    public static void imprimirHora(int hora, int minuto, char periodo) {

        System.out.printf("Hora convertida: %d:%02d ", hora, minuto);

        if (periodo == 'A') {
            System.out.println("A.M.");
        } else {
            System.out.println("P.M.");
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        String continuar;

        do {
            System.out.print("Digite a hora (0-23): ");
            int hora = sc.nextInt();

            System.out.print("Digite os minutos: ");
            int minuto = sc.nextInt();

            converterHora(hora, minuto);

            System.out.print("\nDeseja converter outra hora? (s/n): ");
            continuar = sc.next();

            System.out.println();

        } while (continuar.equalsIgnoreCase("s"));

        System.out.println("Programa encerrado.");

        sc.close();
    }
}

```


