
# Tratamento de dados utilizando Python para produção de relatório gerencial

![photovoltaics-solar-power-station-energy-from-natural](https://github.com/user-attachments/assets/4e619ca7-5d2f-4e0b-9ee3-af5c8b2080cf)
Usina Solar. Créditos: Freepik.


## Tecnologias e ferramentas
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" width="15" height="15"/> Python
   &nbsp;&nbsp;&nbsp;
   <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/pandas/pandas-original.svg" width="15" height="15"/> Pandas
   &nbsp;&nbsp;&nbsp;
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg" width="15" height="15" /> VS Code
    &nbsp;&nbsp;&nbsp;

## Contexto

Recebi a tarefa de produzir relatórios dinâmicos para uma empresa de gerenciamento de ativos. O objetivo era apresentar, de forma clara e eficiente, os principais indicadores de desempenho de um conjunto de usinas fotovoltaicas monitoradas por eles. Atualmente, a empresa utiliza Python para criar dashboards e gera relatórios estáticos em PDF. Embora esse processo atenda às necessidades dos clientes, ele é demorado e limita a exploração e visualização dos dados.

Minha proposta foi desenvolver uma solução que combinasse Python com uma ferramenta de visualização de dados, criando dashboards interativos e dinâmicos. Essa abordagem buscou demonstrar a viabilidade de otimizar a produção de relatórios e proporcionar uma experiência mais ágil e rica na análise dos indicadores.

## Estruturação e Preparação dos Dados
Os dados fornecidos pela contratante estavam no formato .json e eram organizados por SPE (uma subdivisão territorial das usinas entre transformadores). Minha primeira ação foi explorar um dos dicionários para compreender como os dados estavam estruturados.

Após identificar os KPIs (indicadores de performance) presentes na estrutura dos dados, separei aqueles que eram relevantes para a análise, conforme as orientações fornecidas pela empresa contratante. Esses KPIs foram organizados em uma lista, utilizada posteriormente na construção dos dataframes.

Na sequência, utilizei a biblioteca Pandas para criar DataFrames com os dados, transformando-os em tabelas que poderiam ser facilmente manipuladas e visualizadas no Power BI. Primeiramente, criei um DataFrame para cada arquivo .json existente e os salvei no formato .xlsx. Durante esse processo, precisei calcular a variável "Meta", conforme as instruções fornecidas pela contratante, e também realizar a transformação das datas, que estavam em formato de milissegundos, para o formato datetime. Essas operações se tornaram mais simples com o uso do Pandas, que facilita a sintaxe e otimiza o processamento do código.

Após obter os arquivos .xlsx individuais por SPE, o próximo passo foi concatená-los em um único DataFrame, de forma a unificar as informações. Esse DataFrame final incluiria todos os dados dos arquivos .xlsx individuais, além de uma coluna adicional que indicaria o SPE correspondente a cada conjunto de dados. Com o arquivo final salvo, segui para o Power BI para construir as visualizações.

