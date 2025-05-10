# desafio-de-poo-com-java-pratico

  Vamos desmistificar os conceitos de POO através de um desafio prático. Aqui está uma abordagem passo a passo para implementar os pilares da OO em um projeto Java.

1. Definição do Problema

  Vamos criar um sistema simples de gerenciamento de animais em um zoológico, que nos permitirá explorar todos os conceitos de POO.

2. Implementação dos Pilares da POO

   Abstração\
   Vamos criar classes que representam conceitos do mundo real:

   ```
       // Classe abstrata representando um animal genérico
    public abstract class Animal {
        private String nome;
        private int idade;
        
        public Animal(String nome, int idade) {
            this.nome = nome;
            this.idade = idade;
        }
        
        // Método abstrato - cada animal terá sua própria implementação
        public abstract void emitirSom();
        
        // Método concreto
        public void dormir() {
            System.out.println(nome + " está dormindo...");
        }
        
        // Getters e Setters
        public String getNome() {
            return nome;
        }
        
        public int getIdade() {
            return idade;
        }
    }
```

Encapsulamento

Protegemos os atributos e fornecemos acesso controlado:

```

    public class Leao extends Animal {
        private double tamanhoJuba;
        
        public Leao(String nome, int idade, double tamanhoJuba) {
            super(nome, idade);
            this.tamanhoJuba = tamanhoJuba;
        }
        
        public double getTamanhoJuba() {
            return tamanhoJuba;
        }
        
        public void setTamanhoJuba(double tamanhoJuba) {
            if(tamanhoJuba > 0) {
                this.tamanhoJuba = tamanhoJuba;
            } else {
                System.out.println("Tamanho da juba deve ser positivo");
            }
        }
        
        @Override
        public void emitirSom() {
            System.out.println(getNome() + " diz: Roar!");
        }
    }

```


