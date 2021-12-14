# Programação Orientada a Objetos - Nelio Alves

## 64. Resolvendo um Problema sem POO

```java
package application;

import java.util.Locale;
import java.util.Scanner;

public class Program {

	public static void main(String[] args) {
		
		Locale.setDefault(Locale.US);
		Scanner input = new Scanner(System.in);
		
		double xA, xB, xC, yA, yB, yC;
		
		double p = 0;
		
		System.out.println("Enter the measures of triangle X: ");
		xA = input.nextDouble();
		xB = input.nextDouble();
		xC = input.nextDouble();
		
		System.out.println("Enter the measures of triangle X: ");
		yA = input.nextDouble();
		yB = input.nextDouble();
		yC = input.nextDouble();
		
		p = (xA + xB + xC) / 2.0;
		double areaX = Math.sqrt(p * (p - xA) * (p - xB) * (p - xC));
		
		p = (yA + yB + yC) / 2.0;
		double areaY = Math.sqrt(p * (p - yA) * (p - yB) * (p - yC));
		
		System.out.printf("Triangle X Area: %.4f%n", areaX);
		System.out.printf("Triangle Y Area: %.4f%n", areaY);
		
		if(areaX > areaY) {
			System.out.println("Larger area: X");
		}else {
			System.out.println("Larger area: Y");
		}
		
		input.close();
	}

}

```

---

## 65. Criando uma classe com três atributos para apresentar melhor o triângulo

→ O triângulo é uma entidade com três atributos: a, b e c.

Estamos usando três variáveis para representar cada triângulo. (xA, xB, xC, yA...).

Para melhorar isso, vamos usar uma CLASSE para representar um triângulo.

### Instanciação

→ No momento em que executamos o comando `new Triangle()`, os objetos são alocados em um local chamado Heap. 

Heap é uma área onde são criados objetos dinâmicos em tempo de execução.

Temos o local Stack, onde ficam as variáveis, neste caso `p`, `areaX`, etc. O nosso objeto x também está na stack, mas consta um endereço que leva para a área Heap. Ou seja, o `x` na Stack é apenas uma referência ao objeto x na Heap. 

