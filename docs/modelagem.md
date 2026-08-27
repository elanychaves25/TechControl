# Modelagem do Sistema TechControl

## 1. Objetivo da modelagem

A modelagem representa o funcionamento básico do sistema TechControl, desenvolvido para controlar o empréstimo de equipamentos.

O fluxo apresenta as principais operações do sistema: cadastro de equipamentos, consulta, empréstimo, devolução, acompanhamento da situação dos equipamentos e consulta do histórico.

## 2. Fluxo geral do sistema

O usuário acessa o sistema e escolhe a operação que deseja realizar. A partir dessa escolha, o sistema executa o processo correspondente.

As principais operações são:

- Cadastrar equipamentos;
- Consultar equipamentos;
- Realizar empréstimos;
- Registrar devoluções;
- Consultar a situação dos equipamentos;
- Consultar o histórico de empréstimos e devoluções.

## 3. Diagrama do fluxo

```mermaid
flowchart TD

A([Início]) --> B[Usuário acessa o sistema]
B --> C{Escolher operação}

C --> D[Cadastrar equipamento]
C --> E[Consultar equipamentos]
C --> F[Realizar empréstimo]
C --> G[Registrar devolução]
C --> H[Consultar situação]
C --> I[Consultar histórico]

D --> D1[Informar nome e identificação]
D1 --> D2[Registrar equipamento]
D2 --> D3[Definir situação do equipamento]
D3 --> J([Fim])

E --> E1[Visualizar equipamentos cadastrados]
E1 --> E2{Qual é a situação?}
E2 -->|Disponível| E3[Exibir como disponível]
E2 -->|Emprestado| E4[Exibir como emprestado]
E2 -->|Indisponível| E5[Exibir como indisponível]
E3 --> J
E4 --> J
E5 --> J

F --> F1[Selecionar equipamento]
F1 --> F2[Informar usuário responsável]
F2 --> F3[Informar data de retirada]
F3 --> F4{Equipamento disponível?}
F4 -->|Sim| F5[Registrar empréstimo]
F5 --> F6[Atualizar situação para emprestado]
F6 --> J
F4 -->|Não| F7[Informar que o equipamento não está disponível]
F7 --> J

G --> G1[Selecionar equipamento emprestado]
G1 --> G2[Registrar devolução]
G2 --> G3[Atualizar situação para disponível]
G3 --> J

H --> H1[Selecionar equipamento]
H1 --> H2[Visualizar situação atual]
H2 --> J

I --> I1[Consultar registros anteriores]
I1 --> I2[Visualizar empréstimos e devoluções]
I2 --> J
