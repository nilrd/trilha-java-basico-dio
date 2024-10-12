# Projeto: Conta Banco

## Descrição
Este projeto em Java simula a criação de uma conta bancária, onde o usuário insere informações como número da conta, agência, nome do cliente e saldo inicial. O programa então exibe uma mensagem confirmando a criação da conta e mostrando os detalhes fornecidos, com o saldo formatado de forma adequada (incluindo separadores de milhar e casas decimais).

## Funcionalidades
- Solicitação dos dados da conta bancária (número da conta, agência, nome do cliente e saldo).
- Exibição de uma mensagem formatada com os dados da conta criada.
- Formatação adequada do saldo, com separadores de milhar e duas casas decimais.

## Tecnologias utilizadas
- Linguagem: Java
- Biblioteca: `java.util.Scanner` para capturar dados do usuário.
- Biblioteca: `java.text.DecimalFormat` para formatar números.

## Estrutura do projeto

### Arquivo principal: `ContaTerminal.java`

```java
import java.text.DecimalFormat;
import java.util.Scanner;

public class ContaTerminal {

    public static void main(String[] args) throws Exception {
        // Criando um objeto da classe Scanner para capturar os dados do terminal
        Scanner scanner = new Scanner(System.in);

        // Exibindo mensagens para o usuário e capturando os dados
        System.out.println("Por favor, digite o número da conta: ");
        int numero = scanner.nextInt();
        scanner.nextLine();  // Consumir a quebra de linha

        System.out.println("Por favor, digite o número da Agência: ");
        String agencia = scanner.nextLine();

        System.out.println("Por favor, digite o nome do cliente: ");
        String nomeCliente = scanner.nextLine();

        System.out.println("Por favor, digite o saldo inicial: ");
        double saldo = scanner.nextDouble();

        // Formatando o saldo com duas casas decimais e separadores de milhar
        DecimalFormat df = new DecimalFormat("###,###.00");

        // Exibindo a mensagem com os dados fornecidos
        System.out.println("Olá " + nomeCliente + ", obrigado por criar uma conta em nosso banco, sua agência é " 
                            + agencia + ", conta " + numero + " e seu saldo " + df.format(saldo) + " já está disponível para saque.");

        // Fechando o Scanner
        scanner.close();
    }
}
```

## Como implementar o código

1. **Crie o projeto Java:**
   - No seu ambiente de desenvolvimento, crie um novo projeto Java chamado `ContaBanco`.

2. **Crie o arquivo `ContaTerminal.java`:**
   - Dentro da pasta `src` do projeto, crie um arquivo chamado `ContaTerminal.java` e copie o código acima.

3. **Importe as bibliotecas necessárias:**
   - A classe `Scanner` é usada para capturar os dados do usuário.
   - A classe `DecimalFormat` é usada para formatar o saldo em um formato legível.

## Como executar o código

1. **Compile o projeto:**
   - No terminal, navegue até a pasta do projeto e compile o código com o seguinte comando:
     ```bash
     javac ContaTerminal.java
     ```

2. **Execute o projeto:**
   - Após a compilação, execute o programa com o seguinte comando:
     ```bash
     java ContaTerminal
     ```

3. **Interaja com o programa:**
   - O programa solicitará que você insira o número da conta, o número da agência, o nome do cliente e o saldo inicial.
   - Após inserir esses dados, o programa exibirá uma mensagem formatada com as informações fornecidas.

## Exemplo de execução

```
Por favor, digite o número da conta: 
XXXXXX
Por favor, digite o número da Agência: 
XXXX
Por favor, digite o nome do cliente: 
Nome do Usuario
Por favor, digite o saldo inicial: 
XXXXXXX.XX

Será exibido os dados e valor
```

## Observações
- O código utiliza `DecimalFormat` para garantir que o saldo seja exibido com duas casas decimais e separadores de milhar.
- Certifique-se de que o JDK esteja instalado corretamente em sua máquina e que as variáveis de ambiente estejam configuradas para a execução de programas Java.
