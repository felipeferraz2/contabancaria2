import java.util.Scanner;

public class TestaConta {
    public static void main(String[] args) {
        // Scanner para capturar dados do usuário
        Scanner scanner = new Scanner(System.in);

        // Entrada de dados para a criação da conta
        System.out.print("Digite o nome do titular: ");
        String nome = scanner.nextLine();

        System.out.print("Digite o número da conta: ");
        int numero = scanner.nextInt();

        System.out.print("Digite a agência: ");
        String agencia = scanner.next();

        System.out.print("Digite o saldo inicial: ");
        double saldoInicial = scanner.nextDouble();

        // Criação de um objeto Conta
        Conta conta = new Conta(nome, numero, agencia, saldoInicial);

        // Movimentação: Saque e Depósito
        System.out.print("Digite o valor a ser sacado: ");
        double valorSaque = scanner.nextDouble();
        conta.sacar(valorSaque);

        System.out.print("Digite o valor a ser depositado: ");
        double valorDeposito = scanner.nextDouble();
        conta.depositar(valorDeposito);

        // Cálculo de rendimento
        double rendimento = conta.calcularRendimento();
        System.out.println("Rendimento mensal da conta: R$ " + rendimento);

        // Recuperação e impressão dos dados
        System.out.println("\nDados atualizados da conta:");
        System.out.println(conta.recuperaDadosParaImpressao());

        scanner.close();
    }
}