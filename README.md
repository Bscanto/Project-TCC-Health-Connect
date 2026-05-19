# Health Connect - Sistema de Gestão de Prontuários para CAPSi

## 📌 Descrição do Projeto

O **Health Connect** é um sistema web desenvolvido para informatizar os prontuários físicos no Centro de Atenção Psicossocial Infantojuvenil (CAPSi). Seu objetivo é facilitar o gerenciamento das informações dos pacientes, promovendo um atendimento mais eficiente, organizado e seguro, além de garantir a confidencialidade dos dados conforme a LGPD.

## 🎯 Objetivo do Sistema

Desenvolver uma solução digital que substitua prontuários físicos, permitindo:

- Melhor organização das informações;
- Agilidade no atendimento clínico;
- Redução de erros e perda de dados;
- Apoio à tomada de decisão com relatórios.

## 🏥 Contexto de Aplicação

O sistema foi desenvolvido para o CAPSi, que atende crianças e adolescentes com transtornos mentais. A informatização dos prontuários contribui para:

- Acompanhamento clínico mais eficiente;
- Centralização das informações;
- Melhoria nos serviços de saúde mental;
- Apoio às políticas públicas de saúde.

## ⚙️ Funcionalidades Principais

### Gerenciamento de Prontuários

- Cadastro e atualização de pacientes.
- Registro de histórico médico e familiar.

### Acesso Controlado

- Diferentes níveis de usuário: administrador, profissional e secretária.
- Controle por permissões para proteger dados sensíveis.

### Busca Avançada

- Localização rápida de informações do paciente e de suas consultas.

### Relatórios e Métricas

- Estatísticas de atendimentos e consultas.
- Impressão de fichas e relatórios em PDF.

### Segurança de Dados

- Uso de criptografia para senhas.
- Estrutura pensada para apoiar conformidade com a LGPD.

## 🧠 Metodologia

O projeto seguiu o modelo Cascata (Waterfall) com as seguintes etapas:

- Análise e definição de requisitos
- Projeto do sistema
- Implementação
- Testes
- Implantação

Essa abordagem permitiu um desenvolvimento estruturado e controlado.

## 📋 Análise e Definição de Requisitos

A coleta de requisitos foi realizada no CAPSi, em Alegrete/RS, por meio de:

- Entrevistas com profissionais da saúde
- Análise de documentos (prontuários e relatórios)
- Observação do fluxo de trabalho

### Requisitos Funcionais

- Cadastro de pacientes
- Registro de atendimentos
- Consulta de prontuários
- Geração de relatórios
- Controle de usuários

### Requisitos Não Funcionais

- Segurança conforme LGPD
- Alto desempenho
- Interface intuitiva
- Controle de acesso por níveis
- Integridade dos dados

### Regras de Negócio

- Apenas profissionais autorizados acessam prontuários.
- Secretárias não acessam dados clínicos sensíveis.
- Todo atendimento deve estar vinculado a um paciente.
- O sistema mantém histórico de alterações.

## 🧩 Arquitetura do Sistema

O sistema segue o modelo cliente-servidor:

- Frontend: interface do usuário
- Backend: regras de negócio em PHP
- Banco de dados: armazenamento em MySQL
- Comunicação: requisições HTTP com AJAX

## 💻 Tecnologias Utilizadas

- Frontend: HTML, CSS, Bootstrap 5, jQuery, DataTables
- Backend: PHP com PDO
- Banco de dados: MySQL
- PDF: DOMPDF
- Controle de versão: Git

## 👥 Usuários do Sistema

- **Administrador**
  - Gerencia usuários e relatórios.
- **Profissional de Saúde**
  - Realiza atendimentos e registros.
- **Secretária**
  - Cadastra pacientes e agenda consultas.
- **Paciente**
  - Crianças e adolescentes atendidos no CAPSi.

## 🔍 Casos de Uso

- Cadastrar pacientes
- Consultar prontuários
- Registrar atendimentos
- Gerar relatórios
- Gerenciar usuários

## 🚀 Instalação e Configuração

### 1. Instalar o XAMPP

Baixe em: https://www.apachefriends.org/pt_br/index.html

Inicie:

- Apache
- MySQL

### 2. Clonar o repositório

```bash
git clone https://github.com/Bscanto/Health-Connect-.git
```

### 3. Copiar para o XAMPP

Copie a pasta do projeto para `htdocs`.

### 4. Criar o banco de dados

Acesse `http://localhost/phpmyadmin` e crie o banco `health`.

### 5. Importar o arquivo SQL

Importe `health.sql` para criar as tabelas iniciais.

### 6. Configurar `conexao.php`

Ajuste os dados do banco:

```php
$servidor = 'localhost';
$banco = 'health';
$usuario = 'root';
$senha = '';
```

### 7. Acessar o sistema

Use a URL correta no navegador, por exemplo:

```text
http://localhost/Project-TCC-Health-Connect-main/
```

> Ajuste conforme o nome da pasta no `htdocs`.

## 🗂️ Estrutura de Pastas

- `index.php` - página de login
- `autenticar.php` - validação de login
- `recuperar-senha.php`, `alterar-senha.php`, `resetar-senha.php` - fluxo de recuperação de senha
- `conexao.php` - conexão com o banco
- `health.sql` - estrutura e dados iniciais do banco
- `painel/` - área administrativa
- `painel/paginas/` - módulos de cadastro e consulta
- `painel/relatorios/` - geração de relatórios em PDF
- `painel/dompdf/` - biblioteca DOMPDF

## 🗄️ Banco de Dados

Tabelas principais:

- `usuarios`
- `paciente`
- `acao_realizada`
- `anamnese`
- `config`
- `grupo_acessos`
- `usuarios_permissoes`

### Observação de segurança

O sistema usa `sha1()` para hash de senha no campo `senha_crip`. Para produção, é recomendada a migração para `password_hash()`.

## 🔒 Boas Práticas e Segurança

- Não deixe `display_errors` ativo em produção.
- Use credenciais seguras no banco de dados.
- Sanitizar entradas de formulários.
- Validar permissões antes de exibir dados sensíveis.

## 🚧 Melhorias Recomendadas

- Migrar para `password_hash()` e `password_verify()`.
- Implementar expiração de sessão.
- Adicionar proteção CSRF nos formulários.
- Melhorar tratamento de erros do PDO.

## 📄 Licença

Este projeto está licenciado sob a **Apache License 2.0**.
Veja o arquivo `LICENSE` para mais detalhes.
