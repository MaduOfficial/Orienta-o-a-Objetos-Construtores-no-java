# Orienta-o-a-Objetos-Construtores-no-java
Anotações de Orientação a Objetos: Construtores

                                                            Orientação a Objetos: Construtores

Construtor simples e vazio

class Carro {

    String marca;
    String modelo;
    int numPassageiros; //número de passageiros
    double capCombustivel; //capacidade do tangue de combustivel
    double consumoCombustivel; //consumo de combustivel por km

    Carro(){ }

    void exibirAutonomia:

    System.out.println("A altonomia so carro é: " +
            capCombustivel * consumoCombustivel + " km");
    }

    double obterAutononia()(
        return capCombustivel * consumoCombustivel;
    }

    double calcularCombustivel(double km){
        return km/consumoCombustivel;
    }
}

É como se nós criassemos um método sem retorno e sem parâmetro algum, então não ter o construtor declarado na classe é a mesma coisa que ter ai na tela
"Carro(){ }" esse carro abre fevcha parênteses abre fecha chaves simplesmente vazio.

Outro exemplo

Carro(){
    numPassageiros = 4;
}

Um outro exemplo é que caso agente precisa inicializar a variável como nós vimos nas aulas de método nós criamos algumas variáveis por exemplo como um
jogo da velha e nós já inicializamos o array a matriz do jogo da velha ali dentro da classe, a gente poderia ter feito aquele código dentro do consultor
poder ficar mais elegante como esse aqui que já existe um valor padrão para aquele atributo para todas as classes a gente já pode colocar esses valores
dentro do contrutor.

contrutor com parâmetro

Carro(String marca_, String modelo_){
    marca = marca_;
    modelo = modelo ;
}

se a gente precisar nós também podemos declarar contrutor com parâmetro assim por exemplo se ao invés de você instãnciar a classe depois você for sitando
atributo por atributo você já pode passar todos os atributos ali no construtor da classe.

package com.madu.poo.Construtores;

public class Carro {

	String marca;
	String modelo;
    int numPassageiros;
	double capCombustivel;
	double consumoCombustivel;
	
	Carro() {
		System.out.println("Classe Carro foi instanciada");
		numPassageiros = 4;
	}
	
	Carro(String marca_, String modelo_, int numPassageiros_, double capCombustivel_, double consumoCombustivel_){
		marca = marca_;
		modelo = modelo_;
		numPassageiros =  numPassageiros_;
		capCombustivel = capCombustivel_;
		consumoCombustivel = consumoCombustivel_;
	}
			
	void exibirAutonomia() {
	System.out.println("A autonomia do carro é: " + capCombustivel * consumoCombustivel + " km");
	}
			
    double obterautonomia() {
				
		System.out.println("Método obterAltonomia foi chamado.");
				
		return capCombustivel * consumoCombustivel;
	}
		
	double calcularCombustivel(double km) {
		
		double qtdCombustivel = km/consumoCombustivel;
		
		return qtdCombustivel;
	}
}


Ex:

package com.madu.poo.Construtores;

public class TesteCarro {

	public static void main(String[] args) {
		
		Carro van = new Carro();
		van.marca = "Fiat";
		van.modelo = "Ducato";
		//van.numPassageiros = 10;
		van.capCombustivel = 100;
		van.consumoCombustivel = 0.2;
		
		System.out.println(van.numPassageiros);
		
		Carro van2 = new Carro("Fiat", "Ducato", 10, 100, 0.2);
		
		System.out.println(van2.marca);
		System.out.println(van2.modelo);
		System.out.println(van2.numPassageiros);
		System.out.println(van2.capCombustivel);
		System.out.println(van2.consumoCombustivel);
	}

}


Console:
Classe Carro foi instanciada
4
Fiat
Ducato
10
100.0
0.2
