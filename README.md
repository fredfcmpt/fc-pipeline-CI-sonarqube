# Integração Contínua com GitHub Actions e SonarQube

Aplicação Node.js simples usada para validar uma pipeline de CI com testes unitários em Jest e análise de qualidade no SonarQube.

## Estrutura

```text
├── .github/
│   └── workflows/
│       └── ci.yaml
├── Analise/
├── src/
├── tests/
├── sonar-project.properties
└── README.md
```

## Como executar localmente

```bash
npm install
npm test
npm start
```

## Configuração obrigatória no GitHub

1. Cadastre os secrets do repositório:
   - `SONAR_TOKEN`
   - `SONAR_HOST_URL`
2. Abra um Pull Request contra a branch `main`.
3. Configure a proteção da branch `main` em `Settings > Branches > Branch protection rules`.
4. Ative `Require status checks to pass before merging`.
5. Marque os checks `tests` e `sonarqube` como obrigatórios.

## Entrega

O desafio deve ser entregue com o Pull Request aberto, sem merge, para que o avaliador veja os checks verdes e marcados como `Required`.
