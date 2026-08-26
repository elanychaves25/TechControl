# Modelagem do Sistema TechControl

## 1. Objetivo da modelagem

A modelagem representa o fluxo básico do sistema TechControl, um sistema de controle de empréstimo de equipamentos escolares.

O fluxo demonstra o processo desde a seleção de um equipamento pelo usuário até o registro do empréstimo, devolução e atualização da situação do equipamento.

## 2. Fluxo do sistema

O processo funciona da seguinte forma:

1. O usuário seleciona um equipamento.
2. O sistema verifica se o equipamento está disponível.
3. Caso o equipamento não esteja disponível, o sistema informa ao usuário que ele não está disponível.
4. Caso o equipamento esteja disponível, o sistema registra o empréstimo.
5. O equipamento é entregue ao usuário.
6. Posteriormente, é registrada a devolução.
7. O sistema atualiza a situação do equipamento.
8. O processo é finalizado.

## 3. Diagrama do fluxo

```mermaid
flowchart TD
    A[Início] --> B[Usuário seleciona equipamento]
    B --> C{Equipamento disponível?}

    C -->|Não| D[Informar que não está disponível]
    D --> E[Fim]

    C -->|Sim| F[Registrar empréstimo]
    F --> G[Entregar equipamento]
    G --> H[Registrar devolução]
    H --> I[Atualizar situação do equipamento]
    I --> E
