
# Sistema de Controle de Estacionamento

Este projeto é um sistema simples de controle de estacionamento desenvolvido em Python, que permite registrar entradas e saídas de veículos, calcular o tempo de permanência e o valor a ser pago conforme taxas configuráveis, e gerar um relatório em CSV.

## Funcionalidades

- Configurar taxas de estacionamento (por tipo de veículo: carro ou moto).
- Registrar entrada de veículos, informando placa, tipo e horário.
- Registrar saída de veículos, calculando tempo de permanência e valor a pagar.
- Armazenar as informações de cada operação em um arquivo CSV.
- Interface interativa via terminal.

## Como usar

1. **Clone o repositório** ou copie o arquivo `main.py` para o seu ambiente local.
2. **Execute o script** com Python 3:

```bash
python main.py
```

3. O sistema exibirá um menu interativo com as seguintes opções:

- `1. Configurar taxas`: permite alterar os valores cobrados por tipo de veículo.
- `2. Registrar entrada`: cadastra a entrada de um veículo.
- `3. Registrar saída`: registra a saída, calcula o valor a pagar e grava no relatório.
- `4. Ver arquivo CSV gerado`: mostra o caminho do arquivo de relatório.
- `5. Sair`: encerra o programa.

## Estrutura do Projeto

- **main.py**: script principal com todas as funcionalidades.
- **relatorio_estacionamento.csv**: arquivo gerado automaticamente para armazenar os registros de entrada e saída.

## Formato do Relatório (CSV)

| Placa | Tipo | Entrada | Saída | Permanência (h) | Valor (R$) |
|-------|------|---------|-------|-----------------|------------|
| ABC1234 | carro | 2025-05-22 10:00 | 2025-05-22 12:30 | 2.50 | 15.00 |

## Configuração de Taxas

Por padrão:

- **Carro**: R$ 10,00 pela primeira hora + R$ 5,00 por hora adicional.
- **Moto**: R$ 7,00 pela primeira hora + R$ 3,00 por hora adicional.

As taxas podem ser ajustadas conforme a necessidade pelo próprio menu do sistema.

## Requisitos

- Python 3.x
- Módulos padrão: `datetime`, `csv`, `os`

## Observações

- O sistema não armazena dados em memória após o encerramento — apenas o CSV permanece.
- A entrada e saída devem ser digitadas no formato: `dd/mm/aaaa HH:MM` (exemplo: `22/05/2025 14:30`).

## Melhorias Futuras

- Interface gráfica.
- Banco de dados para persistência completa.
- Geração de relatórios mais elaborados.
- Suporte para diferentes tipos de veículos.

## Autor

- Desenvolvido por Gabriel Medina Peres.
