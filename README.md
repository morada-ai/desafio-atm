# Desafio Técnico Morada.ai: Caixa Eletrônico API

## Descrição
Esta API simula o funcionamento de um caixa eletrônico. Ela recebe um valor de saque desejado e retorna a quantidade de cédulas de cada valor necessárias para compor esse saque, utilizando a menor quantidade de cédulas possível. As cédulas consideradas são: 100, 50, 20, 10, 5 e 2.

## Requisitos

1. **Algoritmo para saque**: A lógica deve ser capaz de calcular a quantidade mínima de cédulas necessárias para um valor de saque dado.
2. **Endpoint para saque**:
   - **Entrada**: Valor do saque desejado (inteiro positivo).
   - **Saída**: Quantidade de cédulas de cada valor.

## Formato do Endpoint

- **URL**: `/api/saque`
- **Método**: POST
- **Entrada** (JSON):
  ```json
  {
    "valor": 380
  }
  ```
- **Saída** (JSON):
  ```json
  {
    "100": 3,
    "50": 1,
    "20": 1,
    "10": 1,
    "5": 0,
    "2": 0
  }
  ```

## Desafios

1. **Tratamento de Entradas Inválidas**: Garantir que o valor inserido é um número inteiro positivo.
2. **Eficiência na Distribuição de Cédulas**: Implementar uma lógica que sempre retorne a menor quantidade de cédulas possível.
3. **Erros e Exceções**: Lidar com cenários onde o valor de saque não pode ser atendido com as cédulas disponíveis.
4. **Documentação e Testes**: Garantir que o código esteja bem documentado e com testes adequados para validar a lógica de saque.

## Exemplos de Uso

- **Requisição**:
  ```bash
  curl -X POST -H "Content-Type: application/json" -d '{"valor": 380}' http://localhost:5000/api/saque
  ```
- **Resposta**:
  ```json
  {
    "100": 3,
    "50": 1,
    "20": 1,
    "10": 1,
    "5": 0,
    "2": 0
  }
  ```

## Considerações Finais

Este projeto foi desenvolvido para simular um caixa eletrônico simples. A lógica foi otimizada para garantir a menor quantidade de cédulas possíveis para qualquer valor de saque permitido. Quaisquer dúvidas ou problemas, por favor, abra uma issue no repositório.

## Instruções para Envio

- Subir o código para um repositório no GitHub;
- Incluir um README.md no repositório contendo a documentação, quais foram os principais desafios, e uma instrução de como excutar o projeto;
- Enviar o link do repositório até o prazo determinado.

## Perguntas Frequentes
### Qual linguagem?
Não temos preferência por linguagem. Porém, aqui utilizamos: Javascript e Python

### Devo construir uma interface?
Não é necessário desenvolver uma interface gráfica para este projeto. O foco principal da avaliação será a lógica aplicada e a robustez do código. Estamos interessados em verificar se o código está bem organizado, legível e se ele atende aos critérios estabelecidos pelos testes.

### Quando vou receber meu feedback?
Você receberá o feedback em até 15 dias após o encerramento das inscrições.

### Posso realizar alguma alteração depois do prazo de encerramento?
Não é possível realizar alterações após o prazo estabelecido. Mesmo que modificações sejam feitas após este prazo, nossa equipe avaliará apenas o último commit válido realizado antes do encerramento das inscrições.
