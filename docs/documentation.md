# Documentação Técnica — Projeto Ozzy Barbearia

## 1. Visão Geral do Projeto

A Ozzy Barbearia é uma aplicação web desenvolvida com foco na apresentação de serviços voltados ao cuidado pessoal masculino, incluindo:

- Cortes de cabelo;
- Barba;
- Manicure e pedicure;
- Sobrancelhas;
- Agendamentos online.

O projeto possui caráter:
- Institucional;
- Catálogo de serviços;
- Experiência visual moderna;
- Integração automatizada para agendamentos.

### Público-alvo

Homens interessados em:
- Estética masculina;
- Cuidados pessoais;
- Experiência premium.

---

## Objetivos do Site

O projeto possui como principais finalidades:

- Apresentar a marca Ozzy Barbearia;
- Comunicar missão e proposta visual;
- Expor serviços prestados;
- Facilitar contato;
- Permitir solicitação de agendamento;
- Fortalecer identidade visual e presença digital.

---

## Estrutura Geral

O site segue uma estrutura típica de:
- Landing page institucional;
- Catálogo de serviços;
- Navegação multipágina;
- CMS integrado;
- Formulários conectados a automações.

Páginas:

| Página | Função |
|---|---|
| Home | Apresentação principal |
| Work | Catálogo de serviços |
| About | História e missão |
| Contact | Contato |
| Appointment | Agendamento |
| Appointment Response | Feedback pós-envio |
| Work/Cut | Serviço de corte |
| Work/Beard | Serviço de barba |
| Work/Hands-and-Feet | Serviço de manicure/pedicure |
| Work/Eyebrows | Serviço de sobrancelha |

---

# 2. Arquitetura Frontend

- Framer

### Informações Técnicas

- Renderização baseada em componentes;
- Estrutura típica exportada do Framer;
- Roteamento interno automático;
- Animações nativas do Framer Motion;
- Organização visual baseada em sections/frames;
- Assets hospedados via CDN do Framer.

---

## Estratégia Arquitetural

### Modelo estrutural

O site segue:

- Arquitetura componentizada;
- Reutilização de blocos visuais;
- Tema visual centralizado;
- Estrutura de design system implícita;
- CMS para renderização dinâmica de serviços.

---

## Frameworks e Bibliotecas

| Tecnologia |
|---|---|
| Framer |
| Framer Motion |
| CMS Framer |
| JavaScript modular |
| CSS-in-JS do Framer |
| Responsividade nativa do Framer |
| Make.com |
| Google Sheets |
| Gmail Integration |

---

# 3. Estrutura de Navegação

## Página Inicial

### URL
https://ozzy-barbearia.framer.website/

### Objetivo

- Apresentação da marca;
- Introdução dos serviços;
- Direcionamento para agendamento.

### Componentes

- Navbar;
- Hero banner;
- Sessões institucionais;
- Cards de serviços;
- CTA buttons;
- Footer.

### Fluxo

Home → Serviços → Agendamento → Resposta de confirmação

---

## Página Work

### URL
https://ozzy-barbearia.framer.website/work

### Objetivo

Apresentar catálogo visual de serviços.

### Estrutura

- Grid de serviços;
- Cards clicáveis;
- Navegação dinâmica;
- Conteúdo proveniente do CMS.

---

# 4. Estrutura HTML

## Estratégia Estrutural

O HTML renderizado aparenta seguir o padrão do Framer:

- Múltiplos containers `<div>`;
- Estrutura em frames;
- Uso intenso de classes geradas automaticamente;
- Organização hierárquica baseada em componentes.

---

## Elementos Estruturais

### Header

```html
<header>
  <nav>
    <a>Home</a>
    <a>Work</a>
    <a>About</a>
    <a>Contact</a>
    <a>Appointment</a>
  </nav>
</header>
```

---

## Hero Section

```html
<section>
  <h1>Branding principal</h1>
  <p>Descrição institucional</p>
  <button>CTA</button>
</section>
```

---

## Cards de Serviço

```html
<article>
  <img />
  <h3>Serviço</h3>
  <p>Descrição</p>
</article>
```

---

## Formulário de Agendamento

```html
<form>
  <input type="text" />
  <input type="email" />
  <input type="tel" />
  <select></select>
  <button type="submit"></button>
</form>
```

---

# 5. Estrutura CSS

## Estratégia Visual

O projeto utiliza:

- Estilização visual centralizada;
- Tokens visuais compartilhados;
- Padrões consistentes;
- Responsividade nativa do Framer.

---

## Sistema Visual

### Características

- Visual minimalista;
- Estética premium;
- Predominância de contraste;
- Foco em tipografia forte;
- Imagens de destaque;
- Espaçamento generoso.

---

## Responsividade CSS

- Menu colapsável;
- Adaptação de grids;
- Largura relativa;
- Containers fluidos;
- Reorganização vertical em mobile.

---

# 6. Estrutura JavaScript

## Comportamentos

| Funcionalidade |
|---|---|
| Navegação dinâmica |
| Animações de transição |
| Hover animations |
| Submit assíncrono |
| Integração webhook |
| CMS dinâmico |

---

## Integrações Externas

### Make.com

Fluxo:

1. Webhook recebe formulário;
2. Dados enviados ao Make.com;
3. Inserção em Google Sheets;
4. Envio de email automático.

---

## Estrutura do Webhook

Campos recebidos:

- Dia;
- Email;
- Horário;
- Nome;
- Serviço;
- Telefone.

