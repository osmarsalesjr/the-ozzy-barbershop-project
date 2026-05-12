# Documentação Técnica — Projeto Ozzy Barbearia

## 1. Visão Geral do Projeto

A Ozzy Barbearia é uma aplicação web desenvolvida com foco na apresentação de serviços voltados ao cuidado pessoal masculino, incluindo:

- cortes de cabelo;
- barba;
- manicure e pedicure;
- sobrancelhas;
- agendamentos online.

O projeto possui caráter:
- institucional;
- catálogo de serviços;
- experiência visual moderna;
- integração automatizada para agendamentos.

### Público-alvo

Homens interessados em:
- estética masculina;
- cuidados pessoais;
- experiência premium.

---

## Objetivos do Site

O projeto possui como principais finalidades:

- apresentar a marca Ozzy Barbearia;
- comunicar missão e proposta visual;
- expor serviços prestados;
- facilitar contato;
- permitir solicitação de agendamento;
- fortalecer identidade visual e presença digital.

---

## Estrutura Geral

O site segue uma estrutura típica de:
- landing page institucional;
- catálogo de serviços;
- navegação multipágina;
- CMS integrado;
- formulários conectados a automações.

Páginas identificadas:

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

### Evidências Técnicas

Detectado:
- renderização baseada em componentes;
- estrutura típica exportada do Framer;
- roteamento interno automático;
- animações nativas do Framer Motion;
- organização visual baseada em sections/frames;
- assets hospedados via CDN do Framer.

---

## Estratégia Arquitetural

### Modelo estrutural identificado

O site segue:

- arquitetura componentizada;
- reutilização de blocos visuais;
- tema visual centralizado;
- estrutura de design system implícita;
- CMS para renderização dinâmica de serviços.

---

## Frameworks e Bibliotecas Detectadas

| Tecnologia | Status |
|---|---|
| Framer | Detectado |
| React | Provável |
| Framer Motion | Provável |
| CMS Framer | Detectado |
| JavaScript modular | Detectado |
| CSS-in-JS do Framer | Provável |
| Responsividade nativa do Framer | Detectado |
| Make.com | Detectado |
| Google Sheets | Detectado |
| Gmail Integration | Detectado |

---

# 3. Estrutura de Navegação

## Página Inicial

### URL
https://ozzy-barbearia.framer.website/

### Objetivo

- apresentação da marca;
- introdução dos serviços;
- direcionamento para agendamento.

### Componentes Identificados

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

### Estrutura Detectada

- Grid de serviços;
- Cards clicáveis;
- Navegação dinâmica;
- Conteúdo proveniente do CMS.

---

# 4. Estrutura HTML

## Estratégia Estrutural Identificada

O HTML renderizado aparenta seguir o padrão do Framer:

- múltiplos containers `<div>`;
- estrutura em frames;
- uso intenso de classes geradas automaticamente;
- organização hierárquica baseada em componentes.

---

## Elementos Estruturais Detectados

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

## Estratégia Visual Detectada

O projeto utiliza:

- estilização visual centralizada;
- tokens visuais compartilhados;
- padrões consistentes;
- responsividade nativa do Framer.

---

## Sistema Visual

### Características detectadas

- visual minimalista;
- estética premium;
- predominância de contraste;
- foco em tipografia forte;
- imagens de destaque;
- espaçamento generoso.

---

## Responsividade CSS

Detectado:

- menu colapsável;
- adaptação de grids;
- largura relativa;
- containers fluidos;
- reorganização vertical em mobile.

---

# 6. Estrutura JavaScript

## Comportamentos Detectados

| Funcionalidade | Status |
|---|---|
| Navegação dinâmica | Detectado |
| Animações de transição | Detectado |
| Hover animations | Detectado |
| Submit assíncrono | Detectado |
| Integração webhook | Detectado |
| CMS dinâmico | Detectado |

---

## Integrações Externas Detectadas

### Make.com

Fluxo identificado:

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

# 7. Componentes Identificados

## Navbar

### Função
- navegação global;
- acesso rápido às páginas.

### Comportamento
- colapsável em mobile;
- sticky provável.

---

## Hero Section

### Função
- posicionamento visual;
- branding;
- CTA principal.

---

## Cards de Serviço

### Função
- catálogo visual;
- navegação contextual.

### Comportamento
- clique navegável;
- hover visual.

---

## Formulário

### Função
- solicitação de agendamento.

### Integração
- webhook Make.com.

---

## Footer

### Função
- informações institucionais;
- links complementares;
- identidade visual.

---

# 8. Responsividade

## Estratégias Detectadas

