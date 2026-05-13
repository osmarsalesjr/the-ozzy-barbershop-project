# README — Projeto Ozzy Barbearia

## Sobre o Projeto

O projeto **Ozzy Barbearia** é um site institucional desenvolvido utilizando a plataforma **Framer**, com foco em:

- Apresentação da marca;
- Catálogo de serviços;
- Experiência visual moderna;
- Solicitação de agendamentos;
- Automação de atendimento utilizando Make.com.

O site foi construído utilizando recursos no-code/low-code do Framer, combinados com integrações externas para automação operacional.

---

# Tecnologias Utilizadas

## Frontend

- Framer
- CMS do Framer
- Responsividade nativa
- Componentização visual
- Animações do Framer

## Automação

- Make.com
- Webhooks
- Google Sheets
- Gmail

---

# Estrutura do Projeto

## Páginas Principais

| Página | Finalidade |
|---|---|
| `/` | Página inicial |
| `/work` | Catálogo de serviços |
| `/about` | História e missão |
| `/contact` | Página de contato |
| `/appointment` | Solicitação de agendamento |
| `/appointment-response` | Confirmação do envio |

---

# Estrutura de Serviços CMS

Os serviços da Ozzy Barbearia são organizados utilizando o CMS do Framer.

Cada serviço possui:
- Título;
- Descrição;
- Imagem;
- Página dinâmica própria;
- CTA de agendamento.

## Serviços cadastrados

- Corte
- Barba
- Hands and Feet
- Eyebrows

---

# Como Publicar o Projeto no Framer

## Pré-requisitos

- Conta no Framer
- Projeto clonado/importado
- Permissão para edição/publicação

---

## Passo a Passo

### 1. Abrir o Projeto

Acesse:

https://www.framer.com/

Abra o projeto Ozzy Barbearia no dashboard do Framer.

---

### 2. Validar Conteúdo

Antes da publicação:
- Revise textos;
- Valide links;
- Valide páginas;
- Valide imagens;
- Teste o formulário.

---

### 3. Publicar o Projeto

No Framer:

1. Clique em **Publish**
2. Escolha o domínio:
   - Domínio do Framer;
   - Domínio customizado.
3. Confirme a publicação.

### 4. Link Publico do Projeto no Framer

https://framer.com/projects/ozzy-barbearia--KSzOVGVessRh6BpGXYA7-6RIVg

## 5. Link Publico do Website

https://ozzy-barbearia.framer.website/

---

# Estrutura de Agendamento

## Fluxo Funcional

O fluxo de agendamento funciona da seguinte forma:

Cliente → Formulário Framer → Webhook Make.com → Google Sheets → Email automático

---

# Integração com Make.com

## Objetivo da Integração

A integração com Make.com automatiza:

- Recebimento de agendamentos;
- Persistência dos dados;
- Envio de confirmação automática por email.

---

# Cenário Make.com

O cenário já está pronto e exportado no arquivo:

```text
MyAPIWithFramerOzzyBarbearia.blueprint.json
```

---

# Como Importar o Cenário no Make.com

## 1. Acessar o Make.com

Acesse:

https://www.make.com/

---

## 2. Criar um Novo Scenario

No painel:
- clique em **Create a new scenario**

---

## 3. Importar Blueprint

No editor do Make:

1. Clique nos três pontos do cenário
2. Selecione:
   - **Import Blueprint**
3. Faça upload do arquivo:

```text
MyAPIWithFramerOzzyBarbearia.blueprint.json
```
## 4. Link Publico do Cenário

https://us2.make.com/public/shared-scenario/ONa5JF5l0pv/my-apiwith-framer-ozzy-barbearia


---

# Estrutura do Cenário

## Módulo 1 — Webhook

Responsável por:
- receber os dados enviados pelo formulário do Framer.

Campos esperados:
- Name
- Email
- Telefone
- Dia
- Horario
- Servico

---

## Módulo 2 — Google Sheets

Responsável por:
- Armazenar os agendamentos em planilha.

Planilha esperada:
```text
AGENDAMENTOS_OZZY_BARBERIA
```

Aba:
```text
Agendamentos
```

---

## Módulo 3 — Gmail

Responsável por:
- enviar confirmação automática para o cliente.

