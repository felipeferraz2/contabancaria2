public class Conta {
    // Atributos privados
    private String nomeTitular;
    private int numero;
    private String agencia;
    private double saldo;

    // Construtor
    public Conta(String nomeTitular, int numero, String agencia, double saldoInicial) {
        this.nomeTitular = nomeTitular;
        this.numero = numero;
        this.agencia = agencia;
        this.saldo = saldoInicial;
    }

    // Métodos
    public void sacar(double valor) {
        if (saldo >= valor) {
            saldo -= valor;
            System.out.println("Saque realizado. Novo saldo: " + saldo);
        } else {
            System.out.println("Saldo insuficiente.");
        }
    }

    public void depositar(double valor) {
        saldo += valor;
        System.out.println("Depósito realizado. Novo saldo: " + saldo);
    }

    public double calcularRendimento() {
        return saldo * 0.1;  // Rendimento de 10%
    }

    // Método para recuperar os dados para impressão
    public String recuperaDadosParaImpressao() {
        return "Titular: " + nomeTitular + "\nNúmero da Conta: " + numero + "\nAgência: " + agencia + "\nSaldo: " + saldo;
    }

    // Getters e setters necessários
    public String getNomeTitular() {
        return nomeTitular;
    }

    public void setNomeTitular(String nomeTitular) {
        this.nomeTitular = nomeTitular;
    }

    public int getNumero() {
        return numero;
    }

    public void setNumero(int numero) {
        this.numero = numero;
    }

    public String getAgencia() {
        return agencia;
    }

    public void setAgencia(String agencia) {
        this.agencia = agencia;
    }

    public double getSaldo() {
        return saldo;
    }

    public void setSaldo(double saldo) {
        this.saldo = saldo;
    }
}