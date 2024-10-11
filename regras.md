# Permissionamento

## Cadastro de novo usuário

### Validações que devem ser feitas no usuário logado:
  1. Usuário logado está ativo?
  2. Usuário logado é gestor?
  3. Usuário logado possui permissão para cadastrar novos usuários?

### Validações que devem ser feitas no novo usuário:
  1. CPF é válido?
  2. CPF novo possui restrição no BX?
  3. CPF novo possui restrição na Nuclea?
  4. CPF novo foi marcado como restrito no banco de dados?
  5. Qual loja o novo CPF será cadastrado?
     - Se mesma loja do gestor, OK
     - Se loja diferente, verificar se pertence ao mesmo grupo.
       - Se forem do mesmo grupo, OK
       - Se forem de grupos diferentes, rejeitar cadastro.
  6. Telefone informado do novo usuário já pertence a outro CPF?
     - Se não existir, ou se existir mas estiver marcado como excluído, OK
     - Se existir, rejeita o cadastro
  7. E-mail informado do novo usuário já pertence a outro CPF?
     - Se não existir, ou se existir mas estiver marcado como excluído, OK
     - Se existir, rejeita o cadastro
    
## Digitação de propostas

### Validações a serem feitas no usuário logado
  1. Usuário logado está ativo?
  2. Usuário logado possui alguma restrição?
  3. Usuário logado possui certificados validos?
  4. Usuário logado possui permissão para digitação de propostas?

### Validações que devem ser feitas sobre o CPF do cliente
  1. CPF válido?
  2. CPF do cliente está impedido de operar?
  3. CPF válido na Receita Federal (Bureau/HW)

## Consulta de propostas
  1. Usuário logado está ativo?
  2. Usuário logado possui alguma restrição?
  3. Usuário logado possui permissão de "Visão Digitador"?
  4. A proposta pesquisada pertence ao usuário logado?
  6. Se não pertence ao usuário logado, este usuário possui a permissão "Visão de Grupo"?
     - A loja na qual a proposta foi digitada pertence ao mesmo grupo do usuário?
    
## Relatórios
  1. Usuário logado está ativo?
  2. Usuário logado possui alguma restrição?
  3. Usuário logado possui permissão de "Relatórios"?
  4. O relatório acessado necessita de alguma permissão específica?
  5. O usuáripossui as permissóes específicas necessárias para acesso ao relatório?
