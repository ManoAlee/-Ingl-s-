# Past Verbs Study Site - Documentação

## Visão Geral

Este projeto é um site interativo para estudo de verbos no passado em inglês, desenvolvido com React, TypeScript, Tailwind CSS, shadcn/ui e Framer Motion. O site oferece uma experiência completa de aprendizado com várias funcionalidades interativas e uma base de dados acadêmica confiável.

## Funcionalidades

1. **Autenticação de Usuário**
   - Login simples com armazenamento no localStorage
   - Persistência de sessão entre visitas
   - Personalização da experiência com nome do usuário

2. **Quiz Interativo**
   - Perguntas sobre Past Simple e Past Continuous
   - Validação em tempo real das respostas
   - Feedback visual de acerto/erro com explicações
   - Registro de pontuação no histórico de progresso

3. **Transformação de Frases**
   - Exercícios para transformar frases entre Past Simple e Past Continuous
   - Exemplos interativos com explicações detalhadas
   - Baseado em exemplos acadêmicos de uso real

4. **Mini-histórias**
   - Textos curtos com verbos no passado destacados
   - Explicações contextuais sobre o uso dos tempos verbais
   - Múltiplas histórias com diferentes níveis de complexidade

5. **Lista de Verbos**
   - Tabela completa de verbos irregulares
   - Sistema de busca e filtragem
   - Informações sobre forma base, passado simples, particípio passado e significado
   - Exemplos de uso em frases contextualizadas

6. **Sistema de Progresso**
   - Armazenamento local do histórico de atividades
   - Visualização de pontuações anteriores
   - Estatísticas de desempenho

7. **Exportação em PDF**
   - Geração de relatórios de progresso em PDF
   - Personalização com dados do usuário
   - Histórico de pontuações e datas de acesso

## Estrutura do Projeto

```
past-verbs-study-site/
├── my-app/                  # Diretório principal do projeto React
│   ├── public/              # Arquivos públicos
│   ├── src/                 # Código-fonte
│   │   ├── components/      # Componentes React
│   │   │   ├── ui/          # Componentes de UI do shadcn/ui
│   │   │   ├── Login.tsx    # Componente de login
│   │   │   ├── Quiz.tsx     # Componente de quiz
│   │   │   ├── Transform.tsx # Componente de transformação de frases
│   │   │   ├── Story.tsx    # Componente de mini-histórias
│   │   │   ├── VerbTable.tsx # Componente de tabela de verbos
│   │   │   ├── Progress.tsx # Componente de progresso
│   │   │   ├── ExportPDF.tsx # Componente de exportação PDF
│   │   │   └── PastVerbsStudySite.tsx # Componente principal
│   │   ├── data/            # Dados do aplicativo
│   │   │   ├── verbList.js  # Lista de verbos irregulares
│   │   │   ├── quizData.js  # Dados do quiz
│   │   │   ├── transformationData.js # Dados de transformação
│   │   │   └── storyData.js # Dados de mini-histórias
│   │   ├── App.tsx          # Componente App
│   │   └── index.tsx        # Ponto de entrada
│   ├── package.json         # Dependências e scripts
│   └── tsconfig.json        # Configuração TypeScript
└── project-structure.md     # Documentação da estrutura do projeto
```

## Tecnologias Utilizadas

- **React**: Biblioteca JavaScript para construção de interfaces
- **TypeScript**: Superset tipado de JavaScript
- **Tailwind CSS**: Framework CSS utilitário
- **shadcn/ui**: Componentes de UI reutilizáveis
- **Framer Motion**: Biblioteca para animações
- **jsPDF**: Biblioteca para geração de PDFs
- **LocalStorage API**: Para persistência de dados local

## Fontes Acadêmicas

Os dados utilizados neste projeto foram compilados a partir de fontes acadêmicas confiáveis:

1. **Universidade Veracruzana**: Lista de verbos irregulares
2. **Cambridge English**: Exemplos de uso e estrutura gramatical
3. **British Council**: Exemplos contextualizados e explicações didáticas

## Instalação e Execução

### Pré-requisitos

- Node.js (versão 14 ou superior)
- npm ou pnpm

### Passos para Instalação

1. Clone o repositório:
   ```
   git clone [URL_DO_REPOSITÓRIO]
   ```

2. Navegue até o diretório do projeto:
   ```
   cd past-verbs-study-site/my-app
   ```

3. Instale as dependências:
   ```
   npm install
   ```
   ou
   ```
   pnpm install
   ```

4. Inicie o servidor de desenvolvimento:
   ```
   npm run dev
   ```
   ou
   ```
   pnpm run dev
   ```

5. Acesse o aplicativo em seu navegador:
   ```
   http://localhost:5173
   ```

## Construção para Produção

Para gerar uma versão de produção otimizada:

```
npm run build
```
ou
```
pnpm run build
```

Os arquivos de produção serão gerados na pasta `dist`.

## Personalização e Expansão

### Adicionando Novos Verbos

Para adicionar novos verbos à lista, edite o arquivo `src/data/verbList.js` seguindo o formato existente:

```javascript
{
  base: "novo_verbo",
  past: "forma_passado",
  participle: "particípio_passado",
  meaning: "significado",
  example: "Exemplo de uso em uma frase."
}
```

### Adicionando Novas Perguntas ao Quiz

Para adicionar novas perguntas ao quiz, edite o arquivo `src/data/quizData.js` seguindo o formato existente:

```javascript
{
  q: "Pergunta com __________ (verbo) no espaço.",
  a: "resposta_correta",
  explanation: "Explicação da resposta."
}
```

### Adicionando Novas Histórias

Para adicionar novas histórias, edite o arquivo `src/data/storyData.js` seguindo o formato existente:

```javascript
{
  title: "Título da História",
  content: `Texto com <span class="highlight-verb">verbos destacados</span>.`,
  explanation: "Explicação sobre os verbos usados."
}
```

## Manutenção

### Atualizando Dependências

Para atualizar as dependências do projeto:

```
npm update
```
ou
```
pnpm update
```

### Solução de Problemas Comuns

1. **Problema de renderização**: Verifique se todos os componentes estão importados corretamente.
2. **Dados não aparecem**: Verifique se os arquivos de dados estão formatados corretamente.
3. **Problemas de localStorage**: Limpe o localStorage do navegador e tente novamente.

## Contribuição

Para contribuir com o projeto:

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Faça commit das suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Faça push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.

## Contato

Para dúvidas ou sugestões, entre em contato através de [seu-email@exemplo.com].

---

Documentação criada em: Junho de 2025
