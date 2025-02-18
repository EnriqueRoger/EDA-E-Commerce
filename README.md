# **Análise Exploratória de Dados de um E-commerce**

![final_image](https://github.com/user-attachments/assets/cfb05277-9f31-48ee-bced-7b9849d18a16)

A Análise Exploratória de Dados (EDA) de um e-commerce é um processo essencial
que permite compreender a estrutura e características dos dados de vendas online. 
Esse processo envolve a utilização de técnicas em ETL (Extract, Transformation and Load),
Business Intelligence, Estatística descritiva e Python para resumir e examinar os 
dados coletados, identificando padrões, tendências, e possíveis 
anomalias. A EDA é fundamental para fornecer insights iniciais que guiam a construção de 
modelos preditivos, estratégias de marketing, e melhorias operacionais. Além disso, 
ela ajuda a garantir a qualidade dos dados e a detectar qualquer inconsistência 
ou erro que possa afetar as análises subsequentes.

## **Sumário**

1. **Objetivo**
2. **Problema de Negócio**
3. **Metadados**
4. **Entrega do Resultado**
5. **Conclusão da Análise**

## **Objetivo**

Este projeto visa explorar e aplicar conhecimentos em Análise Exploratória de Dados (EDA) utilizando o dataset do Kaggle 
"refined_ecommerce_product_data". O dataset está disponível para download neste repositório para aqueles que desejam explorá-lo também.

Dado que este é um dataset simples, achei interessante realizar uma exploração mais detalhada para descobrir insights 
em cada etapa de transformação e visualização de dados. Descrever o meu ponto de vista ao analisar os dados em um formato visual 
facilita a comunicação desses insights. Por isso, decidi formatar toda a análise em um Jupyter Notebook, que será publicado aqui no GitHub e em outras plataformas.

Nesse projeto de análise de dados, será feito um exercicio para praticar habilidades analíticas e exploratórias em um 
dataset de E-Commerce para entender o comportamento dos dados, tendências, correlação entre variáveis e identificar padrões 
que possam fornecer insights valiosos sobre o desempenho das vendas, preferências dos clientes e possíveis oportunidades 
de otimização. Os resultados da análise serão apresentados por meio de visualizações gráficas, permitindo uma melhor interpretação dos dados e facilitando a extração de insights estratégicos.

Antes de prosseguir para extração dos dados, vamos definir um contexto para o business case e algumas perguntas de 
problema de negócio utilizando o Copilot, que vai interpretar o meu metadados e entregar todo o problema estruturado
para servir como guia ao longo da análise explorátoria.

## **Problema de Negócio**

O principal desafio deste projeto é compreender de forma aprofundada o comportamento dos clientes e o desempenho dos produtos,
a fim de embasar decisões estratégicas que impulsionem as vendas, otimizem a precificação e aprimorem a experiência do consumidor. 
Para isso, a análise de dados será utilizada para identificar padrões de consumo, preferências e oportunidades de melhoria, 
permitindo uma abordagem mais assertiva na personalização de ofertas, na alocação de recursos e no desenvolvimento de ações 
que maximizem a satisfação e a fidelização dos clientes.

### **Audiência**

A solicitação para esta análise partiu do time de Business Intelligence (BI) da empresa, com o propósito de gerar insights 
estratégicos que subsidiem a tomada de decisão orientada por dados. O estudo atenderá diferentes áreas da organização, 
permitindo uma visão mais clara sobre o comportamento do consumidor e a performance dos produtos. As principais audiências beneficiadas incluem:

**Equipe de Marketing:** Para aprofundar o conhecimento sobre o perfil dos clientes, identificar suas preferências e personalizar ações de engajamento.

**Gestores de Produção:** Para avaliar o desempenho dos produtos com base em feedbacks, avaliações e histórico de compras, permitindo ajustes na qualidade e no portfólio.

**Equipe de Vendas:** Para otimizar a segmentação de mercado, aprimorar estratégias comerciais e ajustar campanhas promocionais com base em dados concretos.

Essa abordagem integrada permitirá decisões mais embasadas, contribuindo para o crescimento sustentável e a competitividade da empresa.

### **Perguntas de Negócio**

1. Quais são as faixas etárias dos clientes mais ativos no e-commerce? (Gráfico de barras para distribuição etária dos clientes)
2. Qual é a distribuição de gênero entre os clientes? Existe diferença no comportamento de compra entre eles? (Boxplot comparando o número de compras por gênero).
3. Como a faixa de preço dos produtos varia entre diferentes categorias e subcategorias? (Gráfico de colunas para visualizar a variação de preços).
4. Existe correlação entre preço e avaliação dos produtos? (Gráfico de Dispersão para visualizar a relação entre Preço e Nota_Avaliação).
5. Como os sentimentos das avaliações estão distribuídos entre os produtos? (Gráfico de barras empilhado para comparar a Revisão de Sentimento entre categorias e subcategorias de produtos).

## Metadados

Este conjunto de dados sintético representa dados de produtos de comércio eletrônico. Cada registro inclui as seguintes variáveis:

**Product_ID:** Um identificador exclusivo para cada produto.

**Product_Name:** Um nome que descreve o produto (por exemplo, "Mouse sem fio", "Smartphone"), gerado de acordo com sua categoria.

**Category:** a categoria ampla à qual o produto pertence (por exemplo, "Eletrônicos", "Roupas", "Móveis").

**Sub_Category:** Uma subcategoria específica dentro da categoria principal (por exemplo, "Telefones celulares" em "Eletrônicos").

**Price:** O preço do produto, que varia de acordo com sua categoria.

**Customer_Age:** A idade de um cliente que pode comprar o produto, variando de 18 a 65 anos.

**Customer_Gender:** O sexo do cliente ("Masculino" ou "Feminino").

**Purchase_History:** Uma contagem simulada do número de compras feitas pelo cliente, influenciada por sua idade e categoria de produto.

**Review_Rating:** Uma classificação dada ao produto, com base em seu preço, variando de 1 a 5 estrelas.

**Review_Sentiment:** o sentimento da avaliação, que pode ser "Negativo", "Neutro", "Positivo" ou "Muito Positivo", com base no preço.

O conjunto de dados simula as interações com o cliente de uma plataforma de comércio eletrônico, 
fornecendo insights realistas para tarefas de aprendizado de máquina, como sistemas de recomendação, 
segmentação de clientes ou previsão de preços.

## Entrega do Resultado

A Entrega do resultado é onde juntamos todos os insights adquiridos no Jupyter Notebook aqui, aglomerando
as principais informações, após visualizar os gráficos e dados, pensando no público que
vai receber não apenas as novas informações que foram vistas ao longo da análise, mas guiar os gestores e as equipes
a absorverem os insights sem que fiquem com dúvidas.

O cenário ideal para entregar esse resultado é aplicar algumas técnicas de Storytelling e fazer com que todos
saibam o próximo passo com os novos conhecimentos que foram adquiridas com a análise de dados.

### **Gestores de Produção**

☑ - Foco na Qualidade dos Produtos: Implementar processos rigorosos 
de controle de qualidade para as categorias com avaliações mais baixas. 
Investigar causas de insatisfação e ajustar o design, material e fabricação dos produtos.

☑ - Manter a Qualidade em Eletrônicos e Eletrodomésticos: Continuar investindo na qualidade 
dos produtos mais bem avaliados, garantindo que as expectativas dos clientes sejam continuamente atendidas.

☑ - Priorizar Produtos com Ticket Médio Elevado: Assegurar a 
disponibilidade de produtos com maior retorno financeiro para atender à demanda.

☑ - Introdução de Produtos de Preço Intermediário: Explorar a produção de novos 
produtos que atendam a uma faixa de preço intermediária para equilibrar a percepção de valor e ampliar a base de clientes.

### **Equipe de Marketing**

☑ - Categorias Premium: Identificar e promover produtos como 
itens de luxo para atrair consumidores que buscam qualidade superior.

☑ - Marketing Unificado: Desenvolver campanhas de marketing que possam 
ser aplicadas de maneira geral, considerando a semelhança nos padrões 
de compra entre os gêneros, mas monitorando continuamente para ajustes personalizados.

☑ - Transparência e Descrições Detalhadas: Melhorar as descrições de 
produtos para gerenciar expectativas e destacar características de valor agregado.

☑ - Ajuste de Preços para Produtos de Baixo Ticket Médio: Revisar e 
ajustar estratégias de preços para categorias de beleza e roupas, 
tentando encontrar um equilíbrio que aumente a percepção de valor sem comprometer a competitividade.

### **Equipe de Vendas**

☑ - Foco em Produtos de Beleza e Roupas: Treinar a equipe de 
vendas para oferecer suporte mais eficaz e informado sobre 
produtos de beleza e roupas, respondendo rapidamente às 
dúvidas e preocupações dos clientes.

☑ - Manter Suporte Diferenciado para Eletrônicos e Eletrodomésticos: 
Continuar oferecendo suporte de alta qualidade, enfatizando o valor do atendimento pós-venda.

☑ - Políticas Flexíveis de Devolução: Implementar políticas que 
facilitem a devolução de produtos, especialmente para os mais 
baratos, para aumentar a confiança dos clientes e em sequência, a revisão de sentimento.

☑ - Monitoramento Contínuo de Feedback: Estabelecer sistemas 
para revisar continuamente o feedback dos clientes e usar 
essas informações para fazer melhorias proativas nos produtos e serviços.

## Conclusão da Análise

Ao longo da análise exploratória dos dados do E-Commerce, foi possível identificar padrões e tendências valiosas sobre o comportamento dos consumidores, a qualidade percebida dos produtos e as oportunidades de melhoria dentro do marketplace. Cada insight extraído contribui para um entendimento mais profundo sobre como otimizar estratégias de precificação, marketing e gestão de produtos para maximizar a satisfação do cliente e o desempenho do negócio.

Os eletrônicos e eletrodomésticos despontam como os produtos mais bem avaliados, destacando-se pela alta satisfação do cliente. Essa percepção positiva pode ser resultado da qualidade percebida e do suporte eficiente, evidenciando a importância de manter estratégias de marketing eficazes e suporte ao cliente diferenciado para essas categorias.

Em contrapartida, os produtos de beleza e roupas apresentam as avaliações mais baixas, sugerindo a necessidade de uma investigação mais aprofundada sobre fatores como qualidade, atendimento ao cliente e percepção de valor. O ticket médio mais baixo dessas categorias pode indicar que os consumidores estão menos propensos a investir em tais produtos, possivelmente devido às expectativas não atendidas. Para reverter essa situação, estratégias como melhorias na qualidade, revisão de preços e marketing mais assertivo podem ser implementadas.

O estudo também revelou uma forte correlação entre preço e satisfação: produtos mais caros tendem a receber melhores avaliações, enquanto os mais baratos enfrentam desafios na percepção de qualidade. Esse fenômeno destaca a necessidade de gestão das expectativas dos clientes por meio de descrições de produtos mais detalhadas e transparentes, bem como políticas de devolução mais flexíveis.

A análise também apontou oportunidades na segmentação de mercado. A identificação de categorias premium e a possibilidade de introduzir produtos de preço intermediário podem equilibrar melhor a percepção de valor, ao mesmo tempo que ampliam as opções disponíveis para diferentes perfis de consumidores. Além disso, categorias com ticket médio elevado devem ser priorizadas na gestão de estoque para garantir a disponibilidade de itens com maior retorno financeiro.

Outro aspecto relevante é o comportamento de compra entre os gêneros, que mostrou padrões semelhantes, apesar de haver valores discrepantes no grupo masculino. Isso indica que estratégias de marketing podem ser amplamente aplicadas de maneira unificada, ao mesmo tempo em que o monitoramento contínuo dessas tendências pode trazer novas oportunidades de personalização no futuro.

Por fim, fica evidente a necessidade de um monitoramento contínuo da satisfação do cliente por meio da revisão de sentimentos e feedbacks. Essa prática não apenas permite melhorias contínuas na qualidade dos produtos e serviços, mas também possibilita um melhor posicionamento estratégico no mercado.

Com essas informações, o E-Commerce pode não apenas corrigir falhas e melhorar a percepção de valor dos produtos, mas também potencializar suas vendas, fidelizar clientes e fortalecer sua presença no mercado digital.
