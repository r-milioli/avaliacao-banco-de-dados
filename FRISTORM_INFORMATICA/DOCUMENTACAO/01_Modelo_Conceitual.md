# MODELO CONCEITUAL - FRISTORM INFORMÁTICA

## 📋 Descrição Geral

O Modelo Conceitual representa a visão de alto nível do sistema de banco de dados da **Fristorm Informática**, 
identificando as entidades principais, seus atributos e os relacionamentos entre elas.

## 🏗️ Entidades Identificadas

### 1. **ESTOQUE**
**Descrição**: Representa os locais de armazenamento de produtos da empresa.

**Atributos**:
- `codEstoque` (Chave Primária): Identificador único do estoque
- `qdtProduto`: Quantidade de produtos disponível no estoque

**Justificativa**: Necessário para controle de inventário e localização de produtos.

### 2. **PRODUTO**
**Descrição**: Representa os produtos comercializados pela empresa.

**Atributos**:
- `codProduto` (Chave Primária): Identificador único do produto
- `nomeProduto`: Nome/descrição do produto

**Justificativa**: Entidade central do sistema, representando o catálogo de produtos.

### 3. **FORNECEDOR**
**Descrição**: Representa as empresas que fornecem produtos para a Fristorm.

**Atributos**:
- `codFornecedor` (Chave Primária): Identificador único do fornecedor
- `nomeFornecedor`: Nome da empresa fornecedora

**Justificativa**: Essencial para controle de supply chain e relacionamento com parceiros.

### 4. **CLIENTE**
**Descrição**: Representa os clientes que adquirem produtos da empresa.

**Atributos**:
- `codCliente` (Chave Primária): Identificador único do cliente
- `qdtCompra`: Quantidade de produtos adquiridos pelo cliente

**Justificativa**: Fundamental para gestão de vendas e relacionamento com clientes.

## 🔗 Relacionamentos

### 1. **ESTOQUE ↔ PRODUTO** (Relacionamento: "estoque")
- **Tipo**: N:N (Muitos para Muitos)
- **Cardinalidade**: (0,n) - (0,n)
- **Descrição**: Um produto pode estar em múltiplos estoques, e um estoque pode conter múltiplos produtos
- **Justificativa**: Permite flexibilidade na distribuição de produtos entre diferentes locais

### 2. **PRODUTO ↔ FORNECEDOR** (Relacionamento: "fornece")
- **Tipo**: N:N (Muitos para Muitos)
- **Cardinalidade**: (1,n) - (1,n)
- **Descrição**: Um produto pode ser fornecido por múltiplos fornecedores, e um fornecedor pode fornecer múltiplos produtos
- **Justificativa**: Permite diversificação de fornecedores e competitividade de preços

### 3. **PRODUTO ↔ CLIENTE** (Relacionamento: "adquire")
- **Tipo**: N:N (Muitos para Muitos)
- **Cardinalidade**: (1,n) - (0,n)
- **Descrição**: Um produto pode ser adquirido por múltiplos clientes, e um cliente pode adquirir múltiplos produtos
- **Justificativa**: Permite análise de vendas e comportamento do cliente

## 🎯 Escolhas de Modelagem

### **Decisões Tomadas**:

1. **Número de Entidades**: Optou-se por 4 entidades principais para manter o modelo focado e gerenciável
2. **Atributos Mínimos**: Incluídos apenas os atributos essenciais para identificação e descrição básica
3. **Relacionamentos N:N**: Todos os relacionamentos são muitos-para-muitos para máxima flexibilidade
4. **Cardinalidades**: Definidas com base nas regras de negócio reais da empresa

### **Alternativas Consideradas**:

1. **Mais Entidades**: Poderiam ser incluídas entidades como "Categoria", "Pedido", "Funcionário"
2. **Atributos Adicionais**: Poderiam ser incluídos preços, datas, endereços, etc.
3. **Relacionamentos 1:N**: Poderiam ser considerados relacionamentos mais restritivos

### **Justificativa das Escolhas**:

- **Simplicidade**: Modelo fácil de entender e implementar
- **Flexibilidade**: Relacionamentos N:N permitem máxima adaptabilidade
- **Escalabilidade**: Estrutura permite expansão futura
- **Foco**: Concentra-se nas entidades mais importantes para o negócio

## 📊 Diagrama ER Conceitual

O diagrama ER conceitual está disponível em: `../DIAGRAMAS/modelo_conceitual.png`

## 🔄 Próximos Passos

Este modelo conceitual servirá como base para:
1. Desenvolvimento do Modelo Lógico
2. Definição das tabelas e chaves
3. Implementação do Modelo Físico no MySQL

---
*Documentação do Modelo Conceitual - Fristorm Informática*