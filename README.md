package pagomensual;

import java.util.Scanner;

/**
 * Programa que calcula el pago mensual y total de una compra
 * utilizando una progresión geométrica, basado en el método de las 6D.
 */
public class PagoMensual {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int N = solicitarNumeroMeses(scanner);
        double pagoInicial = solicitarPagoInicial(scanner);
        
        calcularYMostrarPagos(N, pagoInicial);
        
        scanner.close();
    }
    
    // Método para solicitar el número de meses
    private static int solicitarNumeroMeses(Scanner scanner) {
        System.out.print("Ingrese el número de meses (N): ");
        return scanner.nextInt();
    }
    
    // Método para solicitar el pago inicial
    private static double solicitarPagoInicial(Scanner scanner) {
        System.out.print("Ingrese el pago inicial: ");
        return scanner.nextDouble();
    }
    
    // Método para calcular y mostrar los pagos
    private static void calcularYMostrarPagos(int N, double pagoInicial) {
        double totalPagado = 0;
        double pagoMensual = pagoInicial;
        
        System.out.println("\nDetalle de pagos:");
        for (int i = 1; i <= N; i++) {
            System.out.printf("Mes %d: $%.2f\n", i, pagoMensual);
            totalPagado += pagoMensual;
            pagoMensual *= 2; // Duplica el pago para el siguiente mes
        }
        
        System.out.printf("\nTotal a pagar después de %d meses: $%.2f\n", N, totalPagado);
    }
}
