git # FRISTORM INFORMÁTICA
## Sistema de Gestão de Estoque e Vendas

---

## 📋 **DESCRIÇÃO DO PROJETO**

Este projeto foi desenvolvido para a disciplina de **Banco de Dados** como parte da avaliação acadêmica. O objetivo é criar um sistema completo de banco de dados para a empresa fictícia **Fristorm Informática**, especializada em produtos de informática.

### **🎯 Objetivos do Projeto:**
- Desenvolver um banco de dados relacional completo
- Aplicar conceitos de modelagem de dados (Conceitual, Lógico e Físico)
- Implementar consultas SQL avançadas
- Demonstrar domínio em operações de banco de dados

---

## 📚 **ESTRUTURA DO PROJETO**

```
FRISTORM_INFORMATICA/
├── 📁 DOCUMENTACAO/
│   ├── 01_Modelo_Conceitual.md
│   ├── 02_Modelo_Logico.md
│   └── 03_Modelo_Fisico.md
├── 📁 BANCO_DADOS_FOLDER/
│   ├── banco_dados_fristorm.sql
│   └── parte2_consultas_completas.sql
├── 📁 DIAGRAMAS/
│   ├── modelo_conceitual.png
│   ├── modelo_logico.png
│   └── modelo_fisico.png
├── README.md
├── RELATORIO_FINAL.md
├── PARTE_2_CONSULTAS_SQL.md
└── ENTREGA_FINAL_PARTE2.md
```

---

## 🎯 **PARTE 1: MODELAGEM DE BANCO DE DADOS**

### **1.1 Modelo Conceitual**
- **Objetivo**: Criar diagrama ER com pelo menos 4 entidades
- **Requisitos**:
  - Entidades com atributos descritivos
  - Relacionamentos bem definidos
  - Cardinalidades corretas (1:N, N:N, 0,n, 1,n)
  - Documentação explicativa

### **1.2 Modelo Lógico**
- **Objetivo**: Transformar modelo conceitual em estrutura relacional
- **Requisitos**:
  - Transformação de entidades em tabelas
  - Definição de chaves primárias e estrangeiras
  - Resolução de relacionamentos N:N
  - Apresentação clara e organizada

### **1.3 Modelo Físico**
- **Objetivo**: Implementação direta no MySQL
- **Requisitos**:
  - Criação do banco de dados
  - Definição de todas as tabelas
  - Pelo menos 10 registros por tabela
  - Respeito à integridade referencial
  - Arquivo SQL executável

---

## 🔍 **PARTE 2: CONSULTAS E OPERAÇÕES AVANÇADAS**

### **Objetivo**: Aplicar conhecimentos de SQL sobre banco modelado e populado

### **📊 Critérios de Avaliação (40 pontos):**

| Critério | Descrição | Consultas | Pontos |
|----------|-----------|-----------|--------|
| 1 | SELECT e WHERE | 2 consultas | 2,0 |
| 2 | GROUP BY e ORDER BY | 2 consultas | 2,0 |
| 3 | Operadores aritméticos | 2 consultas | 3,0 |
| 4 | Operadores de comparação | 3 consultas | 2,0 |
| 5 | Operadores lógicos (AND, OR) | 3 consultas | 3,0 |
| 6 | Operadores lógicos e NOT | 2 consultas | 3,0 |
| 7 | Operadores auxiliares | 3 consultas | 3,0 |
| 8 | Funções de agregação | 3 consultas | 2,0 |
| 9 | Funções de datas | 2 consultas | 3,0 |
| 10 | Sub-consultas | 3 consultas | 5,0 |
| 11 | JOIN e visualização | 3 consultas | 6,0 |
| 12 | Tipos de JOIN (INNER, LEFT, RIGHT) | 4 consultas | 6,0 |
| **TOTAL** | **33 consultas** | **40,0** |

---

## 🗄️ **ESTRUTURA DO BANCO DE DADOS**

### **Entidades Principais:**
- **Produto**: Produtos de informática
- **Estoque**: Controle de quantidade em estoque
- **Fornecedor**: Empresas fornecedoras
- **Cliente**: Clientes da empresa

