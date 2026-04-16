# 🚀 Banco API Performance

## 📌 Introdução
Este repositório tem como objetivo realizar testes de performance em uma API bancária utilizando o K6 com JavaScript. A proposta é simular diferentes cenários de carga para avaliar a estabilidade, tempo de resposta e comportamento da aplicação sob estresse.

---

## 🛠️ Tecnologias utilizadas
- JavaScript
- K6 (ferramenta de teste de carga)
- GJSON - para extração de dados em respostas JSON. 
- Variáveis de ambiente para configuração dinâmica (ex: `BASE_URL`)

---

## 📂 Estrutura do repositório
```
.
├── config/             # Arquivo de configuração
├── fixtures/           # Dados mockados utilizados nos testes
├── helpers/            # Funções utilitárias
|── tests/              # Scripts de teste de performance
├── utils/              # Funções auxiliares e helpers
├└── README.md          # Documentação do projeto
```

---

## 🎯 Objetivo de cada grupo de arquivos

### 📁 tests/
Contém os cenários de teste escritos em JavaScript para execução no K6.

### 📁 fixtures/
Armazena dados estáticos utilizados durante os testes, como payloads e massas de dados.

### 📁 utils/
Funções auxiliares para reutilização de código, como autenticação, geração de dados e configurações.

### 📁 helpers/
Contém funções auxiliares (ex: geração de tokens, manipulação de datas, validação de resposta)

### 📁 Config/
Contém arquivos de configuração de varáveis de ambiente.


## ⚙️ Instalação

### 1. Clonar o repositório
```bash
git clone https://github.com/PinkFlowGirl/banco-api-performance.git
cd banco-api-performance
```

### 2. Instalar o K6


## ▶️ Execução do projeto

### 🔑 Definir variável de ambiente
O projeto utiliza a variável de ambiente `BASE_URL`, que deve ser definida antes da execução dos testes.

#### Exemplo (Linux/MacOS)
```bash
export BASE_URL=https://sua-api.com
```

#### Exemplo (Windows - Git Bash)
```bash
export BASE_URL=https://sua-api.com
```

#### Exemplo (Windows - CMD)
```bash
set BASE_URL=https://sua-api.com
```

---

### 🚀 Executar testes com K6
```bash
k6 run tests/seu-teste.js
```

---

### 📊 Execução com dashboard em tempo real + exportação de relatório

Para acompanhar os testes em tempo real no navegador e exportar o relatório em HTML:

#### Linux/MacOS / Git Bash
```bash
K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run tests/seu-teste.js
```

#### Windows (CMD)
```bash
set K6_WEB_DASHBOARD=true && set K6_WEB_DASHBOARD_EXPORT=html-report.html && k6 run tests/seu-teste.js
```

O relatório será gerado no arquivo `html-report.html`.

---

## 📈 Considerações finais
Este projeto pode ser expandido com novos cenários de teste, integração com pipelines CI/CD e monitoramento contínuo para garantir a qualidade da aplicação ao longo do tempo.

---

💡 Dica: mantenha seus testes organizados por tipo (carga, stress, soak) para facilitar manutenção e análise.
