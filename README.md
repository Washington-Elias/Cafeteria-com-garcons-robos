# Cafeteria com Garçons Robôs 🤖☕

## Descrição do Projeto
Este projeto analisa dados de restaurantes nos EUA para identificar padrões sobre redes de restaurantes, número de assentos e distribuição geográfica.  
O objetivo é entender quais tipos de estabelecimentos são mais comuns em redes, como dimensionar o número de assentos e quais locais oferecem melhores oportunidades para expansão de negócios — aplicando esses insights ao conceito de uma **cafeteria inovadora com garçons robôs**.

## Ferramentas e Bibliotecas Utilizadas
- **Pandas** – manipulação de dados  
- **Matplotlib** – visualização gráfica  
- **Seaborn** – análises estatísticas (boxplots, distribuições)  
- **Regex (re)** – extração de nomes de ruas a partir dos endereços  

## Tabela
As principais variáveis do dataset `rest_data_us_upd.csv` foram:
- **object_type** – tipo de estabelecimento (café, restaurante, fast food etc.)  
- **chain** – indica se é de rede (1 = sim, 0 = não)  
- **number** – número de assentos  
- **address** – endereço completo  
- **street** – nome da rua (extraído via regex)  

## Metodologia
1. Carregamento e inspeção inicial dos dados (head, info, valores ausentes)  
2. Análise da proporção de tipos de estabelecimentos  
3. Comparação entre **redes** e **não redes**  
4. Estudo do número de assentos por tipo e por rede  
5. Extração dos nomes das ruas a partir do endereço  
6. Identificação das ruas mais movimentadas e análise da distribuição de assentos  
7. Criação de gráficos: pizza, barras e boxplots  

## Pré-processamento
- Conversão de colunas para tipo numérico (`number`, `chain`)  
- Remoção de valores ausentes  
- Criação da coluna **street** a partir da coluna **address**  
- Seleção de subset de dados para ruas com ≥ 10 restaurantes  

## Análise dos Dados
- **Redes** tendem a ter estabelecimentos menores e padronizados  
- **Independentes** costumam ter mais assentos e estruturas maiores  
- **Tipos mais comuns em redes**: cafés, lanchonetes e fast foods  
- **Ruas movimentadas** mostram diversidade, mas a maioria dos restaurantes concentra entre 30–60 assentos  
- **Maioria das ruas** tem apenas um restaurante cadastrado → dispersão geográfica  

## Resultados
- Restaurantes de rede priorizam unidades compactas para alto giro e menor custo fixo  
- Estabelecimentos independentes geralmente são maiores e menos padronizados  
- Há oportunidade de crescimento em ruas com baixa concorrência  
- Faixa ideal para novos estabelecimentos: **30–50 assentos**  

## Aprendizados
- O modelo de cafeterias inovadoras (como com garçons robôs) deve ser **padronizável e escalável**  
- Espaços menores favorecem eficiência e replicabilidade  
- Ruas com alta densidade são bons pontos para testar protótipos  
- Ruas pouco exploradas representam oportunidade de expansão estratégica  
- É viável criar uma rede competitiva, equilibrando custo, tempo de atendimento e experiência do cliente
