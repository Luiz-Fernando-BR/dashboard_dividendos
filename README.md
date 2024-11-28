# Análise de ações que pagam dividendos de pelo menos 6%
Este projeto consiste em uma aplicação interativa desenvolvida com Streamlit, que permite analisar os dividendos pagos por ações nos últimos 12 meses. 
O principal objetivo é calcular e exibir o valor total de dividendos pagos, juntamente com um gráfico que ilustra o histórico de pagamentos, com base no Dividend Yield (DY) de no mínimo 6%.
# Funcionalidades
  - Consulta de Dividendos: O usuário pode inserir o código de uma ação (no formato .SA para ações brasileiras) e a aplicação irá buscar os dados históricos de dividendos dos últimos 12 meses.
  -  Cálculo do Preço Máximo: Com base no valor total dos dividendos pagos, a aplicação sugere o preço máximo que seria adequado pagar pela ação, considerando um Dividend Yield mínimo de 6%.
  - Visualização Gráfica: Exibe um gráfico de barras dos dividendos pagos, com a data no eixo X formatada como "Mês/Ano", permitindo uma visualização clara da distribuição dos dividendos ao longo do tempo.
# Requisitos
  Antes de rodar a aplicação, é necessário ter o seguinte ambiente configurado:
  Python 3.12.4
# Bibliotecas:
  yfinance para acessar os dados financeiros
  streamlit para construir a interface interativa
  matplotlib para visualização gráfica
  pandas para manipulação de dados
# Como Rodar
  1 - Instale as dependências: É recomendável utilizar um ambiente virtual. No terminal, execute: pip install -r requirements.txt
  2 - Rodar a aplicação: Após instalar as dependências, execute o seguinte comando para iniciar a aplicação Streamlit: streamlit run dashboard_dividendos.py
  3 - Interação com a aplicação:
      - Acesse a interface na web que será aberta automaticamente.
      - Insira o código da ação (exemplo: XPCA11.SA) na barra lateral e clique no botão "OK" para visualizar os dividendos em tabela, o somatório dos mesmos, a sugestão de preço máximo e um gráfico de barras.
# Como Funciona
  Consulta de Dados: Ao inserir o código de uma ação, o programa usa o yfinance para obter os dados históricos dos últimos 12 meses da ação no mercado brasileiro.  
  Filtragem de Dividendos: Apenas os dividendos positivos são exibidos e utilizados para o cálculo total.  
  Cálculo do Preço Máximo: O valor total dos dividendos pagos nos últimos 12 meses é dividido por 6% (DY mínimo), fornecendo uma estimativa do preço máximo sugerido para a ação.  
  Gráfico de Dividendos: Um gráfico de barras é gerado para visualizar o pagamento dos dividendos ao longo do ano, facilitando a análise.
# Exemplo de Saída
  Após inserir um código de ação válido, a aplicação exibirá:
    Tabela com os dividendos pagos.
    Total de dividendos pagos no período de 12 meses.
    Preço máximo sugerido para compra da ação.
    Gráfico de barras com os dividendos pagos ao longo do ano.