### Mobile

Detectado:
- colapso do menu;
- reorganização vertical;
- adaptação de imagens;
- containers fluidos.

---

## Tablet

Provável:
- grids intermediários;
- espaçamentos ajustados.

---

## Desktop

Detectado:
- layout expandido;
- hero horizontal;
- maior uso visual de imagens.

---

# 9. SEO e Performance Aparente

## SEO

### Detectado

- heading hierarchy;
- páginas separadas;
- URLs amigáveis;
- conteúdo institucional estruturado.

### Provável

- meta descriptions;
- Open Graph;
- metadata do Framer.

---

## Performance

### Detectado

- assets otimizados via CDN;
- lazy loading provável;
- otimização automática do Framer;
- imagens responsivas.

---

# 10. Correlação com o Roteiro do Usuário

## Objetivo Institucional

### Requisito

Apresentar a Ozzy Barbearia e seus serviços.

### Evidências Encontradas

- Homepage institucional;
- Sessões explicativas;
- Catálogo visual;
- Página About.

### Implementação Detectada

- estrutura orientada a branding;
- navegação clara;
- CTA para agendamento.

---

## Uso do Framer

### Requisito

Uso de ferramenta visual low-code/no-code.

### Evidências

Detectado:
- padrão estrutural do Framer;
- CMS integrado;
- componentização nativa.

---

## CMS para Serviços

### Requisito

Serviços renderizados dinamicamente.

### Evidências

- páginas `/work/*`;
- estrutura repetitiva consistente;
- comportamento típico de CMS Collection.

---

## Integração Make.com

### Requisito

Automação de agendamentos.

### Evidências

Webhook + Google Sheets + Gmail detectados no cenário anexado.

### Fluxo Detectado

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

# 12. Aplicação de Padrões Web

## HTML

Aplicação observada:
- separação por seções;
- hierarquia visual;
- componentes reutilizáveis.

---

## CSS

Aplicação observada:
- consistência visual;
- design responsivo;
- grid adaptativo;
- tipografia padronizada.

---

## JavaScript

Aplicação observada:
- interatividade;
- transições;
- integração externa;
- renderização dinâmica.

---

# 13. Elementos Customizados Manualmente

## Integração com Make.com

Maior elemento customizado identificado.

### Valor agregado

- automação operacional;
- persistência de dados;
- confirmação automática;
- melhoria da experiência do cliente.

---

## Estrutura CMS

Customização do template base:
- adaptação para catálogo;
- páginas específicas de serviços;
- identidade visual própria.

---

# 14. Cuidados com Responsividade e Acessibilidade

## Responsividade

Implementações detectadas:
- layouts fluidos;
- menu mobile;
- grids adaptativos;
- imagens responsivas.

---

## Acessibilidade

### Detectado

- contraste visual adequado;
- navegação clara;
- botões destacados.

### Não identificado claramente

- ARIA labels;
- navegação via teclado;
- contraste validado WCAG;
- landmarks semânticos avançados.

---

# 15. Aprendizados sobre No-Code/Low-Code

## Benefícios

- aceleração extrema de desenvolvimento;
- facilidade de prototipagem;
- forte integração visual;
- redução de complexidade frontend.

---

## Limitações

- abstração excessiva do HTML;
- menor controle de performance;
- dependência estrutural da plataforma;
- dificuldade de customizações avançadas.

---

# 16. Possíveis Melhorias

## Estruturais

- melhorar semântica HTML;
- adicionar landmarks acessíveis;
- reforçar SEO técnico.

---

## Performance

- otimização adicional de imagens;
- redução de scripts externos;
- controle mais granular de carregamento.

---

## Acessibilidade

- suporte completo a teclado;
- melhorias ARIA;
- validação WCAG.

---

# 17. Conclusão Técnica

O projeto da Ozzy Barbearia demonstra uma implementação sólida utilizando abordagem no-code/low-code através do Framer, com forte foco em:

- identidade visual;
- experiência do usuário;
- responsividade;
- automação operacional;
- catálogo institucional.

A integração com Make.com amplia significativamente as capacidades do site ao transformar um formulário simples em um fluxo automatizado completo envolvendo:
- armazenamento estruturado;
- automação operacional;
- comunicação com clientes.

A arquitetura encontrada mostra uma boa aplicação prática de:
- HTML;
- CSS;
- JavaScript;
- componentização;
- CMS;
- automação web;
- design responsivo.

Mesmo utilizando uma plataforma visual, o projeto evidencia compreensão consistente sobre padrões modernos de desenvolvimento frontend e experiência digital.
