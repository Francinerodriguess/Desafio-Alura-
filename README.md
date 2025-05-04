Nome do Projeto
Desafio de Conta Bancária em Java

Este projeto é uma aplicação simples que simula um sistema de gerenciamento de conta bancária, permitindo ao usuário consultar saldo, transferir e receber valores.

Tecnologias Utilizadas
Java
JDK
IntelliJ IDEA
Instalação
Faça o download e instale o [JDK](link para o download do JDK).
Instale o [IntelliJ IDEA](link para o download do IntelliJ IDEA).
Clone este repositório:
Copiar
git clone https://github.com/seuusuario/seurepositorio.git
Funcionalidades
O projeto aborda os seguintes tópicos principais:

Instalação do JDK e IntelliJ IDEA: Aprenda a instalar o kit de desenvolvimento Java (JDK) e o ambiente de desenvolvimento integrado (IDE) IntelliJ IDEA.
Variáveis: Demonstra como declarar e atribuir valores a variáveis, tanto primitivas quanto do tipo String.
Conversão de Tipos (Casting): Explicação sobre a conversão de tipos de dados em Java.
Condicionais: Uso de condicionais para tomar decisões no código.
Loops: Implementação de loops e desafios para praticar.
Código
Aqui está um exemplo do código desenvolvido no projeto:

Copiar
import java.util.Scanner;

public class Desafio {
    public static void main(String[] args) {
        String nome = "Sandra Bullock";
        String tipoConta = "Corrente";
        double saldo = 3000.99;
        int opcao = 0;

        System.out.println("***************************");
        System.out.println("\nNome do cliente: " + nome);
        System.out.println("Tipo de conta: " + tipoConta);
        System.out.println("Saldo atual: " + saldo);
        System.out.println("\n***************************");

        String menu = """
                ** Digite sua opção **
                 1 - Consultar saldo
                 2 - Transferir valor
                 3 - Receber valor
                 4 - Sair
                """;
        Scanner leitura = new Scanner(System.in);

        while (opcao != 4) {
            System.out.println(menu);
            opcao = leitura.nextInt();

            if (opcao == 1) {
                System.out.println("O saldo atualizado é " + saldo);
            } else if (opcao == 2) {
                System.out.println("Qual o valor que deseja transferir?");
                double valor = leitura.nextDouble();
                if (valor > saldo) {
                    System.out.println("Não há saldo para realizar a transferência.");
                } else {
                    saldo -= valor;
                    System.out.println("Novo saldo: " + saldo);
                }
            } else if (opcao == 3) {
                System.out.println("Valor recebido: ");
                double valor = leitura.nextDouble();
                saldo += valor;
                System.out.println("Novo saldo: " + saldo);
            } else if (opcao != 4) {
                System.out.println("Opção inválida.");
            }
        }
    }
}
Considerações Finais
Os instrutores incentivam os alunos a continuarem seus estudos em Java e desejam sucesso na jornada de aprendizado.
