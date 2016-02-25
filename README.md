# Taller-1
Taller 1 de POO. Ejercicio del Triangulo.
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package triangulo;

import java.util.Scanner;
public class Triangulo {
    private Scanner teclado;
    private int x1,y1,x2,y2,x3,y3;
    private double lado1,lado2,lado3,per,semiper,areatri,h1,h2,h3;

public void ingpuntos(){
    teclado=new Scanner(System.in);
    System.out.println("---COORDENADAS DEL TRIÁNGULO---");
    System.out.println("PUNTO A:");
    System.out.print("Coordenada x1:");
    x1= teclado.nextInt();
    System.out.print("Coordenada y1:");
    y1= teclado.nextInt();
    System.out.println("PUNTO B:");
    System.out.print("Coordenada x2:");
    x2= teclado.nextInt();
    System.out.print("Coordenada y2:");
    y2= teclado.nextInt();
    System.out.println("PUNTO C:");
    System.out.print("Coordenada x3:");
    x3= teclado.nextInt();
    System.out.print("Coordenada y3:");
    y3= teclado.nextInt();
}
public void distancialados(){

    lado1=Math.sqrt(Math.abs(Math.pow((x2-x1),2)+Math.pow((y2-y1),2))); 
    System.out.println("Distancia Lado 1 = " + lado1);
    lado2=Math.sqrt(Math.abs(Math.pow((x3-x2),2)+Math.pow((y3-y2),2))); 
    System.out.println("Distancia Lado 2 = " + lado2);
    lado3=Math.sqrt(Math.abs(Math.pow((x1-x3),2)+Math.pow((y1-y3),2))); 
    System.out.println("Distancia Lado 3 = " + lado3);
    }
public void sumper(){
    per=(lado1+lado2+lado3);
    System.out.println("El Perímero del Triángulo es = " + per);
   
}
public void semiperimetro(){
    semiper=((lado1+lado2+lado3)/2);
     System.out.println("El Semiperímero del Triángulo es = " + semiper);
}
 public void areatriangulo(){
    areatri=Math.sqrt(semiper*(semiper-lado1)*(semiper-lado2)*(semiper-lado3));
     System.out.println("El Área del Triángulo es = " +areatri+ " Unidades cuadradas");
}    
 public void alturatriangulo(){
     h1=((2*areatri)/lado1);
     System.out.println("La altura del Triángulo del Punto A al Lado 2 es: " + h1);
     h2=((2*areatri)/lado2);
     System.out.println("La altura del Triángulo del Punto B al Lado 3 es: " + h2);
     h3=((2*areatri)/lado3);
     System.out.println("La altura del Triángulo del Punto C al Lado 1 es: " + h3);
}
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Triangulo triangulo1 = new Triangulo();
        triangulo1.ingpuntos();
        triangulo1.distancialados();
        triangulo1.sumper();
        triangulo1.semiperimetro();
        triangulo1.areatriangulo();
        triangulo1.alturatriangulo();
        // TODO code application logic here
    }
    
}
