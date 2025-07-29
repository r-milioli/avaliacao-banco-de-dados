# ENTREGA FINAL - PARTE 2
## Consultas e Operações Avançadas em SQL
### FRISTORM INFORMÁTICA

---

## 📋 ORIENTAÇÕES PARA ENTREGA

### **Formato de Entrega:**
- **Arquivo PDF** com todas as instruções executáveis
- **Documento .pdf ou .docx** contendo:
  - Explicação resumida de cada grupo de consultas
  - **Prints das execuções** das queries no MySQL

---

## 🎯 EXPLICAÇÃO RESUMIDA DE CADA GRUPO DE CONSULTAS

### **1. CONSULTAS COM SELECT E WHERE (2,0 pts)**
**Objetivo**: Demonstrar consultas básicas com filtros simples.
- **Consulta 1.1**: Identifica produtos que estão em estoques com quantidade maior que 100
- **Consulta 1.2**: Lista fornecedores que fornecem produtos específicos (códigos 1, 2, 3)

**Aplicação Prática**: Útil para relatórios de estoque e análise de fornecedores.

---

### **2. CONSULTAS COM GROUP BY E ORDER BY (2,0 pts)**
**Objetivo**: Demonstrar agrupamento e ordenação de dados.
- **Consulta 2.1**: Conta quantos produtos cada fornecedor oferece, ordenado por quantidade
- **Consulta 2.2**: Calcula a média de compras por cliente, ordenado por valor

**Aplicação Prática**: Análise de performance de fornecedores e comportamento de clientes.

---

### **3. CONSULTAS COM OPERADORES ARITMÉTICOS (3,0 pts)**
**Objetivo**: Demonstrar cálculos matemáticos em consultas.
- **Consulta 3.1**: Calcula estoque disponível (80%) e reserva (20%) para cada produto
- **Consulta 3.2**: Calcula valores com desconto de 10% nas compras

**Aplicação Prática**: Gestão de estoque e cálculo de preços com descontos.

---

### **4. CONSULTAS COM OPERADORES DE COMPARAÇÃO (2,0 pts)**
**Objetivo**: Demonstrar diferentes tipos de comparações.
- **Consulta 4.1**: Produtos com estoque exato de 150 unidades
- **Consulta 4.2**: Clientes que não compraram exatamente 5 itens
- **Consulta 4.3**: Fornecedores com mais de 2 produtos

**Aplicação Prática**: Filtros específicos para relatórios e análises pontuais.

---

### **5. CONSULTAS COM OPERADORES LÓGICOS AND/OR (3,0 pts)**
**Objetivo**: Demonstrar combinação de condições.
- **Consulta 5.1**: Produtos em estoque específico E com quantidade > 100
- **Consulta 5.2**: Clientes que compraram 3 OU 8 itens
- **Consulta 5.3**: Fornecedor específico E produtos específicos

**Aplicação Prática**: Consultas complexas para análise de dados específicos.

---

### **6. CONSULTAS COM OPERADOR NOT (3,0 pts)**
**Objetivo**: Demonstrar exclusão de dados.
- **Consulta 6.1**: Produtos NÃO fornecidos por fornecedor específico
- **Consulta 6.2**: Clientes que NÃO compraram produtos específicos

**Aplicação Prática**: Identificação de lacunas no negócio e oportunidades.

---

### **7. CONSULTAS COM OPERADORES AUXILIARES (3,0 pts)**
**Objetivo**: Demonstrar operadores especiais do SQL.
- **Consulta 7.1**: Produtos com nome contendo 'Dell' (LIKE)
- **Consulta 7.2**: Estoques com quantidade entre 100 e 200 (BETWEEN)
- **Consulta 7.3**: Fornecedores específicos (IN)

**Aplicação Prática**: Buscas flexíveis e filtros por faixas de valores.

---

### **8. CONSULTAS COM FUNÇÕES DE AGREGAÇÃO (2,0 pts)**
**Objetivo**: Demonstrar cálculos estatísticos.
- **Consulta 8.1**: Soma total de produtos em estoque (SUM)
- **Consulta 8.2**: Média de compras por cliente (AVG)
- **Consulta 8.3**: Contagem de produtos por fornecedor (COUNT)

**Aplicação Prática**: Relatórios gerenciais e análises estatísticas.

---

### **9. CONSULTAS COM FUNÇÕES DE DATAS (3,0 pts)**
**Objetivo**: Demonstrar manipulação de datas.
- **Consulta 9.1**: Data atual e componentes (ano, mês, dia)
- **Consulta 9.2**: Cálculos de datas futuras e passadas

**Aplicação Prática**: Controle temporal e planejamento de atividades.

---

### **10. SUB-CONSULTAS COM AGREGAÇÃO (5,0 pts)**
**Objetivo**: Demonstrar consultas aninhadas complexas.
- **Consulta 10.1**: Produtos com estoque acima da média
- **Consulta 10.2**: Fornecedores com mais produtos que a média
- **Consulta 10.3**: Clientes com compras acima da média

**Aplicação Prática**: Análises comparativas e identificação de outliers.

---

### **11. CONSULTAS COM JOIN (6,0 pts)**
**Objetivo**: Demonstrar relacionamento entre tabelas.
- **Consulta 11.1**: Produtos e seus fornecedores
- **Consulta 11.2**: Clientes e produtos adquiridos
- **Consulta 11.3**: Produtos e estoques

**Aplicação Prática**: Relatórios integrados e análise de relacionamentos.

---

