# Respostas das Questões da Lista de Exercícios da Semana 07

#### 1.  **_A) O código avalia a expressão, imprime true e calcula o produto dos números na lista e imprime o resultado no console._** 

**Justificativa:** A expressão booleana resulta em true e o código calcula corretamente o produto dos valores do array [3, 6, 9, 12, 15], imprimindo o resultado 29160 no console.
______

#### 2.  **_A) Ambas as funções exibirão: 'Seu crédito foi aprovado. Saldo disponível: 400.'_**

**Justificativa:** Ambas as funções somam os valores de compras enquanto o total for menor ou igual o limite. O total final é 4600, o limite é 5000, então o crédito é aprovado e o saldo disponível é 400.
______

#### 3.  **_B) O código verifica se a idade pertence à faixa adulta. Se for, exibe "Você é um adulto!". Caso contrário, verifica se é menor de idade e exibe "Você é menor de idade!". Se nenhuma das condições anteriores for verdadeira, exibe "Você está na melhor idade!"._**

**Justificativa:** O código verifica se a idade está na faixa adulta (entre 18 e 60). Caso não, checa se é menor de idade. Caso nenhuma das duas condições seja verdadeira (ou seja, idade maior ou igual 60), exibe a mensagem "Você está na melhor idade!".
______

#### 4.  **_B)_**

**Justificativa:** O código simula o consumo de energia de cinco dispositivos. O primeiro dispositivo consome 300 unidades e é ligado com a energia principal, restando 900. O segundo consome 600 e também é ligado com a energia principal, restando 300. O terceiro dispositivo consome 500; como só há 300 de energia principal, ele usa 200 da bateria extra, é ligado com bateria e restam 200 na bateria. O quarto consome 200 e é ligado com a bateria restante, esgotando-a. Já o quinto dispositivo precisa de 400, mas não há mais energia disponível, e portanto não pode ser ligado.
______

#### 5.  **_B) O método update() é chamado continuamente a cada quadro (frame) do jogo, sendo usado para atualizar a lógica, movimentação e interações dos objetos na cena._**

**Justificativa:** O método update() é chamado a cada frame e serve para atualizar a lógica do jogo em tempo real. É nele que se controlam ações como movimentação de personagens, verificações de colisão e atualizações de estados ou animações dos objetos na cena.
______

#### 6.  **_A) Simular física avançada, incluindo corpos rígidos, colisões complexas e interação entre objetos com gravidade e forças._**

**Justificativa:** O módulo Matter.js Physics no Phaser é utilizado para simular física avançada no jogo, como corpos rígidos, colisões complexas, gravidade e aplicação de forças. Ele permite comportamentos realistas entre objetos e reações físicas detalhadas.
______

#### 7.  

```javascript
Início
    Escreva("Digite o valor total da compra:")
    Leia valorTotal

    Se valorTotal < 50 então
        Escreva("Frete não disponível!")
    Senão se valorTotal >= 50 e valorTotal <= 199.99 então
        Escreva("Frete com custo adicional!")
    Senão
        Escreva("Frete grátis!")
Fim
```

**Justificativa:** O pseudocódigo usa estruturas condicionais para verificar em qual faixa de preço o valor se encaixa e exibe a mensagem correspondente.
______

#### 8. (Utilizei o ChatGPT para me auxiliar nessa questão)

```javascript
// Classe base Veiculo
Classe Veiculo
    Atributos:
        modelo
        ano

    Método Construtor(modelo, ano):
        este.modelo ← modelo
        este.ano ← ano

    Método CalcularConsumo():
        Escreva("Cálculo genérico de consumo. Deve ser sobrescrito.")


// Classe derivada Carro
Classe Carro herda de Veiculo
    Atributos:
        quilometragem
        eficiencia  // km por litro

    Método Construtor(modelo, ano, quilometragem, eficiencia):
        Chamar Veiculo.Construtor(modelo, ano)
        este.quilometragem ← quilometragem
        este.eficiencia ← eficiencia

    Método CalcularConsumo():
        consumo ← quilometragem / eficiencia
        Retorne consumo


// Classe derivada Moto
Classe Moto herda de Veiculo
    Atributos:
        quilometragem
        eficiencia  // km por litro

    Método Construtor(modelo, ano, quilometragem, eficiencia):
        Chamar Veiculo.Construtor(modelo, ano)
        este.quilometragem ← quilometragem
        este.eficiencia ← eficiencia

    Método CalcularConsumo():
        consumo ← quilometragem / eficiencia
        Retorne consumo
```

**Justificativa:** As classes Carro e Moto herdam da classe Veiculo, aproveitando os atributos comuns (modelo e ano). Cada uma implementa seu próprio método CalcularConsumo, que utiliza a quilometragem percorrida e a eficiência (km/l) para calcular o consumo de combustível.
______

#### 9. (Utilizei o ChatGPT para me auxiliar nessa questão)

```javascript
Início
    Escreva("Digite a velocidade inicial da sonda (m/s):")
    Leia velocidadeInicial

    Escreva("Digite a velocidade segura para pouso (m/s):")
    Leia velocidadeSegura

    Escreva("Digite a desaceleração constante (m/s²):")
    Leia desaceleracao

    Escreva("Digite o tempo máximo permitido para a descida (s):")
    Leia tempoMaximo

    Se desaceleracao <= 0 então
        Escreva("Desaceleração inválida. Deve ser maior que zero.")
        Fim

    tempo ← (velocidadeInicial - velocidadeSegura) / desaceleracao

    Se tempo > tempoMaximo então
        Escreva("Não é possível reduzir a velocidade a tempo. Risco de desvio orbital!")
    Senão se tempo < 0 então
        Escreva("Velocidade inicial já está abaixo da velocidade segura.")
    Senão
        Escreva("Tempo necessário para pouso seguro: ", tempo, " segundos.")
Fim
```

**Justificativa:** O programa aplica a fórmula fornecida para calcular o tempo necessário para reduzir a velocidade até o nível seguro, levando em conta a desaceleração constante. Ele verifica se o tempo está dentro do limite permitido e se os valores inseridos são válidos.
______

#### 10. (Utilizei o ChatGPT para me auxiliar nessa questão)

```javascript
Função MultiplicarMatrizesInvestimento(matrizA, matrizB):
    linhasA ← tamanho(matrizA)
    colunasA ← tamanho(matrizA[0])
    linhasB ← tamanho(matrizB)
    colunasB ← tamanho(matrizB[0])

    Se colunasA ≠ linhasB então:
        Retornar "As matrizes não podem ser multiplicadas. Dimensões incompatíveis."

    matrizResultado ← novaMatriz(linhasA, colunasB)

    Para i de 0 até linhasA - 1 faça:
        Para j de 0 até colunasB - 1 faça:
            soma ← 0
            Para k de 0 até colunasA - 1 faça:
                soma ← soma + (matrizA[i][k] * matrizB[k][j])
            matrizResultado[i][j] ← soma

    Retornar matrizResultado
```

**Justificativa:** A função realiza a multiplicação de duas matrizes de forma clássica, onde cada elemento da matriz resultante é calculado pela soma dos produtos dos elementos correspondentes da linha da primeira matriz com a coluna da segunda. Essa multiplicação representa a combinação entre tipos de investimentos e seus impactos financeiros ao longo do tempo. A função também verifica se as dimensões são compatíveis para multiplicação, garantindo validade da operação.





