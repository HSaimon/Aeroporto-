💼 Atividade de Programação em Java: Sistema de Cadastro de Passageiros
🎯 Objetivo
Desenvolver um sistema simples de cadastro de passageiros utilizando Java, com funcionalidades de validação de CPF e e-mail, armazenamento em memória e testes automatizados.

📦 Requisitos do Sistema
1. Criar a Classe Passageiro

A classe deve conter os seguintes atributos:
int id
String nome
String cpf
String email

Inclua métodos para:

Validar o CPF (utilize uma lógica adequada para verificação de CPF).
Validar o e-mail (use regex ou métodos disponíveis para validação de formato).

2. Armazenamento
Utilize uma ArrayList<Passageiro> para armazenar os objetos da classe Passageiro.

Os passageiros cadastrados devem poder ser recuperados e listados posteriormente.3. Criar Menu Interativo (Console)

Desenvolva um menu simples no método main da classe MainApp, com as seguintes opções:
1 - Cadastrar passageiro
2 - Listar passageiros
3 - Sair

🧪 Testes Automatizados

Utilize JUnit 5 para criar os seguintes testes:
Verificação de CPF válido e inválido.
Verificação de e-mail válido e inválido.
Testar se a função de cadastro está inserindo corretamente os passageiros na lista.

🛠️ Tecnologias e Ferramentas

Linguagem: Java
Gerenciador de dependências: Maven
Framework de testes: JUnit 5
Cobertura de testes: JaCoCo

🧱 Estrutura do Sistema
1. 📄 Classe Passageiro
Atributos:
int id
String nome
String cpf
String email
Requisitos:
Validar CPF (utilize uma lógica correta).
Validar e-mail (regex).

2. 🛩️ Classe Aviao
Atributos:
int id
String modelo
int capacidade
String fabricante
Requisitos:
Validar que a capacidade seja maior que zero.
Cada avião poderá ser associado a um ou mais voos.

3. ✈️ Classe Voo
Atributos:
int id
String origem
String destino
LocalDateTime dataHora
Aviao aviao
Requisitos:
Deve estar vinculado a um avião.
As vagas disponíveis são calculadas com base na capacidade do avião menos o número de reservas existentes.

4. 🎫 Classe Reserva
Atributos:
int id
Passageiro passageiro
Voo voo
LocalDateTime dataReserva
Requisitos:
Deve verificar a disponibilidade de vagas no voo antes de criar a reserva.

🗃️ Armazenamento
Use listas para manter os dados em memória:
ArrayList<Passageiro>
ArrayList<Aviao>
ArrayList<Voo>
ArrayList<Reserva>

🖥️ Menu Interativo no Console
Implemente um menu na classe MainApp com as seguintes opções:
CopyEdit
1 - Cadastrar passageiro  
2 - Listar passageiros  
3 - Cadastrar avião  
4 - Listar aviões  
5 - Cadastrar voo  
6 - Listar voos  
7 - Reservar passagem  
8 - Listar reservas  
9 - Sair

🖥️ Casos de Teste – Sistema de Passagens Aéreas
1. Validação de Passageiros
Testar CPF válido (exemplo: "52998224725") → Deve retornar true
Testar CPF inválido (exemplo: "12345678900") → Deve retornar false
Testar e-mail válido (exemplo: "ana.souza@email.com") → Deve retornar true
Testar e-mail inválido (exemplo: "ana.souza@com") → Deve retornar false
2. Cadastro de Passageiros
Cadastrar passageiro com dados válidos → Deve adicionar à lista
Tentar cadastrar passageiro com CPF inválido → Deve falhar ou lançar exceção
3. Cadastro de Aviões
Cadastrar avião com modelo e capacidade válidos → Deve ser salvo corretamente
Tentar cadastrar avião com capacidade zero → Deve lançar exceção ou falhar
Tentar cadastrar avião com capacidade negativa → Deve lançar exceção ou falhar
4. Cadastro de Voos
Cadastrar voo com origem, destino, data e avião válido → Deve ser salvo corretamente
Tentar cadastrar voo sem avião associado → Deve lançar exceção ou falhar
5. Reserva de Passagens
Criar reserva com vagas disponíveis → Deve ser realizada com sucesso
Criar reserva quando todas as vagas estiverem ocupadas → Deve falhar ou lançar exceção
Criar reserva duplicada para o mesmo passageiro e voo → Deve impedir ou notificar (se implementado)
6. Listagens
Listar passageiros após 3 cadastros → Deve retornar 3 registros
Listar aviões após 2 cadastros → Deve retornar 2 registros
Listar voos após 1 cadastro → Deve retornar 1 registro com dados do avião
Listar reservas após 2 registros → Deve retornar 2 reservas com passageiro e voo