### **12. TIPOS DE JOIN: INNER, LEFT, RIGHT (6,0 pts)**
**Objetivo**: Demonstrar diferentes tipos de junção.
- **Consulta 12.1**: INNER JOIN - apenas registros que existem em ambas as tabelas
- **Consulta 12.2**: LEFT JOIN - todos os produtos, mesmo sem fornecedor
- **Consulta 12.3**: RIGHT JOIN - todos os fornecedores, mesmo sem produtos
- **Consulta 12.4**: Múltiplos INNER JOINs - relacionamento complexo

**Aplicação Prática**: Análises completas incluindo dados ausentes.

---

## 📸 INSTRUÇÕES PARA PRINTS DAS EXECUÇÕES

### **Passo a Passo para Capturar os Prints:**

#### **1. Preparação do Ambiente:**
1. Abra o **pgAdmin** ou **MySQL Workbench**
2. Conecte ao banco de dados `fristorm_informatica`
3. Execute o script SQL da pasta `BANCO_DADOS_FOLDER`

#### **2. Para Cada Grupo de Consultas:**

**Grupo 1 - SELECT e WHERE:**
- Execute a Consulta 1.1
- Capture o print da tela mostrando:
  - Query executada
  - Resultados retornados
- Execute a Consulta 1.2
- Capture outro print
- **Repita para todos os 12 grupos**

#### **3. Formato dos Prints:**
- **Tamanho**: Captura de tela completa ou da janela de resultados
- **Visibilidade**: Query e resultados devem estar claros
- **Organização**: Um print por consulta ou grupo de consultas similares

#### **4. Estrutura Sugerida para o Documento:**
```
1. GRUPO 1 - SELECT E WHERE
   - Explicação do grupo
   - Print da Consulta 1.1
   - Print da Consulta 1.2

2. GRUPO 2 - GROUP BY E ORDER BY
   - Explicação do grupo
   - Print da Consulta 2.1
   - Print da Consulta 2.2

[... continua para todos os 12 grupos]
```

---

## 📊 RESUMO DOS RESULTADOS ESPERADOS

### **Resultados Típicos das Consultas:**

#### **Grupo 1 - SELECT e WHERE:**
- **Consulta 1.1**: Deve retornar produtos como "Notebook Dell Inspiron", "Mouse Wireless Logitech"
- **Consulta 1.2**: Deve retornar fornecedores como "Dell Brasil", "Logitech"

#### **Grupo 2 - GROUP BY:**
- **Consulta 2.1**: Deve mostrar cada fornecedor com sua contagem de produtos
- **Consulta 2.2**: Deve mostrar cada cliente com sua média de compras

#### **Grupo 3 - Operadores Aritméticos:**
- **Consulta 3.1**: Deve mostrar estoque disponível (80%) e reserva (20%)
- **Consulta 3.2**: Deve mostrar valores originais e com desconto

#### **Grupo 8 - Funções de Agregação:**
- **Consulta 8.1**: Deve retornar um valor total (ex: 1645)
- **Consulta 8.2**: Deve retornar uma média (ex: 4.5)
- **Consulta 8.3**: Deve mostrar contagem por fornecedor

---

## ✅ CHECKLIST PARA ENTREGA

### **Documento Final Deve Conter:**

- [ ] **Capa** com identificação do projeto
- [ ] **Introdução** explicando o objetivo da Parte 2
- [ ] **12 seções** (uma para cada grupo de consultas)
- [ ] **Explicação** de cada grupo de consultas
- [ ] **Prints** de todas as execuções
- [ ] **Conclusão** sobre os resultados obtidos
- [ ] **Anexos** com o código SQL completo

### **Formato Final:**
- **Arquivo**: PDF ou DOCX
- **Páginas**: Aproximadamente 15-20 páginas
- **Imagens**: Prints de alta qualidade
- **Texto**: Explicações claras e objetivas

---

## 🎯 CRITÉRIOS DE AVALIAÇÃO ATENDIDOS

| Critério | Consultas | Pontos | Status |
|----------|-----------|--------|--------|
| 1. SELECT e WHERE | 2 consultas | 2,0 | ✅ |
| 2. GROUP BY e ORDER BY | 2 consultas | 2,0 | ✅ |
| 3. Operadores aritméticos | 2 consultas | 3,0 | ✅ |
| 4. Operadores de comparação | 3 consultas | 2,0 | ✅ |
| 5. Operadores lógicos (AND, OR) | 3 consultas | 3,0 | ✅ |
| 6. Operadores lógicos e NOT | 2 consultas | 3,0 | ✅ |
| 7. Operadores auxiliares | 3 consultas | 3,0 | ✅ |
| 8. Funções de agregação | 3 consultas | 2,0 | ✅ |
| 9. Funções de datas | 2 consultas | 3,0 | ✅ |
| 10. Sub-consultas | 3 consultas | 5,0 | ✅ |
| 11. JOIN e visualização | 3 consultas | 6,0 | ✅ |
| 12. Tipos de JOIN | 4 consultas | 6,0 | ✅ |
| **TOTAL** | **33 consultas** | **40,0** | **✅** |

---

## 🚀 PRÓXIMOS PASSOS

1. **Execute todas as consultas** no pgAdmin
2. **Capture os prints** de cada execução
3. **Organize o documento** seguindo a estrutura sugerida
4. **Revise e formate** o documento final
5. **Converta para PDF** para entrega

---

*Documento de Orientação para Entrega - Parte 2 - Fristorm Informática*