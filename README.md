# Implementação de Lista Encadeada Simples em C

## Descrição
Este projeto em C implementa uma lista encadeada simples, uma estrutura de dados linear onde os elementos são armazenados em nós, com cada nó apontando para o próximo. A lista suporta operações básicas como inclusão, exclusão, alteração, e obtenção de elementos.

## Funcionalidades
- **Inicialização da Lista**: Cria uma lista encadeada vazia, pronta para receber elementos.
- **Inclusão de Elemento**: Insere um novo elemento na lista em uma posição específica.
- **Alteração de Elemento**: Modifica o valor de um elemento existente na lista.
- **Exclusão de Elemento**: Remove um elemento da lista em uma posição específica.
- **Obtenção de Elemento**: Recupera o valor de um elemento em uma posição específica da lista.
- **Tamanho da Lista**: Retorna o número de elementos atualmente armazenados na lista.

## Como Usar
1. Compile o código utilizando um compilador C. Exemplo:
   ```bash
   gcc -o lista_encadeada lista_encadeada.c
   ```
2. Inclua e altere os elementos da lista conforme necessário, utilizando as funções implementadas.

## Estrutura de Dados
O projeto utiliza a seguinte estrutura de dados:

- **nodo**: Representa um nó da lista, contendo um `elemento` e um ponteiro para o próximo nó (`prox`).
- **lista_encadeada**: Representa a lista como um todo, contendo um ponteiro para o primeiro nó (`lista`) e o tamanho atual da lista (`tamanho`).

## Funções Principais
- **inicializa_lista(lista_encadeada *le)**: Inicializa uma lista encadeada vazia.
- **tamanho(lista_encadeada le)**: Retorna o tamanho atual da lista.
- **obter_elemento(lista_encadeada le, int i, elemento *e)**: Obtém o elemento na posição `i` da lista.
- **incluir_elemento(lista_encadeada *le, int i, elemento e)**: Insere um elemento na posição `i` da lista.
- **alterar_elemento(lista_encadeada *le, int i, elemento e)**: Altera o elemento na posição `i` da lista.
- **excluir_elemento(lista_encadeada *le, int i)**: Remove o elemento na posição `i` da lista.

## Exemplo de Uso
Um exemplo básico de uso das funções implementadas:
```c
lista_encadeada le;
inicializa_lista(&le);

elemento e1 = 10;
incluir_elemento(&le, 1, e1);

elemento e2 = 20;
incluir_elemento(&le, 2, e2);

elemento e;
obter_elemento(le, 1, &e);
printf("Elemento na posição 1: %d\n", e);  // Saída: 10

alterar_elemento(&le, 2, 30);
obter_elemento(le, 2, &e);
printf("Elemento na posição 2: %d\n", e);  // Saída: 30

excluir_elemento(&le, 1);
printf("Tamanho da lista após exclusão: %d\n", tamanho(le));  // Saída: 1
```

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
