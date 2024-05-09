## Documentação do Modelo Relacional

**Projeto:** Abandono Zero

**Data:** 2024-05-08

**Autor:** Davi Abreu da Silveira

**Objetivo:** Descrever o modelo relacional do projeto de forma resumida e simplificada.

## Entidades

- **Usuários** (`users`): Armazena informações básicas sobre todos os usuários (email, senha, data de registro, cargo).
- **Formulário Comum** (`commom_form`): Detalhes comuns do usuário que responde ao formulário (nome, idade, sexo, educação, tipo de moradia, composição familiar, renda familiar, número de pessoas na casa, país, estado, cidade, bairro).
- **Formulário Usuário que já teve Cães** (`past_form`): Informações sobre o usuário que em seu histório já teve outro(s) cães (já teve outros cães, já teve outros gatos, gostaria de ter um novo cão).
- **Formulário de Úsuário que Quer Ter Cães no Futurp** (`want_dog_future_form`): Informações sobre os cães que o usuário deseja ter no futuro (características imaginárias do cão desejado, razões para querer um cão, preferência entre adotar ou comprar, previsão de compra, preferência de personalidade do cão, custos mensais médios estimados).
- **Formulário de Presente com Cães** (`present_form`): Informações sobre o cão atual do usuário (possui outros cães, possui outros gatos, razões para ter ou não poder manter um cão atualmente).
- **Formulário com Informações do Cão de Usuário que já Teve Cão** (`past_dog`): Informações sobre os cães anteriores do usuário (nome do cão, tutor, personalidade do cão, se foi o primeiro cão, se foi castrado, idade na castração, raça, idade quando adquirido, origem do cão, valor pago, motivo da aquisição, personalidades que mais gostava e menos gostava, visitas ao veterinário, razões das visitas ao veterinário, data de saída, idade na saída, motivo da saída).
- **Formulário Usuário que não Quer ter um Cão no Futuro** (`dont_want_dog_future_form`): Razões do usuário para não querer um cão no futuro.
- **Formulário com Informações do Cão de Usuário que Possui Cão** (`present_dog`): Informações sobre o cão atual do usuário (nome do cão, sexo do cão, tutor, se foi castrado, tempo com o cão, se é o primeiro cão, raça, origem do cão, valor pago, idade do cão ao ser adquirido, personalidade do cão, razões para ter o cão, características do cão que o tutor gosta, pessoas envolvidas na decisão de ter o cão, visitas ao veterinário, número de vezes que foi ao veterinário, se outras pessoas estariam dispostas a adotar o cão).

## Relacionamentos

- Um usuário pode ter um único formulário comum (1:1).
- Cada formulário específico está associado a um formulário comum (1:1).
- Um usuário pode ter vários formulários relacionados a cães (1:N).
- Cada formulário de cão está associado a um formulário específico (1:1).

## Regras de Negócio

- Todos os campos obrigatórios devem ser preenchidos.
- As informações devem ser consistentes entre os formulários.
- Os usuários não podem editar informações já salvas, exceto em casos específicos.
- As informações dos usuários são confidenciais.

## Considerações Finais

Este modelo relacional simplificado fornece uma base para o gerenciamento eficiente das informações dos usuários e suas respostas nos formulários do projeto Abandono Zero. As entidades, seus atributos e relacionamentos garantem a organização e a integridade dos dados. As regras de negócio garantem a consistência e a confiabilidade das informações.

**Observações:**

- Este modelo é uma versão simplificada e pode ser adaptado às necessidades específicas do projeto.
- É importante documentar detalhadamente o modelo relacional para facilitar o entendimento e a manutenção do sistema.
- A implementação do modelo relacional deve seguir boas práticas de desenvolvimento de banco de dados.