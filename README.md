# Calculo-idade-altura-e-peso-codigo-em-Java

Considere o seguinte problema:

Faça um programa que receba a idade, a altura e o peso de 25 pessoas, calcule e mostre:

a quantidade de pessoas com idade superior a 50 anos;
a média das alturas das pessoas com idade entre 10 e 20 anos;
a percentagem de pessoas com peso inferior a 40 quilos entre todas as pessoas analisadas.
Complete o programa abaixo, arrastando e soltando os trechos de código nos espaços vazios de forma que o problema acima seja implementado de forma correta.



public class AnalisePessoas {
	public static void main(String[] args) {
		int quantMaior50 = 0, quantEntre10e20 = 0, quantInf40Kg = 0;
		[double somaAlturas = 0;]
		
		[for(int cont = 1; cont <= 25; cont++)] {
			System.out.printf("------------------------ PESSOA %02d ------------------------\n", cont);
			System.out.print("Idade: ");
			int idade = Integer.parseInt(System.console().readLine());
			System.out.print("Altura: ");
			double altura = Double.parseDouble(System.console().readLine());
			System.out.print("Peso: ");
			double peso = Double.parseDouble(System.console().readLine());
			
			[if(idade > 50)]
				[quantMaior50++;]
			else [if(idade >= 10 && idade <= 20)] {
				somaAlturas += altura;
				[quantEntre10e20++;]
			}
			
			if(peso < 40)
				quantInf40Kg++;
		}
		
		double mediaAlturas = somaAlturas / quantEntre10e20;
		double percInf40Kg = quantInf40Kg * 100.0 / 25;
		
		System.out.printf("\nQUANTIDADE DE PESSOAS COM MAIS DE 50 ANOS = %d\n", quantMaior50);
		System.out.printf("MEDIA DAS ALTURAS DAS PESSOAS ENTRE 10 E 20 ANOS = %.2f metros\n", mediaAlturas);
		System.out.printf("PERCENTAGEM DE PESSOAS COM MENOS DE 40 KG = %.1f%%\n", percInf40Kg);
	}
}
