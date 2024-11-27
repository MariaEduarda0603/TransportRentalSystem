# TransportRentalSystem
## Sistema de Gerenciamento de Meios de Transporte Individuais

Este projeto é uma implementação do padrão de projeto **Abstract Factory** para gerenciar diferentes tipos de meios de transporte individuais, diferenciando-os pela categoria de propulsão (movidos a bateria ou por esforço humano). O sistema permite criar e gerenciar meios de transporte como bicicletas, patinetes, patins e skates, categorizando-os entre movidos por bateria ou por esforço humano.

## Objetivo
O objetivo deste sistema é demonstrar a utilização do padrão **Abstract Factory**, onde cada fábrica concreta cria meios de transporte específicos para duas categorias de propulsão:

- **Movidos a Bateria**: Patinetes elétricos, bicicletas elétricas.
- **Movidos pelo Esforço Humano**: Bicicletas convencionais, patins, skates.

## Estrutura do Projeto
A estrutura do projeto é organizada da seguinte forma:

src/

└── com/example/transport
  
    ├── Transport.java                           (Interface genérica de meio de transporte)
    
    ├── ElectricScooter.java                     (Classe concreta: Patinete Elétrico)
    
    ├── ElectricBike.java                        (Classe concreta: Bicicleta Elétrica)
    
    ├── Bicycle.java                             (Classe concreta: Bicicleta Convencional)
    
    ├── RollerSkates.java                        (Classe concreta: Patins)

    ├── Skateboard.java                          (Classe concreta: Skate)
    
    ├── TransportFactory.java                    (Fábrica Abstrata)
    
    ├── ElectricTransportFactory.java            (Fábrica concreta: Meios movidos a Bateria)
    
    ├── HumanPoweredTransportFactory.java        (Fábrica concreta: Meios movidos a Esforço Humano)
    
    └── Main.java                                (Ponto de entrada - Classe principal)



## Como Funciona

### Interface `Transport`
Define o método `ride()` que será implementado por todas as classes de meios de transporte. Este método exibe uma mensagem indicando o uso do transporte.

### Classes Concretas
As classes concretas representam os meios de transporte específicos, como `ElectricScooter`, `ElectricBike`, `Bicycle`, `RollerSkates`, e `Skateboard`. Cada classe implementa o método `ride()` de maneira personalizada para cada tipo de transporte.

### Abstract Factory `TransportFactory`
Define os métodos `createScooter()` e `createBike()` que são implementados por fábricas concretas para criar os meios de transporte adequados.

### Fábricas Concretas:
- **`ElectricTransportFactory`**: Cria meios de transporte movidos a bateria (Patinete Elétrico e Bicicleta Elétrica).
- **`HumanPoweredTransportFactory`**: Cria meios de transporte movidos pelo esforço humano (Bicicleta Convencional, Patins e Skate).

### Classe Principal `Main`
O ponto de entrada do sistema, onde as fábricas são instanciadas, meios de transporte são criados e as mensagens são exibidas com o uso de cada transporte.

## Exemplo de Execução

Ao executar o código, o sistema cria diferentes meios de transporte e exibe mensagens indicando o uso de cada um.

Exemplo de saída:
![console](https://github.com/user-attachments/assets/0b64b3c8-b1bc-4279-9ba3-8a09c05f182b)


## Como Rodar o Projeto

### Clonar o repositório:

Se ainda não tiver o repositório, você pode cloná-lo usando o seguinte comando:

```bash
git clone https://github.com/mendonca.fernandes@academico.ifg.edu.br/TransportRentalSystem.git


Compilar o Código:
Navegue até a pasta onde o código está localizado e compile todas as classes usando o comando:
javac $(find . -name "*.java")


Executar o Programa:
Para rodar o programa, execute o comando:
java com.example.transport.Main


Contribuições
Sinta-se à vontade para contribuir com melhorias ou correções. Para isso, basta seguir os seguintes passos:
Fork o repositório.
Crie uma branch para sua alteração (git checkout -b nova-feature).
Faça commit das suas alterações (git commit -am 'Adicionando nova feature').
Envie para o repositório remoto (git push origin nova-feature).
Abra um pull request.


Licença
Este projeto é de código aberto e está disponível sob a licença MIT.









        
