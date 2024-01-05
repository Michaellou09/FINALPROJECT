/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package javaapplication16;

import java.util.Scanner;

/**
 *
 * @author MICHAE LOU LIM
 */
public class JavaApplication16 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Leveling Calculator");
        System.out.println("-------------------");

        // Input known elevation (back sight)
        System.out.print("Enter the elevation of the known point (back sight): ");
        double backSightElevation = scanner.nextDouble();

        // Input rod reading on the known point
        System.out.print("Enter the rod reading on the known point (back sight): ");
        double backSightRodReading = scanner.nextDouble();

        // Input rod reading on the point for which elevation is to be established (foresight)
        System.out.print("Enter the rod reading on the point (foresight): ");
        double foresightRodReading = scanner.nextDouble();

        // Calculate elevation of the point using leveling formula
        double pointElevation = backSightElevation + (backSightRodReading - foresightRodReading);

        // Display the result
        System.out.println("\nElevation of the point: " + pointElevation);

        scanner.close();
    }
}
