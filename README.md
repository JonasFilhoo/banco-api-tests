# banco-api-tests

Este projeto tem como objetivo automatizar os testes da API REST disponível em [juliodelimas/banco-api](https://github.com/juliodelimas/banco-api). A automação contribui para que os endpoints da API se comportem conforme o esperado, utilizando dados controlados e validações programáticas.

## Objetivo

Verificar o correto funcionamento dos principais fluxos da API, como autenticação e transferências bancárias, por meio de testes automatizados que podem ser executados localmente ou integrados a pipelines de CI/CD.

## Stack Utilizada

- **Linguagem:** JavaScript (Node.js)  
- **Framework de testes:** [Mocha](https://mochajs.org/)  
- **Asserções:** [Chai](https://www.chaijs.com/)  
- **Requisições HTTP:** [Supertest](https://github.com/visionmedia/supertest)  
- **Relatórios HTML:** [Mochawesome](https://github.com/adamgruber/mochawesome)  
- **Variáveis de ambiente:** [dotenv](https://github.com/motdotla/dotenv)

## Estrutura de Diretórios

```
banco-api-tests/
├── fixtures/                # Dados de entrada para os testes
│   ├── postLogin.json
│   └── postTransferencias.json
├── helpers/                 # Funções auxiliares (ex: geração de token)
│   └── autenticacao.js
├── test/                    # Casos de teste
│   ├── login.test.js
│   └── transferencia.test.js
├── mochawesome-report/     # Relatórios gerados (após testes)
├── .env                     # Variáveis de ambiente (não versionado)
├── .gitignore               # Arquivos e pastas ignorados pelo Git
├── package.json             # Dependências e scripts
└── README.md                # Documentação do projeto
```

## Formato do Arquivo `.env`

Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```
BASE_URL=http://localhost:3000
```

> Substitua a URL acima conforme a porta e endereço utilizados pelo servidor da API.

## Comandos para Execução dos Testes

Instale as dependências do projeto:

```bash
npm install
```

Execute os testes automatizados:

```bash
npm test
```

Isso irá rodar os testes com o Mocha e gerar um relatório HTML completo via Mochawesome.

## Relatório de Testes

Após executar `npm test`, um relatório será gerado automaticamente em:

```
./mochawesome-report/mochawesome.html
```

Abra esse arquivo no navegador para visualizar os resultados detalhados.

## Documentação das Bibliotecas Utilizadas

- [Mocha](https://mochajs.org/)
- [Chai](https://www.chaijs.com/)
- [Supertest](https://github.com/visionmedia/supertest)
- [Mochawesome](https://github.com/adamgruber/mochawesome)
- [dotenv](https://github.com/motdotla/dotenv)

---

Este projeto foi criado com fins didáticos e pode ser expandido para validar outros endpoints da API.
