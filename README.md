# Dividir o Pão

## Sobre o Cliente

O projeto Dividir o Pão é uma iniciativa que surgiu durante a pandemia, em março de 2021, para auxiliar pessoas em situação de rua a se alimentarem, atuando como um banco de captação e distribuição de alimentos. A missão do projeto é mitigar a fome de pessoas em situação de vulnerabilidade, por intermédio de um grupo de voluntários que tem como objetivo distribuir quentinhas pelas ruas e praças de Fortaleza - CE. 

## Sobre o projeto

O projeto é um PWA (híbrido entre _site_ e aplicativo) voltado para _smartphones_ e _desktop_, realizado em parceria com o Dividir o Pão, cujo objetivo é otimizar os processos de captação das listas de insumos (listas de doações e auxílios que cada voluntário faz mensalmente, que guiam os processos de distribuição das doações arrecadadas para os voluntários realizarem os processos de preparação e entrega das quentinhas) e dos cadastros dos voluntários no projeto.

## Sobre a equipe

### Equipe MouseHeros

- Felipe Ferreira do Nascimento
- Marcela Pinto Custódio
- Mateus Marques de Aquino
- Pâmela de Castro Freitas Oliveira 
- Vanessa Rolim de Aquino 


## Mapa de Funcionalidades

### Requisitos implementados
|Requisitos Funcionais Básicos |     Descrição      |  Codificação |
|----------|:-------------:|------:|
| RF_B1. Cadastrar: |  O usuário precisa se cadastrar e fornecer informações pessoais como nome, número de telefone, função no projeto, e-mail e senha.|(Frontend: src\app\pages\signup) ; (Backend: src\modules\user)   |
| RF_B2. Autenticação: |    Com o cadastro, o usuário precisa ser autenticado no banco de dados. Assim, com sua conta registrada no banco, ele pode fazer o login e logout.|(Frontend: src\app\pages\login) ; (Backend: src\modules\voluntario ; src\modules\funcao) |
| RF_B3. Login | O usuário precisa ser capaz de entrar na sua conta.|(Frontend: src\app\pages\login); (Backend: src\modules\voluntario) |
| RF_B4. Logout |  O usuário precisa ser capaz de sair da sua conta.|(Frontend: src\app\core\components\header) ;  (Backend: src\modules\voluntario)  |
| RF_B5. Resetar senha |    O usuário precisa ser capaz de trocar sua senha, caso ele esqueça a mesma.|(Frontend: src\app\pages\reset-password) ; (Backend: *Futura implementação)  |
| RF_B6. Alterar informações pessoais | O usuário precisa ser capaz de alterar suas informações pessoais, como número de telefone, foto de perfil, nome, senha e função.|(Frontend: src\app\pages\update-profile) ; (Backend: *Futura Implementação) |


|Requisitos Funcionais Fundamentais |     Descrição      |  Codificação |
|----------|:-------------:|------:|
| RF_F1. Utilizar banco de dados |  A aplicação utiliza uma base de dados para armazenar os insumos necessários, as informações pessoais dos usuários e as doações. | banco de dados mysql (dividiropao)  |
| RF_F2. Registrar lista de insumos e auxílios |    O usuário pode registrar uma lista de insumos necessários para a sua produção no próximo mês.|(Frontend: src\app\pages\solicitacoes) ; (Backend: src\modules\pedido)    |
| RF_F3. Definir um valor para cada recurso | O usuário (administrador) pode definir o valor de cada recurso (insumo/auxílio) para, assim, o sistema calcular a quantia necessária para comprar todos os produtos por usuário.|(Frontend: src\app\pages\recursos) ; (Backend: src\modules\recurso)     |


|Requisitos Funcionais de Saída |     Descrição      |  Codificação |
|----------|:-------------:|------:|
| RF_S1. Mostrar a lista de insumos/auxílios total |  A aplicação gera uma lista total com todas as solicitações de insumos feitas pelos usuários mensalmente.|(Frontend: src\app\pages\solicitacoes\components) ; (Backend: src\modules\pedido) |
| RF_S2. Mostrar a lista com informações dos usuários | O sistema mostra os dados pessoais como número de telefone, endereço e e-mail dos usuários, facilitando o contato entre colaboradores.|(Frontend: src\app\pages\contatos) ; (Backend: src\modules\voluntario)    |
| RF_S3. Mostrar o valor necessário para comprar todos os insumos/auxílios por voluntário |  O sistema mostra o resultado do cálculo da quantia necessária para comprar todos os produtos por usuário.|(Frontend: src\app\pages\solicitacoes\components\nota-pedido-modal) ; (Backend: src\modules\item-pedido)  |
| RF_S4. Mostrar as doações arrecadadas | O sistema mostra o valor que o projeto já recebeu em dinheiro.|(Frontend: src\app\pages\home\components\alterar-doacao-modal) ; (Backend: src\modules\doacoes)     |


## Como instalar o frontend e executar a aplicação

Para executar a aplicação em seu computador, inicialmente, tenha o Node.js instalado. Tendo esse requisito, abra o código no editor de código de sua preferência e abra o terminal. No terminal, escreva o camando: npm install, para obter os node modules referentes ao projeto e especificados no .json. Depois disso, no terminal, execute o comando: ng serve , para rodar o frontend no seu navegador no localhost:4200.