### **Tabelas de Relacionamento:**
- **estoque**: Relacionamento Produto x Estoque (N:N)
- **adquire**: Relacionamento Cliente x Produto (N:N)
- **fornece**: Relacionamento Fornecedor x Produto (N:N)

### **Dados Populados:**
- **10 registros** na tabela Estoque
- **12 registros** nas tabelas Produto, Fornecedor e Cliente
- **36 registros** em cada tabela de relacionamento
- **Total**: 118 registros distribuídos em 7 tabelas

---

## 🚀 **COMO EXECUTAR O PROJETO**

### **Pré-requisitos:**
- MySQL Server ou pgAdmin
- Conhecimento básico de SQL

### **Passo a Passo:**

#### **1. Preparação do Ambiente:**
```bash
# 1. Abra o pgAdmin ou MySQL Workbench
# 2. Conecte ao servidor de banco de dados
# 3. Certifique-se de ter permissões de criação de banco
```

#### **2. Execução do Banco de Dados:**
```sql
-- Execute o arquivo: BANCO_DADOS_FOLDER/banco_dados_fristorm.sql
-- Este script irá:
-- - Criar o banco 'fristorm_informatica'
-- - Criar todas as tabelas
-- - Inserir todos os dados de exemplo
```

#### **3. Execução das Consultas:**
```sql
-- Execute o arquivo: BANCO_DADOS_FOLDER/parte2_consultas_completas.sql
-- Este arquivo contém todas as 33 consultas organizadas por critérios
```

---

## 📋 **ENTREGA DO PROJETO**

### **Parte 1 - Modelagem:**
- Documentação completa dos 3 modelos
- Diagramas ER em formato PNG
- Arquivo SQL do banco de dados
- Relatório final explicativo

### **Parte 2 - Consultas:**
- **Formato**: PDF ou DOCX
- **Conteúdo**:
  - Explicação resumida de cada grupo de consultas
  - Prints das execuções no MySQL
  - Documentação completa das 33 consultas

### **Estrutura da Entrega:**
```
ENTREGA_FINAL/
├── 📄 Relatório_Parte1.pdf
├── 📄 Relatório_Parte2.pdf
├── 📁 Diagramas/
├── 📁 Banco_Dados/
└── 📁 Consultas_SQL/
```

---

## 🛠️ **TECNOLOGIAS UTILIZADAS**

- **Sistema Gerenciador**: MySQL
- **Ferramenta de Desenvolvimento**: pgAdmin
- **Linguagem**: SQL (DDL e DML)
- **Documentação**: Markdown
- **Diagramas**: Ferramentas de modelagem ER

---

## 📊 **RESULTADOS ESPERADOS**

### **Parte 1:**
- ✅ Modelo conceitual com 4+ entidades
- ✅ Modelo lógico bem estruturado
- ✅ Banco de dados funcional com dados
- ✅ Documentação completa

### **Parte 2:**
- ✅ 33 consultas SQL executáveis
- ✅ Cobertura de todos os critérios
- ✅ Resultados consistentes
- ✅ Documentação com prints

---

## 🎯 **CRITÉRIOS DE SUCESSO**

### **Funcionalidade:**
- Banco de dados operacional
- Consultas executando sem erros
- Dados consistentes e realistas

### **Qualidade:**
- Código SQL bem estruturado
- Documentação clara e completa
- Diagramas profissionais

### **Completude:**
- Todos os requisitos atendidos
- 40 pontos em consultas SQL
- Entrega no formato solicitado
---

## 📝 **NOTAS IMPORTANTES**

1. **Execute sempre** o banco de dados antes das consultas
2. **Capture prints** de todas as execuções para a entrega
3. **Organize** a documentação conforme estrutura sugerida
4. **Teste** todas as consultas antes da entrega final

---

*Projeto desenvolvido para avaliação acadêmica - Fristorm Informática*
*Data: 2025*
*Disciplina: Banco de Dados*