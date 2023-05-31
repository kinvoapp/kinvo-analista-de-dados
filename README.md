> ![Logo Kinvo](https://github.com/kinvoapp/kinvo-mobile-test/blob/master/logo.svg)


# Desafio técnico para candidatos à vaga de Analista de Dados.

## Desafio: Análise e visualização de dados de uma loja de varejo

## Descrição do problema:
Uma loja de varejo fictícia chamada "XYZ Corp." está contratando um analista de dados para ajudar a entender melhor o desempenho de suas vendas. 

A empresa possui um banco de dados relacional com informações sobre vendas, produtos e clientes. Eles desejam que você utilize a linguagem SQL para realizar análises e extrair insights valiosos para o negócio.

## Tarefas:

**Análise de vendas:** Explore os dados de vendas disponíveis no banco de dados e responda às seguintes perguntas utilizando consultas SQL:

1. Quais são os produtos mais vendidos em termos de quantidade?
2. Qual é o valor total das vendas para cada mês do último ano?
3. Quais são as categorias de produtos mais lucrativas?

**Análise de clientes:** Utilize as informações dos clientes para responder às seguintes perguntas:

1. Qual é o perfil demográfico médio dos clientes da loja?
2. Quais são os principais canais de comunicação preferidos pelos clientes?

**Visualizações de dados:** Com base nas análises realizadas, crie visualizações gráficas para comunicar os insights obtidos. Utilize ferramentas específicas de visualização de dados (por exemplo, Zoho analytics, Power BI). Justifique suas escolhas e explique os benefícios de cada visualização criada.

**Insights e recomendações:** Com base na análise dos dados e nas visualizações criadas, forneça insights significativos para a empresa. Por exemplo, você pode identificar um produto com baixo desempenho de vendas que pode ser descontinuado ou uma faixa etária específica de clientes que apresenta alto potencial de crescimento. Além disso, sugira recomendações acionáveis para melhorar o desempenho de vendas com base em suas descobertas.



## Entrega:
Prepare um relatório ou apresentação contendo suas análises, visualizações, insights e recomendações. 

Crie uma view que una as informações das 3 tabelas.

Certifique-se de que sua entrega seja clara, organizada e fácil de entender para uma audiência não técnica. inclua o SQL utilizado para realizar as consultas e criar as visualizações.



## Avaliação:
Sua entrega será avaliada com base na qualidade da análise de dados, eficácia das visualizações, relevância dos insights e recomendações, além da clareza e organização da apresentação.

Boa sorte e aproveite o desafio!


## Scripts SQL para criar as tabelas "vendas", "produtos" e "clientes":

```
-- Criação da tabela "vendas"
CREATE TABLE vendas (
  id INT PRIMARY KEY,
  produto_id INT,
  cliente_id INT,
  data_venda DATE,
  quantidade INT,
  valor_total DECIMAL(10, 2),
  FOREIGN KEY (produto_id) REFERENCES produtos(id),
  FOREIGN KEY (cliente_id) REFERENCES clientes(id)
);


-- Criação da tabela "produtos"
CREATE TABLE produtos (
  id INT PRIMARY KEY,
  nome VARCHAR(100),
  categoria VARCHAR(50),
  preco DECIMAL(10, 2)
);



-- Criação da tabela "clientes"
CREATE TABLE clientes (
  id INT PRIMARY KEY,
  nome VARCHAR(100),
  idade INT,
  cidade VARCHAR(100),
  canal_comunicacao VARCHAR(50)
);
```

## Scripts SQL para inserir registros nas tabelas "vendas", "produtos" e "clientes":

```
-- Inserção de registros na tabela "vendas"
INSERT INTO vendas (id, produto_id, cliente_id, data_venda, quantidade, valor_total)
VALUES
  (1, 1, 1, '2023-05-01', 3, 150.00),
  (2, 2, 2, '2023-05-02', 1, 50.00),
  (3, 3, 3, '2023-05-03', 5, 250.00),
  -- Adicione mais registros de acordo com suas necessidades

-- Inserção de registros na tabela "produtos"
INSERT INTO produtos (id, nome, categoria, preco)
VALUES
  (1, 'Camiseta', 'Vestuário', 25.00),
  (2, 'Calça Jeans', 'Vestuário', 80.00),
  (3, 'Tênis', 'Calçados', 120.00),
  -- Adicione mais registros de acordo com suas necessidades

-- Inserção de registros na tabela "clientes"
INSERT INTO clientes (id, nome, idade, cidade, canal_comunicacao)
VALUES
  (1, 'João', 30, 'São Paulo', 'E-mail'),
  (2, 'Maria', 25, 'Rio de Janeiro', 'Telefone'),
  (3, 'Pedro', 35, 'Belo Horizonte', 'WhatsApp'),
-- Adicione mais registros de acordo com suas necessidades

```
  
