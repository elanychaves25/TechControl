# Controle da Situação dos Equipamentos

## Objetivo

Permitir acompanhar a situação atual de cada equipamento cadastrado no sistema TechControl.

## Situações dos equipamentos

Cada equipamento poderá apresentar uma das seguintes situações:

- **Disponível:** o equipamento pode ser emprestado.
- **Emprestado:** o equipamento está atualmente em posse de um usuário.
- **Indisponível:** o equipamento não está disponível para empréstimo.

## Exemplo

| Identificação | Nome | Situação |
|---|---|---|
| EQ001 | Notebook | Disponível |
| EQ002 | Projetor | Indisponivel |
| EQ003 | Tablet | Disponível  |
| EQ004 | Caixa de som | Emprestado |
| EQ005 | Computador |  Disponível |

## Atualização da situação

A situação do equipamento deve ser atualizada de acordo com os registros de empréstimo e devolução realizados no sistema.
