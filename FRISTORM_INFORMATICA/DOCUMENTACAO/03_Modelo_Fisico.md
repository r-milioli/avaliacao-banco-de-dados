# MODELO FÍSICO - FRISTORM INFORMÁTICA

## 📋 Descrição Geral

O Modelo Físico representa a implementação concreta do banco de dados no SGBD MySQL, 
incluindo a criação das tabelas, inserção de dados e verificação da integridade referencial.

## 🗄️ Implementação no MySQL

### **Banco de Dados Criado**
```sql
CREATE DATABASE IF NOT EXISTS fristorm_informatica;
USE fristorm_informatica;
```

## 🏗️ Estrutura das Tabelas Implementadas

### **Tabelas Principais**

#### 1. **TABELA: Estoque**
```sql
CREATE TABLE Estoque (
    codEstoque INT PRIMARY KEY,
    qdtProduto INT NOT NULL
);
```
**Dados Inseridos**: 10 registros com quantidades variadas de produtos

#### 2. **TABELA: Produto**
```sql
CREATE TABLE Produto (
    codProduto INT PRIMARY KEY,
    nomeProduto VARCHAR(100) NOT NULL
);
```
**Dados Inseridos**: 12 produtos de informática (notebooks, periféricos, componentes)

#### 3. **TABELA: Fornecedor**
```sql
CREATE TABLE Fornecedor (
    codFornecedor INT PRIMARY KEY,
    nomeFornecedor VARCHAR(100) NOT NULL
);
```
**Dados Inseridos**: 12 fornecedores conhecidos do mercado de TI

#### 4. **TABELA: Cliente**
```sql
CREATE TABLE Cliente (
    codCliente INT PRIMARY KEY,
    qdtCompra INT NOT NULL
);
```
**Dados Inseridos**: 12 clientes com diferentes quantidades de compras

### **Tabelas de Junção**

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
**Dados Inseridos**: 36 registros representando produtos em diferentes estoques

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
**Dados Inseridos**: 36 registros representando compras de clientes

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
**Dados Inseridos**: 36 registros representando fornecedores de produtos

## 📊 Dados de Exemplo Inseridos

### **Produtos Cadastrados**:
1. Notebook Dell Inspiron
2. Mouse Wireless Logitech
3. Teclado Mecânico RGB
4. Monitor LG 24"
5. Impressora HP LaserJet
6. Webcam HD 1080p
7. Headset Gamer
8. SSD 500GB Kingston
9. Memória RAM 8GB
10. Fonte 500W Corsair
11. Placa de Vídeo GTX 1660
12. Processador Intel i5

### **Fornecedores Cadastrados**:
1. Dell Brasil
2. Logitech
3. LG Electronics
4. HP Brasil
5. Kingston Technology
6. Corsair
7. NVIDIA
8. Intel Brasil
9. Samsung
10. Western Digital
11. ASUS
12. MSI

## 🔒 Integridade Referencial

### **Constraints Implementadas**:

1. **PRIMARY KEY**: Garantem unicidade dos registros
2. **FOREIGN KEY**: Mantêm integridade referencial entre tabelas
3. **NOT NULL**: Campos obrigatórios não podem ser nulos

### **Verificação de Integridade**:
```sql
-- Contagem de registros em cada tabela
SELECT 'Estoque' as Tabela, COUNT(*) as Total_Registros FROM Estoque
UNION ALL
SELECT 'Produto', COUNT(*) FROM Produto
UNION ALL
SELECT 'Fornecedor', COUNT(*) FROM Fornecedor
UNION ALL
SELECT 'Cliente', COUNT(*) FROM Cliente
UNION ALL
SELECT 'estoque (junção)', COUNT(*) FROM estoque
UNION ALL
SELECT 'adquire (junção)', COUNT(*) FROM adquire
UNION ALL
SELECT 'fornece (junção)', COUNT(*) FROM fornece;
```

## 📈 Estatísticas do Banco

| Tabela | Total de Registros |
|--------|-------------------|
| Estoque | 10 |
| Produto | 12 |
| Fornecedor | 12 |
| Cliente | 12 |
| estoque (junção) | 36 |
| adquire (junção) | 36 |
| fornece (junção) | 36 |

## 🎯 Características da Implementação

### **Aspectos Técnicos**:

1. **SGBD**: MySQL
2. **Encoding**: UTF-8 (suporte a caracteres especiais)
3. **Engine**: InnoDB (suporte a transações e foreign keys)
4. **Índices**: Automáticos nas chaves primárias

### **Qualidade dos Dados**:

1. **Realismo**: Dados representam cenário real de empresa de informática
2. **Variedade**: Produtos, fornecedores e clientes diversos
3. **Consistência**: Relacionamentos lógicos entre as entidades
4. **Quantidade**: Mais de 10 registros por tabela (requisito atendido)

## 🚀 Como Executar

### **Passos para Implementação**:

1. **Abrir MySQL Workbench ou pgAdmin**
2. **Executar o script completo**: `banco_dados_fristorm.sql`
3. **Verificar criação**: O banco será criado automaticamente
4. **Validar dados**: Executar consultas de verificação

### **Comandos de Verificação**:
```sql
-- Verificar se o banco foi criado
SHOW DATABASES;

-- Usar o banco
USE fristorm_informatica;

-- Verificar tabelas criadas
SHOW TABLES;

-- Verificar estrutura das tabelas
DESCRIBE Estoque;
DESCRIBE Produto;
DESCRIBE Fornecedor;
DESCRIBE Cliente;
```

## 📊 Diagrama ER Físico

O diagrama ER físico está disponível em: `../DIAGRAMAS/modelo_fisico.png`

## ✅ Validação dos Requisitos

### **Requisitos Atendidos**:

- ✅ **Implementação no MySQL**: Script SQL completo e funcional
- ✅ **10+ registros por tabela**: Todas as tabelas atendem ao requisito
- ✅ **Integridade referencial**: Foreign keys implementadas
- ✅ **Arquivo SQL**: Script completo para criação e inserção

---
*Documentação do Modelo Físico - Fristorm Informática*