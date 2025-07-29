# FRISTORM INFORMÁTICA
## Sistema de Gestão de Estoque e Vendas

### 📁 Estrutura do Projeto

```
FRISTORM_INFORMATICA/
├── README.md                           # Este arquivo
├── DOCUMENTACAO/
│   ├── 01_Modelo_Conceitual.md        # Documentação do Modelo Conceitual
│   ├── 02_Modelo_Logico.md            # Documentação do Modelo Lógico
│   └── 03_Modelo_Fisico.md            # Documentação do Modelo Físico
├── DIAGRAMAS/
│   ├── modelo_conceitual.png          # Diagrama ER Conceitual
│   ├── modelo_logico.png              # Diagrama ER Lógico
│   └── modelo_fisico.png              # Diagrama ER Físico
├── BANCO_DADOS/
│   └── banco_dados_fristorm.sql       # Script SQL completo
└── RELATORIO_FINAL.md                 # Relatório consolidado
```

### 🎯 Objetivo do Projeto

Desenvolvimento de um sistema de banco de dados MySQL para a **Fristorm Informática**, 
atendendo às necessidades de gestão de produtos, estoque, fornecedores e clientes.

### 📋 Componentes do Sistema

1. **Estoque**: Controle de quantidade de produtos
2. **Produto**: Cadastro de produtos da empresa
3. **Fornecedor**: Gestão de fornecedores
4. **Cliente**: Cadastro de clientes e suas compras

### 🔗 Relacionamentos

- **Produto ↔ Estoque**: Relacionamento N:N (produtos podem estar em múltiplos estoques)
- **Produto ↔ Fornecedor**: Relacionamento N:N (produtos podem ter múltiplos fornecedores)
- **Produto ↔ Cliente**: Relacionamento N:N (clientes podem comprar múltiplos produtos)

### 📊 Tecnologias Utilizadas

- **Modelagem**: Diagramas ER (Entidade-Relacionamento)
- **SGBD**: MySQL
- **Documentação**: Markdown

### 🚀 Como Executar

1. Abra o arquivo `BANCO_DADOS/banco_dados_fristorm.sql`
2. Execute o script no MySQL Workbench ou pgAdmin
3. O banco será criado automaticamente com todos os dados

### 📖 Documentação

- **Modelo Conceitual**: `DOCUMENTACAO/01_Modelo_Conceitual.md`
- **Modelo Lógico**: `DOCUMENTACAO/02_Modelo_Logico.md`
- **Modelo Físico**: `DOCUMENTACAO/03_Modelo_Fisico.md`
- **Relatório Final**: `RELATORIO_FINAL.md`

---
*Desenvolvido para avaliação de banco de dados - Fristorm Informática*