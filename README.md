package javaapplication1;

import java.util.Scanner;

public class JavaApplication1 {

    
    public static void main(String[] args) {
        int valor;
        do{
            System.out.println("Qual valor?");
            Scanner sc1 = new Scanner(System.in);
            valor = sc1.nextInt();
        }while(valor<3);
        
        int[][] matriz = new int[valor][valor];
        int contador = 0;
        String[] letras = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"};
        
        for(int linha = 0;linha<=valor;linha++) {//Defini a linha
            if(linha == 1){//Preenche todas as colunas da linha
                for(int coluna=0;coluna<valor;coluna++) {//defini a coluna
                    if(contador == 25){//contador do alfabeto
                        System.out.print(letras[contador]+ '\t');//printa a letra
                        contador = 0;
                    }else {
                        System.out.print(letras[contador]+ '\t');
                        contador = contador+1;        
                    }
                }
            }else if(linha == valor) {//preenche apenas a coluna certa para formar o Z
                for(int coluna=0;coluna<valor;coluna++) {
                    if(contador == 25){
                        System.out.print(letras[contador]+ '\t');
                        contador = 0;
                    }else {
                        System.out.print(letras[contador]+ '\t');
                        contador = contador+1;
                            
                    }
                }
            }else { //preenche todas as colunas da ultima linha
                for(int coluna=0;coluna<valor;coluna++) {
                    if(coluna == valor - linha){
                        if(contador == 25){
                            System.out.print(letras[contador]+ '\t');
                            contador = 0;
                        }else {
                            System.out.print(letras[contador]+ '\t');
                            contador = contador+1;           
                        }
                    }else {
                        System.out.print("\t");
                    }
                }
            }
            System.out.println();
        }
    }
    
}