---

## Integração Google Sheets

Função:
- persistência de agendamentos.

---

## Integração Gmail

Função:
- confirmação automática ao cliente.

---

# 7. Componentes

## Navbar

### Função
- Navegação global;
- Acesso rápido às páginas.

### Comportamento
- Colapsável em mobile;
- Sticky.

---

## Hero Section

### Função
- Posicionamento visual;
- Branding;
- CTA principal.

---

## Cards de Serviço

### Função
- Catálogo visual;
- Navegação contextual.

### Comportamento
- Clique navegável;
- Hover visual.

---

## Formulário

### Função
- Solicitação de agendamento.

### Integração
- Webhook Make.com.

---

## Footer

### Função
- Informações institucionais;
- Links complementares;
- Identidade visual.

---

# 8. Responsividade

## Estratégias

### Mobile

- Colapso do menu;
- Reorganização vertical;
- Adaptação de imagens;
- Containers fluidos.

---

## Tablet

- Grids intermediários;
- Espaçamentos ajustados.

---

## Desktop

- Layout expandido;
- Hero horizontal;
- Maior uso visual de imagens.

---

# 9. SEO e Performance Aparente

## SEO

- Heading hierarchy;
- Páginas separadas;
- URLs amigáveis;
- Conteúdo institucional estruturado.

---

## Performance

- Assets otimizados via CDN;
- Lazy loading;
- Otimização automática do Framer;
- Imagens responsivas.

---

# 10. Conteúdo e Usuário

## Objetivo Institucional

Apresentar a Ozzy Barbearia e seus serviços.

- Homepage institucional;
- Sessões explicativas;
- Catálogo visual;
- Página About.

### Implementação

- Estrutura orientada a branding;
- Navegação clara;
- CTA para agendamento.

---

## Uso do Framer

Uso de ferramenta visual low-code/no-code com maior disponibilidade de recursos visuais gratuitos e maior intuitividade para implementação e construção de páginas.

- Padrão estrutural do Framer;
- CMS integrado;
- Componentização nativa.

---

## CMS para Serviços

Serviços renderizados dinamicamente.

### Evidências

- Páginas `/work/*`;
- Estrutura repetitiva consistente;
- Comportamento típico de CMS Collection.

---

## Integração Make.com

Automação de agendamentos para guardar os dados do cliente e notificá-lo por email.

### Fluxo

Cliente → Formulário → Make → Planilha → Email automático

---

# 11. Justificativa da Ferramenta Escolhida

## Motivos para utilização do Framer

| Benefício | Impacto |
|---|---|
| Desenvolvimento rápido | Alta produtividade |
| Templates prontos | Redução de esforço inicial |
| Componentização | Consistência visual |
| CMS integrado | Escalabilidade |
| Responsividade nativa | Melhor UX |
| Hospedagem integrada | Simplificação operacional |

---

## Limitações Identificadas

| Limitação | Impacto |
|---|---|
| HTML pouco semântico | SEO técnico limitado |
| Classes geradas automaticamente | Difícil manutenção manual |
| Dependência da plataforma | Menor controle de infraestrutura |
| Estrutura proprietária | Engenharia reversa mais complexa |
| Controle reduzido do bundle JS | Performance avançada limitada |

---

# 12. Elementos Customizados Manualmente

## Integração com Make.com

Integração do formulário de agendamento com Make.com.

### Valor agregado

- Automação operacional;
- Persistência de dados;
- Confirmação automática;
- Melhoria da experiência do cliente.

---

## Estrutura CMS

Customização do template base:
- Adaptação da base para catálogo de serviços;
- Páginas específicas de serviços;
- Identidade visual própria.

---

# 13. Cuidados com Responsividade e Acessibilidade

## Responsividade

- Layouts fluidos;
- Menu mobile;
- Grids adaptativos;
- Imagens responsivas.

---

# 14. Aprendizados sobre No-Code/Low-Code

## Benefícios

- Aceleração extrema de desenvolvimento;
- Facilidade de prototipagem;
- Forte integração visual;
- Redução de complexidade frontend.

---

## Limitações

- Abstração excessiva do HTML;
- Menor controle de performance;
- Dependência estrutural da plataforma;
- Dificuldade de customizações avançadas.

---

# 15. Possíveis Melhorias

## Estruturais

- Melhorar semântica HTML;
- Adicionar landmarks acessíveis;
- Reforçar SEO técnico;
- Validações dos dias e horários de agendamento.

---

## Performance

- Otimização adicional de imagens;
- Redução de scripts externos;
- Controle mais granular de carregamento.

---

# 16. Conclusão Técnica

O projeto da Ozzy Barbearia demonstra uma implementação sólida utilizando abordagem no-code/low-code através do Framer, com forte foco em:

- Identidade visual;
- Experiência do usuário;
- Responsividade;
- Automação operacional;
- Catálogo institucional.

A integração com Make.com amplia significativamente as capacidades do site ao transformar um formulário simples em um fluxo automatizado completo envolvendo:
- Armazenamento estruturado;
- Automação operacional;
- Comunicação com clientes.

A arquitetura mostra uma boa aplicação prática de:
- HTML;
- CSS;
- JavaScript;
- componentização;
- CMS;
- Automação web;
- Design responsivo.

Mesmo utilizando uma plataforma visual, o projeto evidencia compreensão consistente sobre padrões modernos de desenvolvimento frontend e experiência digital.
