# Recuperação de Senha

**RF(Requisitos funcionais)**
- O usuário deve poder recuperar sua senha informando o seu email;
- O usuário deve poder receber um email com instruções de recuperação de senha;
- O usuário deve poder resetar sua senha;

**RNF(Requisitos não funcionais)**
- Utilizar Mailtrap para testar envio de email em dev;
- Utilizar o Amazon SES para envios em produção;
- O envio de emails deve acontecer em segundo plano (background job);

**RN(Regras de negocio)**
- O link enviado por email para resetar senha, deve expirar em 2hrs;
- O usuário precisa confirmar a nova senha ao receber o email de recuperação

# Atualizaçào de perfil

**RF**

- O usuário deve poder atualizar nome, email e senha;

**RN**

- O usuário não pode alterar seu email para um email já utilizado;
- Para atualizar sua senha, o usuário deve informar a senha antiga;
- Para atualizar a sua senha, o usuário precisa confirmar a nova senha;


# Painel do prestador

**RF**

- O usuário deve poder listar seus agendamentos de um dia específico;
- O prestador deve receber uma notificação sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notificações não lidas;

**RNF**

- Os agendamentos do prestador no dia devem ser armazenados no cache;
- As notificações do prestador devem ser armazenadas no MongoDB;
- As notificações devem ser enviadas em tempo-real utilizando Sockte.io

**RN**

- A notificação deve ter um status de lida ou não-lida para que o prestador possa controlar;

# Agendamento de serviços

**RF**

- O usuário deve poder listar todos os prestadores de serviço cadastrados;
- O usário deve poder listar os dias de um mês com pelo menis um horário disponível de um prestador;
- O usuário deve poder listar hórarios disponíveis em um dia específico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador;

**RNF**

- Listagem de prestadores deve ser armazenada em cache;

**RN**

- Cada agendamento deve durar 1hr exatemente;
- Os agendamentos devem estar disponíveis entre 8 às 18h (Primeiro às 8h, último às 17h);
- O usuário não pode agendar em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar serviços consigo mesmo;


