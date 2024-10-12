public class Pessoa {
    private String nome;
    private String cpf;
    private int idade;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getCpf() {
        return cpf;
    }

    public void setCpf(String cpf) {
        this.cpf = cpf;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }
}
public class GerenciadorDePessoas {
    private Pessoa pessoa1;
    private Pessoa pessoa2;

    public void cadastrarPessoa1(Pessoa pessoa) {
        this.pessoa1 = pessoa;
    }

    public void cadastrarPessoa2(Pessoa pessoa) {
        this.pessoa2 = pessoa;
    }

    public void atualizarPessoa1(Pessoa pessoa) {
        this.pessoa1 = pessoa;
    }

    public void atualizarPessoa2(Pessoa pessoa) {
        this.pessoa2 = pessoa;
    }

    public void exibirPessoa1() {
        if (pessoa1 != null) {
            System.out.println("Pessoa 1: " + pessoa1.getNome() + ", CPF: " + pessoa1.getCpf() + ", Idade: " + pessoa1.getIdade());
        } else {
            System.out.println("Pessoa 1 não cadastrada.");
        }
    }

    public void exibirPessoa2() {
        if (pessoa2 != null) {
            System.out.println("Pessoa 2: " + pessoa2.getNome() + ", CPF: " + pessoa2.getCpf() + ", Idade: " + pessoa2.getIdade());
        } else {
            System.out.println("Pessoa 2 não cadastrada.");
        }
    }
}
public class Main {
    public static void main(String[] args) {
        GerenciadorDePessoas gerenciador = new GerenciadorDePessoas();

        Pessoa pessoa1 = new Pessoa();
        pessoa1.setNome("João");
        pessoa1.setCpf("12345678900");
        pessoa1.setIdade(30);
        gerenciador.cadastrarPessoa1(pessoa1);

        Pessoa pessoa2 = new Pessoa();
        pessoa2.setNome("Maria");
        pessoa2.setCpf("09876543211");
        pessoa2.setIdade(25);
        gerenciador.cadastrarPessoa2(pessoa2);

        gerenciador.exibirPessoa1();
        gerenciador.exibirPessoa2();

        // Atualizando a idade da pessoa 1
        pessoa1.setIdade(31);
        gerenciador.atualizarPessoa1(pessoa1);

        System.out.println("Após atualização:");
        gerenciador.exibirPessoa1();
    }
}
# Sistema de Gerenciamento de Pessoas

Este é um sistema simples para gerenciar o cadastro de pessoas.

## Instruções de Compilação e Execução

1. Certifique-se de ter o Java instalado em seu computador.
2. Compile os arquivos .java usando o comando:
3. 3. Execute o programa com o comando:
   4. ## Exemplo de Uso

- O programa cadastra duas pessoas, exibe suas informações e permite a atualização de dados.

## Lógica de Encapsulamento

Os atributos da classe `Pessoa` são encapsulados, ou seja, são privados e podem ser acessados ou modificados apenas por meio de métodos públicos (getters e setters).