Conteúdo enviado:
- Confirmação do agendamento;
- Data;
- Horário;
- Imagem da Ozzy Barbearia.

---

# Configuração Necessária Após Importação

## Reconectar Serviços

Após importar o cenário:

### Reconectar:
- Google Sheets
- Gmail
- Google Drive

---

## Validar IDs

Verifique:
- Planilha Google Sheets;
- Webhook;
- Conexões Google;
- Arquivos de imagem utilizados no email.

---

# Configuração do Webhook no Framer

## Objetivo

O formulário do Framer deve enviar os dados para o webhook do Make.com.

---

## Passo a Passo

### 1. Abrir Página de Appointment

Página:
```text
/appointment
```

---

### 2. Selecionar o Formulário

Localize o formulário de agendamento.

---

### 3. Configurar Submit

No formulário:

- método:
```text
POST
```

- endpoint:
```text
Ajustar o Webhook URL do Make.com (Caso tenha criado um novo webhook)
```

---

# Campos Esperados pelo Webhook

O webhook espera exatamente os seguintes campos:

| Campo | Tipo |
|---|---|
| Name | Texto |
| Email | Texto |
| Telefone | Texto |
| Dia | Texto |
| Horario | Texto |
| Servico | Texto |

---

# Estrutura Recomendada do Formulário

```html
<form>
  <input name="Name" />
  <input name="Email" />
  <input name="Telefone" />
  <input name="Dia" />
  <input name="Horario" />
  <input name="Servico" />
</form>
```

---

# Como Testar o Fluxo

## Teste Completo

### 1. Publicar o site

Ajustar form com link webhook em /appointment
Publique o projeto no Framer.

---

### 2. Abrir formulário

Acesse:
```text
/appointment
```

---

### 3. Preencher dados

Envie um agendamento de teste.

---

### 4. Validar execução no Make.com

No cenário:
- Verifique execução do webhook;
- Valide entrada dos dados.

---

### 5. Validar Google Sheets

Confirme se:
- Uma nova linha foi criada.

---

### 6. Validar Email

Confirme:
- Recebimento do email automático.

---

# Estrutura Visual do Projeto

## Componentes Principais

- Navbar
- Hero
- Grid de serviços
- CMS cards
- Footer
- Formulário de agendamento
- CTA sections

---

# Responsividade

O projeto utiliza:
- Layouts fluidos;
- Grids responsivos;
- Menu colapsável;
- Adaptação mobile nativa do Framer.

---

# Boas Práticas Recomendadas

## Framer

- Reutilizar componentes;
- Centralizar estilos;
- Evitar duplicação visual;
- Utilizar CMS sempre que possível.

---

## Make.com

- Manter nomes dos campos consistentes;
- Validar erros de execução;
- Utilizar filtros para evitar dados inválidos;
- Monitorar limite de operações.

---

# Estrutura Recomendada para Desenvolvedores

```text
Projeto Ozzy Barbearia
│
├── Frontend (Framer)
│   ├── Pages
│   ├── CMS
│   ├── Components
│   ├── Styles
│   └── Forms
│
├── Automação (Make.com)
│   ├── Webhook
│   ├── Google Sheets
│   ├── Gmail
│   └── Assets
│
└── Documentação
    ├── README.md
    └── Documentação Técnica
```

---

# Observações Técnicas

## Limitações do Framer

- Menor controle sobre HTML final;
- Classes geradas automaticamente;
- Limitações avançadas de backend;
- Dependência da infraestrutura da plataforma.

---

# Conclusão

O projeto Ozzy Barbearia demonstra uma arquitetura moderna utilizando ferramentas no-code/low-code integradas com automação web.

A combinação entre:
- Framer;
- Make.com;
- Google Sheets;
- Gmail;

permite criar uma experiência funcional, automatizada e escalável sem necessidade de backend tradicional.

O projeto foi estruturado para facilitar:
- Manutenção;
- Evolução futura;
- Reutilização;
- Onboarding de novos desenvolvedores.

Acessa a documentação completa [aqui.](/docs/documentation.pdf)
Assista ao vídeo de apresentação do projeto [aqui.](https://drive.google.com/file/d/1WzrPzscTGI48_sxW96IOHpwx7jTCBqO0/view?usp=sharing)