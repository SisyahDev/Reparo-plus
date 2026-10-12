# Reparos+

Plataforma web demonstrativa para aproximar moradores de profissionais de reparos e serviços residenciais. O projeto foi desenvolvido como protótipo acadêmico e utilizado como estudo de caso na disciplina **Arquitetura de Software e Computação em Nuvem**, do curso de Análise e Desenvolvimento de Sistemas.

## Objetivo

Facilitar a busca por profissionais, a comunicação entre moradores e prestadores de serviço e o acompanhamento do processo de orçamento e contratação. O protótipo também apresenta recursos de gestão administrativa e moderação.

## Acessos

- **Site publicado:** https://sisyahdev.github.io/Reparo-plus/
- **Repositório GitHub:** https://github.com/SisyahDev/Reparo-plus/

## Integrantes

| Integrante | Matrícula |
|---|---:|
| Silvya Oliveira | 04155813 |
| Daivison Silva | 04191678 |
| Pedro de Freitas | 04177446 |
| Rian Ramos | 04192826 |

## Perfis e funcionalidades

### Morador
- Buscar e consultar profissionais e serviços.
- Acessar conversas com profissionais autenticando-se na demonstração.
- Receber e analisar orçamentos, com opções de aceitar, recusar ou solicitar negociação.
- Percorrer o fluxo demonstrativo de pagamento e avaliação do serviço.
- Registrar denúncias para análise administrativa.

### Profissional
- Acessar o painel do profissional.
- Consultar conversas e solicitações de orçamento.
- Enviar orçamentos e responder a pedidos de negociação.
- Consultar indicadores demonstrativos de rendimento financeiro.

### Administrador (ADM)
- Consultar indicadores administrativos, como quantidade de profissionais, serviços solicitados e valores demonstrativos.
- Destacar profissionais.
- Consultar informações de moradores e profissionais.
- Acessar o módulo de moderação e acompanhar denúncias.

## Tecnologias e dependências

- **HTML5:** estrutura das telas e do conteúdo.
- **CSS:** estilos complementares e personalizações visuais.
- **JavaScript:** navegação, interações, controle demonstrativo de perfis e fluxos da aplicação.
- **Tailwind CSS via CDN:** classes utilitárias de estilização.
- **Font Awesome via CDN:** ícones da interface.
- **Google Fonts:** fontes utilizadas na apresentação visual.
- **localStorage do navegador:** armazenamento local de dados demonstrativos do protótipo.

O projeto é um protótipo front-end em arquivo HTML, sem servidor próprio ou banco de dados remoto integrado. Os fluxos de autenticação, orçamento, pagamento e indicadores são demonstrativos; não representam autenticação segura, processamento financeiro real nem sincronização entre dispositivos.

## Como executar

### Opção 1 — Site publicado

Acesse: https://sisyahdev.github.io/Reparo-plus/

### Opção 2 — Execução local

1. Clone ou baixe este repositório.
2. Abra a pasta do projeto.
3. Abra o arquivo `index.html` em um navegador atualizado.
4. Para carregar Tailwind CSS, Font Awesome e fontes externas, mantenha uma conexão com a internet.

Não é necessário instalar dependências com npm nem configurar um servidor para visualizar o protótipo básico.

## Organização atual do sistema

A implementação está concentrada principalmente no arquivo `index.html`, que reúne estrutura HTML, estilos e lógica JavaScript. As telas são organizadas como áreas de interface ativadas pela navegação:

- **Busca:** apresentação e consulta de profissionais.
- **Autenticação e navegação por perfil:** entrada demonstrativa e direcionamento para a área correspondente.
- **Área do morador:** conversas, orçamentos, contratação demonstrativa, pagamento e avaliação.
- **Painel profissional:** solicitações, orçamentos e indicadores financeiros demonstrativos.
- **Painel ADM:** indicadores, gestão de destaques e acesso à moderação.
- **Moderação:** visualização e tratamento demonstrativo de denúncias.

O estado e alguns dados de demonstração são mantidos no navegador por meio de `localStorage`. Como a solução ainda está concentrada em um arquivo, há baixo custo de execução e configuração, mas existe acoplamento entre apresentação, navegação e regras de interação. Uma evolução possível é separar a interface, os serviços de aplicação e a persistência de dados, além de introduzir uma API e um banco de dados caso o sistema passe a operar com usuários reais.

## Estrutura do repositório

```text
Reparo-plus/
├── index.html
├── README.md
└── docs/
    └── evidencias/
        └── README.md
```

A pasta `docs/evidencias/` é destinada a capturas de tela e outros registros visuais relevantes para a documentação acadêmica.

## Limitações do protótipo

- Dados armazenados localmente no navegador não são compartilhados entre dispositivos ou usuários.
- Os perfis e fluxos de acesso servem para demonstração e não substituem autenticação e autorização implementadas no servidor.
- Pix, cartão, contratação, orçamento e indicadores financeiros são simulações de interface, sem integração com instituições financeiras.
- Para uso em produção, seriam necessários, entre outros itens, backend, banco de dados, controles de segurança, validação no servidor, tratamento de erros e integração real de pagamentos.

## Contexto acadêmico

O Reparos+ é utilizado como caso de estudo para revisão arquitetural: compreensão da organização atual, identificação de aspectos positivos e limitações, definição de características arquiteturais prioritárias e proposição de evolução da arquitetura.
