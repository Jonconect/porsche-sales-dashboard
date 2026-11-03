# porsche-sales-dashboard
 Dashboard interativa de vendas Porsche com filtros, KPIs e insights por modelo e cidade.
# Porsche Sales Dashboard

Dashboard interativa para analisar 100 registros de vendas Porsche. Permite explorar modelos, anos-modelo, cidades, estados, formas de pagamento e períodos de venda.

## Perguntas de negócio

1. **Quais modelos aparecem entre os mais vendidos em cada cidade?**  
   Ajuda a comparar os modelos registrados em cada localidade. O painel mostra os modelos empatados no topo e sinaliza cidades com poucas vendas.

2. **Qual ano-modelo lidera as vendas no recorte selecionado?**  
   Permite identificar o ano-modelo com mais registros após a aplicação dos filtros.

3. **Como as vendas se distribuem ao longo do tempo, por estado e por forma de pagamento?**  
   Ajuda a observar padrões temporais e geográficos, além das formas de pagamento registradas.

## Funcionalidades

- Filtros por modelo, ano-modelo, cidade, forma de pagamento e período.
- Indicadores de vendas, receita registrada, ticket médio, cidades com vendas e ano-modelo líder.
- Gráficos e análises atualizados conforme os filtros.
- Comparação temporal e visão geográfica por estado e cidade.
- Exportação em CSV dos registros filtrados.

## Dados e tratamento

O projeto usa a planilha sanitizada do desafio, com 100 vendas. A dashboard utiliza os campos tratados para apresentar os dados. Mantém os registros como recebidos e sinaliza datas inválidas e datas futuras; as análises temporais usam apenas datas válidas.

A planilha não informa a moeda dos preços nem a data de atualização da fonte. Por isso, esses pontos são indicados no painel, sem presumir uma moeda.

**Privacidade:** os dados estão incorporados ao arquivo HTML para permitir filtros sem servidor. Como este repositório é público, confirme que a base pode ser divulgada e inspecionada por qualquer pessoa.

## Como foi desenvolvido

O projeto foi desenvolvido iterativamente com **Manus Webdev**, a partir dos requisitos do desafio e das perguntas de negócio. Não foi criado com ChatGPT Canvas nem com um agente de skill própria.

### Prompt de trabalho

> Crie uma dashboard responsiva em HTML estático para analisar a planilha sanitizada de 100 vendas Porsche. Inclua filtros por modelo, ano-modelo, cidade, forma de pagamento e período de venda. Responda: quais modelos se destacam em cada cidade; qual ano-modelo lidera no recorte; e como as vendas se distribuem no tempo, por estado e por forma de pagamento. Mostre indicadores de vendas e receita, gráficos que atualizam com os filtros, análise de qualidade dos dados e exportação CSV. Use uma interface elegante e caminhos relativos compatíveis com GitHub Pages.

O painel foi refinado em etapas para incluir comparação temporal, análise geográfica por estado, insights por cidade, exportação CSV e avisos sobre a qualidade dos dados. Na cópia para GitHub Pages, imagens oficiais foram substituídas por espaços reservados por cautela com direitos de redistribuição.

## Acessar

- **Repositório:** https://github.com/Jonconect/porsche-sales-dashboard
- **Dashboard no GitHub Pages:** https://jonconect.github.io/porsche-sales-dashboard/

O endereço do GitHub Pages ficará disponível após ativar o Pages em **Settings → Pages**, usando a branch `main` e a pasta `/(root)`. Depois da publicação, abra o link para confirmar que a página carrega.

## Publicação

O site é estático. Os arquivos `index.html` e a pasta `public/` devem permanecer na raiz do repositório. Para ativar o GitHub Pages, selecione **Settings → Pages → Deploy from a branch → `main` → `/(root)`**.
