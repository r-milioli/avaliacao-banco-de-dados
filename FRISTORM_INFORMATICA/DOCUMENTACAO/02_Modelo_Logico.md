# MODELO LÓGICO - FRISTORM INFORMÁTICA

## 📋 Descrição Geral

O Modelo Lógico representa a transformação do Modelo Conceitual em estruturas de dados relacionais, 
definindo tabelas, colunas, chaves primárias e estrangeiras para implementação no SGBD.

## 🔄 Transformação do Modelo Conceitual

### **Princípio de Transformação**:
- **Entidades** → **Tabelas**
- **Atributos** → **Colunas**
- **Relacionamentos N:N** → **Tabelas de Junção**
- **Chaves Primárias** → **PK (Primary Key)**
- **Relacionamentos** → **FK (Foreign Key)**

## 🏗️ Estrutura das Tabelas

### **Tabelas Principais**

#### 1. **TABELA: Estoque**
```sql
CREATE TABLE Estoque (
    codEstoque INT PRIMARY KEY,
    qdtProduto INT NOT NULL
);
```
**Transformação**: Entidade ESTOQUE → Tabela Estoque
- `codEstoque`: Chave primária (PK)
- `qdtProduto`: Atributo descritivo

#### 2. **TABELA: Produto**
```sql
CREATE TABLE Produto (
    codProduto INT PRIMARY KEY,
    nomeProduto VARCHAR(100) NOT NULL
);
```
**Transformação**: Entidade PRODUTO → Tabela Produto
- `codProduto`: Chave primária (PK)
- `nomeProduto`: Atributo descritivo

#### 3. **TABELA: Fornecedor**
```sql
CREATE TABLE Fornecedor (
    codFornecedor INT PRIMARY KEY,
    nomeFornecedor VARCHAR(100) NOT NULL
);
```
**Transformação**: Entidade FORNECEDOR → Tabela Fornecedor
- `codFornecedor`: Chave primária (PK)
- `nomeFornecedor`: Atributo descritivo

#### 4. **TABELA: Cliente**
```sql
CREATE TABLE Cliente (
    codCliente INT PRIMARY KEY,
    qdtCompra INT NOT NULL
);
```
**Transformação**: Entidade CLIENTE → Tabela Cliente
- `codCliente`: Chave primária (PK)
- `qdtCompra`: Atributo descritivo

### **Tabelas de Junção (Resolução de N:N)**

#### 1. **TABELA: estoque**
```sql
CREATE TABLE estoque (
    codProduto INT,
    codEstoque INT,
    PRIMARY KEY (codProduto, codEstoque),
    FOREIGN KEY (codProduto) REFERENCES Produto(codProduto),
    FOREIGN KEY (codEstoque) REFERENCES Estoque(codEstoque)
);
```
**Transformação**: Relacionamento "estoque" (ESTOQUE ↔ PRODUTO) → Tabela estoque
- **Chave Composta**: (codProduto, codEstoque)
- **Foreign Keys**: Referenciam as tabelas principais

#### 2. **TABELA: adquire**
```sql
CREATE TABLE adquire (
    codCliente INT,
    codProduto INT,
    PRIMARY KEY (codCliente, codProduto),
    FOREIGN KEY (codCliente) REFERENCES Cliente(codCliente),
    FOREIGN KEY (codProduto) REFERENCES Produto(codProduto)
);
```
**Transformação**: Relacionamento "adquire" (PRODUTO ↔ CLIENTE) → Tabela adquire
- **Chave Composta**: (codCliente, codProduto)
- **Foreign Keys**: Referenciam as tabelas principais

#### 3. **TABELA: fornece**
```sql
CREATE TABLE fornece (
    codFornecedor INT,
    codProduto INT,
    PRIMARY KEY (codFornecedor, codProduto),
    FOREIGN KEY (codFornecedor) REFERENCES Fornecedor(codFornecedor),
    FOREIGN KEY (codProduto) REFERENCES Produto(codProduto)
);
```
**Transformação**: Relacionamento "fornece" (PRODUTO ↔ FORNECEDOR) → Tabela fornece
- **Chave Composta**: (codFornecedor, codProduto)
- **Foreign Keys**: Referenciam as tabelas principais

## 🔑 Definição de Chaves

### **Chaves Primárias (PK)**
- **Tabelas Principais**: Chaves simples (INT)
- **Tabelas de Junção**: Chaves compostas (combinação de FK)

### **Chaves Estrangeiras (FK)**
- **Tabela estoque**: `codProduto` → `Produto.codProduto`
- **Tabela estoque**: `codEstoque` → `Estoque.codEstoque`
- **Tabela adquire**: `codCliente` → `Cliente.codCliente`
- **Tabela adquire**: `codProduto` → `Produto.codProduto`
- **Tabela fornece**: `codFornecedor` → `Fornecedor.codFornecedor`
- **Tabela fornece**: `codProduto` → `Produto.codProduto`

## 📊 Mapeamento de Relacionamentos

### **Relacionamento N:N → Tabela de Junção**

| Relacionamento Conceitual | Tabela de Junção | Chaves Compostas |
|---------------------------|------------------|------------------|
| ESTOQUE ↔ PRODUTO | estoque | (codProduto, codEstoque) |
| PRODUTO ↔ CLIENTE | adquire | (codCliente, codProduto) |
| PRODUTO ↔ FORNECEDOR | fornece | (codFornecedor, codProduto) |

## 🎯 Decisões de Modelagem Lógica

### **Escolhas Realizadas**:

1. **Resolução de N:N**: Todos os relacionamentos N:N foram convertidos em tabelas de junção
2. **Chaves Compostas**: Utilizadas nas tabelas de junção para garantir unicidade
3. **Integridade Referencial**: Foreign Keys definidas para manter consistência
4. **Tipos de Dados**: VARCHAR para textos, INT para identificadores e quantidades

### **Benefícios da Estrutura**:

- **Normalização**: Estrutura normalizada (3NF)
- **Flexibilidade**: Permite relacionamentos complexos
- **Integridade**: Constraints garantem consistência dos dados
- **Performance**: Índices automáticos nas chaves primárias

## 📊 Diagrama ER Lógico

O diagrama ER lógico está disponível em: `../DIAGRAMAS/modelo_logico.png`

## 🔄 Próximos Passos

Este modelo lógico servirá como base para:
1. Implementação do Modelo Físico no MySQL
2. Criação das tabelas e constraints
3. Inserção de dados de teste

---
*Documentação do Modelo Lógico - Fristorm Informática*