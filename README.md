# 🎓 Quiz Anjos

> Plataforma educacional gamificada para criação e aplicação de quizzes interativos em tempo real.

O **Quiz Anjos** é uma aplicação web desenvolvida para tornar revisões e atividades escolares mais dinâmicas, permitindo que professores criem quizzes, iniciem partidas por PIN e acompanhem a participação dos alunos em tempo real.

O projeto também integra **Inteligência Artificial** para auxiliar na criação e revisão pedagógica de quizzes.

---

## 🚀 Sobre o projeto

O Quiz Anjos nasceu da ideia de criar uma solução própria para o ambiente escolar, reunindo em uma única plataforma:

- 🎮 Quizzes interativos em tempo real
- 🔢 Entrada dos participantes por PIN
- 🏆 Ranking e sistema de pontuação
- ⚡ Pontuação baseada em acerto, velocidade e sequência
- 👨‍🏫 Controles exclusivos para o professor
- 📊 Relatórios de desempenho
- 📥 Exportação de resultados em CSV
- 📚 Banco de perguntas
- 🤖 Criação de quizzes com Inteligência Artificial
- ✅ Revisão pedagógica assistida por IA
- ♿ Recursos de acessibilidade
- 📱 Interface adaptada para celulares

---

## 🎮 Como funciona

```text
Professor cria ou seleciona um Quiz
                 ↓
         Criação da partida
                 ↓
        Sistema gera um PIN
                 ↓
       Alunos entram na sala
                 ↓
        Professor inicia
                 ↓
         Pergunta exibida
                 ↓
        Alunos respondem
                 ↓
     Pontuação + classificação
                 ↓
          Próxima pergunta
                 ↓
          Resultado final
```

O professor controla o andamento da atividade enquanto os alunos utilizam seus próprios dispositivos para responder.

---

## 👨‍🏫 Recursos para o professor

O apresentador possui controles para:

- iniciar a partida;
- avançar entre perguntas;
- pausar e retomar;
- finalizar uma partida;
- bloquear a entrada de novos participantes;
- remover participantes;
- acompanhar respostas;
- visualizar o ranking;
- acessar relatórios.

Cada partida possui uma chave exclusiva para proteger os controles destinados ao apresentador.

---

## 🏆 Sistema de pontuação

A pontuação considera três fatores principais:

**✅ Acerto + ⚡ Velocidade + 🔥 Sequência de acertos**

Respostas corretas realizadas mais rapidamente podem receber mais pontos.

O sistema também oferece bônus conforme o participante mantém uma sequência de respostas corretas.

---

## 🤖 Inteligência Artificial

O Quiz Anjos possui integração com **Gemini** para auxiliar professores na preparação das atividades.

### ✨ Geração de quizzes

A IA pode gerar um rascunho de quiz utilizando informações como:

- disciplina;
- série/ano;
- dificuldade;
- quantidade de perguntas;
- texto de referência;
- materiais de apoio.

O resultado gerado pode conter perguntas, alternativas, resposta correta, tempo e explicação.

**A IA não publica automaticamente o conteúdo.**

O quiz é apresentado como rascunho para que o professor revise antes de salvá-lo.

---

## ✅ Revisão pedagógica com IA

Um quiz também pode passar por uma análise assistida por Inteligência Artificial.

A ferramenta procura possíveis problemas como:

- perguntas ambíguas;
- alternativas óbvias;
- mais de uma resposta possível;
- repetição;
- possíveis erros factuais;
- linguagem inadequada.

A análise retorna uma avaliação e sugestões.

> A decisão final permanece sempre com o professor.

---

## 📚 Banco de Perguntas

Perguntas de quizzes anteriormente criados podem ser pesquisadas e reutilizadas.

Isso permite construir gradualmente um banco institucional de questões e reduz a necessidade de recriar conteúdos semelhantes.

---

## 📊 Relatórios

Após uma atividade, o professor pode analisar o desempenho dos participantes.

### Por participante

