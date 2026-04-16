# Health Connect - Sistema de Gestão de Prontuários para CAPSi

## 📌 Descrição do Projeto

O **Health Connect** é um sistema web desenvolvido para informatizar os prontuários físicos no Centro de Atenção Psicossocial Infantojuvenil (CAPSi).  

Seu objetivo é facilitar o gerenciamento de informações dos pacientes, promovendo um atendimento mais eficiente, organizado e seguro, além de garantir a confidencialidade dos dados conforme a LGPD.

---

## 🎯 Objetivo do Sistema

Desenvolver uma solução digital para substituir prontuários físicos, permitindo:

- Melhor organização das informações;
- Agilidade no atendimento clínico;
- Redução de erros e perda de dados;
- Apoio à tomada de decisão com relatórios.

---

## 🏥 Contexto de Aplicação

O sistema foi desenvolvido para o **CAPSi**, responsável pelo atendimento de crianças e adolescentes com transtornos mentais.

A informatização dos prontuários contribui para:

- Acompanhamento clínico mais eficiente;
- Centralização das informações;
- Melhoria nos serviços de saúde mental;
- Apoio às políticas públicas de saúde.

---

## ⚙️ Funcionalidades Principais

- **Gerenciamento de Prontuários**
  - Cadastro e atualização de pacientes
  - Histórico médico e familiar

- **Acesso Controlado**
  - Diferentes níveis de usuários (admin, profissional, secretária)

- **Busca Avançada**
  - Localização rápida de informações

- **Relatórios e Métricas**
  - Estatísticas e acompanhamento clínico

- **Segurança de Dados**
  - Criptografia e conformidade com a LGPD

---

## 🧠 Metodologia

O sistema foi desenvolvido utilizando o modelo **Cascata (Waterfall)**, seguindo as etapas:

1. Análise e definição de requisitos  
2. Projeto do sistema  
3. Implementação  
4. Testes  
5. Implantação  

Essa abordagem permitiu um desenvolvimento estruturado e controlado.

---

## 📋 Análise e Definição de Requisitos

A coleta de requisitos foi realizada no CAPSi (Alegrete/RS), utilizando:

- **Entrevistas** com profissionais da saúde  
- **Análise de documentos** (prontuários e relatórios)  
- **Observação** do fluxo de trabalho  

---

## 📌 Requisitos do Sistema

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

---

## 🧩 Regras de Negócio

- Apenas profissionais autorizados acessam prontuários  
- Secretárias não acessam dados clínicos sensíveis  
- Todo atendimento deve estar vinculado a um paciente  
- O sistema mantém histórico de alterações  

---

## 🏗️ Arquitetura do Sistema

O sistema segue o modelo cliente-servidor:

- **Frontend:** Interface com o usuário  
- **Backend:** Regras de negócio (PHP)  
- **Banco de Dados:** Armazenamento (MySQL)  

Comunicação via requisições HTTP com AJAX.

---

## 💻 Tecnologias Utilizadas

- **Frontend**  
  [![](https://skillicons.dev/icons?i=html,css,bootstrap,javascript,jquery,ajax)](https://skillicons.dev)

- **Backend**  
  [![](https://skillicons.dev/icons?i=php)](https://skillicons.dev)

- **Banco de Dados**  
  [![](https://skillicons.dev/icons?i=mysql)](https://skillicons.dev)

- **Controle de Versão**  
  [![](https://skillicons.dev/icons?i=git,github)](https://skillicons.dev)

---

## 👥 Usuários do Sistema

- **Administrador**
  - Gerencia usuários e relatórios  

- **Profissional de Saúde**
  - Realiza atendimentos e registros  

- **Secretária**
  - Cadastra pacientes e agenda consultas  

- **Paciente**
  - Crianças e adolescentes atendidos  

---

## 🔍 Casos de Uso

- Cadastrar pacientes  
- Consultar prontuários  
- Registrar atendimentos  
- Gerar relatórios  
- Gerenciar usuários  

---

## 🚀 Instalação e Configuração

### 1. Instalar o XAMPP

Baixe: https://www.apachefriends.org/pt_br/index.html  
Inicie:
- Apache  
- MySQL  

---

### 2. Clonar o repositório

```bash
git clone https://github.com/Bscanto/Health-Connect-.git
