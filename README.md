# 🏥 Cliniflow: Sistema de Gestão e Marcação de Consultas

> **Descomplique a Marcação.** Um fluxo rápido, eficiente e moderno para clínicas.

## 💔 O Problema

Em uma clínica de médio porte em minha cidade, a marcação de consultas ainda é um processo **manual**, dependente de cadernos, agendas de papel, ou planilhas desconectadas.

Este método arcaico gera uma série de ineficiências:

* **Lentidão:** O processo de agendar um paciente, checar a disponibilidade do médico e registrar a consulta é demorado e propenso a interrupções.
* **Erros Humanos:** Dificuldade em conciliar horários, resultando em **dupla marcação** (overbooking) ou agendamentos em horários inválidos.
* **Baixa Produtividade:** Secretárias e atendentes gastam tempo excessivo com a organização da agenda, desviando o foco do atendimento humanizado.
* **Falta de Dados:** Impossibilidade de gerar relatórios rápidos sobre o volume de pacientes ou o desempenho dos médicos.

## ✨ A Solução: Cliniflow

O **Cliniflow** nasce com o objetivo de **digitalizar e otimizar** a gestão da agenda de clínicas, transformando a marcação de consultas em um **"Flow" (fluxo)** rápido, intuitivo e à prova de erros.

Nosso foco é na **Experiência do Usuário (UX)**, garantindo que o ciclo completo — do registro do paciente à confirmação da consulta — seja concluído com o mínimo de cliques e o máximo de clareza.

### Principais Benefícios do Cliniflow:

* **Marcação em 3 Passos:** Redução drástica do tempo necessário para agendar uma consulta.
* **Visualização Clara da Agenda:** Calendários interativos para médicos e atendentes.
* **Registro Centralizado:** Todas as informações de **Paciente**, **Médico** e **Consulta** em um único lugar.
* **Base para Expansão:** Arquitetura robusta para futuras integrações (ex: lembretes automáticos por SMS/WhatsApp, prontuário eletrônico).

## 🛠️ Tecnologias Utilizadas

Este projeto é construído sobre uma arquitetura robusta e moderna, utilizando as seguintes tecnologias:

| Categoria | Tecnologia |
| :--- | :--- | :--- |
| **Backend** | **Java** |
| **Framework** | **Spring Boot** | 
| **Frontend** | **JSF (JavaServer Faces)** 
| **Frontend (Suporte)** | **PrimeFaces** |
| **Banco de Dados** | **H2 (Em Desenvolvimento)** | **Postgres(AWS)
| **Persistência** | **JPA / Hibernate** | 

## 📊 Entidades Principais (A Estrutura do Sistema)

A fundação do Cliniflow reside em três entidades principais, já implementadas na API:

| Entidade | Descrição | Relacionamentos Chave |
| :--- | :--- | :--- |
| **Paciente** | Representa a pessoa que será atendida. Contém informações básicas de cadastro (nome, CPF, contato). | *1:N* com **Consulta** (Um Paciente pode ter muitas Consultas). |
| **Médico** | Representa o profissional de saúde. Contém informações de identificação e especialidade. | *1:N* com **Consulta** (Um Médico pode atender muitas Consultas). |
| **Consulta** | O agendamento em si. Contém a data, hora, status e a ligação entre as outras entidades. | *N:1* com **Paciente** e *N:1* com **Médico**. |