- Nome
- Pontuação
- Acertos
- Total de respostas
- Aproveitamento

### Por pergunta

- Quantidade de respostas
- Quantidade de acertos
- Percentual de acerto

Os resultados também podem ser exportados em **CSV**.

---

## ♿ Acessibilidade

O projeto inclui recursos como:

- 🔎 ampliação dos textos;
- ◐ alto contraste;
- suporte a `aria-label`;
- avisos utilizando `aria-live`;
- navegação por teclado;
- botões grandes para respostas;
- identificação das alternativas por formas geométricas;
- modo tela cheia.

---

## 🛠️ Tecnologias

### Front-end

- HTML
- CSS
- JavaScript
- LocalStorage
- Web APIs

### Back-end

- Google Apps Script
- JavaScript
- PropertiesService
- CacheService
- LockService

### Inteligência Artificial

- Gemini API

---

## 🏗️ Arquitetura

```text
┌──────────────────────────────┐
│          USUÁRIOS            │
│                              │
│     Professor     Aluno      │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│        INTERFACE WEB         │
│                              │
│   HTML + CSS + JavaScript    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     GOOGLE APPS SCRIPT       │
│                              │
│ • Quizzes                    │
│ • Partidas                   │
│ • Pontuação                  │
│ • Ranking                    │
│ • Relatórios                 │
│ • Banco de Perguntas         │
└───────────┬──────────┬───────┘
            │          │
            ▼          ▼
    ┌────────────┐  ┌───────────┐
    │ Properties │  │ Gemini API│
    │   / Cache  │  │    IA     │
    └────────────┘  └───────────┘
```

---

## 🔐 Segurança

O projeto implementa mecanismos como:

- sanitização das entradas;
- tokens individuais para participantes;
- chave exclusiva para o apresentador;
- bloqueio de operações concorrentes com `LockService`;
- proteção da chave da API no back-end;
- controle de entrada nas partidas;
- prevenção de respostas duplicadas.

> ⚠️ A versão pública deste repositório não deve conter chaves de API, e-mails, domínios privados ou outras configurações internas da instituição.

---

## 📁 Estrutura do projeto

```text
quiz-anjos/
│
├── README.md
│
├── src/
│   ├── Code.gs
│   └── Index.html
│
├── docs/
│   └── documentacao.md
│
├── screenshots/
│
├── .gitignore
└── LICENSE
```

---

## 📸 Screenshots

Em breve serão adicionadas imagens demonstrando:

- Tela inicial
- Criação de quiz
- Criação com IA
- Lobby da partida
- Tela do professor
- Tela do participante
- Ranking
- Relatórios
- Banco de perguntas

---

## 🎯 Objetivo

O projeto busca demonstrar como uma necessidade real do ambiente escolar pode ser transformada em uma solução tecnológica própria.

Além do desenvolvimento da aplicação, o projeto envolve:

- levantamento de necessidades;
- desenvolvimento web;
- regras de negócio;
- experiência do usuário;
- gamificação;
- acessibilidade;
- integração com APIs;
- Inteligência Artificial;
- análise de resultados.

---

## 🔮 Próximas evoluções

Algumas possibilidades estudadas para futuras versões:

- autenticação estruturada para professores;
- organização de quizzes por disciplina;
- categorias e tags;
- histórico individual de alunos;
- dashboards pedagógicos;
- banco de dados dedicado;
- testes automatizados;
- melhorias de escalabilidade;
- novos formatos de perguntas.

---

## 👨‍💻 Desenvolvedor

**Caio Luan Silva**

Auxiliar de TI | Estudante de Tecnologia da Informação

Projeto desenvolvido a partir de uma necessidade identificada no ambiente educacional, buscando aplicar tecnologia para melhorar processos e apoiar professores e alunos.

---

## 📄 Documentação

A documentação técnica completa do projeto está disponível na pasta:

`/docs`

---

⭐ **Quiz Anjos — Tecnologia aplicada à educação.**
