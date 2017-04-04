# HREFLANG

## O que é hreflang
É uma tag  HTML que vai dentro da seção head do código-fonte da página

## Para que é usado
Serve para ajudar os rastreadores do Google a entender que determinadas páginas, subdomínios ou domínios de nível de código de países diferentes são direcionados para um país especifico. Com isso o hreflang marca corretamente as páginas da web informando que existem várias versões dessa mesma página.

## Como implementar
- Em cada uma das páginas do nosso site devemos colocar uma ligação as versões desse conteúdo, em várias línguas. Se publicamos o site em portugues e inglês. Na versão em portugues deveremos colocar uma ligação à versão inglesa, e vice-versa.
- Se você tiver várias versões de um URL em diferentes idiomas, cada página de idioma deve identificar todos, mesmo a língua em que se encontra.
- Se cada região tem conteúdos diferentes, é necessário atualizar o HTML de cada URL e fazer as ligações "link" rel="alternate" hreflang="x". Se tem página padrão que não tem como alvo qualquer idioma ou localidade específica acrescenta rel="alternate" hreflang="x-default".

Existem 3 métodos para implementar a hreflang, mas a forma  mais comum é dentro da página no head, apontando para a url das línguas do site.
```html
<!-- Para seletores de linguagem redirecionar automaticamente -->
<Link rel = "alternate" hreflang = "x-default" href = "http://www.example.com/page.html" />
<!-- Para colocar a url de todas as línguas -->
<Link rel = "alternate" hreflang = "en" href = "http://www.example.com/page.html" />
<Link rel = "alternate" hreflang = "de" href = "http://de.example.com/seite.html" />
<!-- Para colocar a url de mesma língua, mas diferentes área geográfica-->
<Link rel = "alternate" hreflang = "en-gb" href = "http://pt-br.exemplo.com/page.html" />
<Link rel = "alternate" hreflang = "en-us" href = "http://en-us.example.com/page.html" />
```
## O que conseguimos com isso
- Maior visibilidade em motores de busca: O Google dará prioridade a cada versão de língua dependendo da língua do utilizador que efetua a pesquisa e a sua localização. Assim, um utilizador inglês encontrará primeiro a versão em inglês do nosso site.
- Aumentará o rácio de cliques nos resultados de pesquisas: se oferecermos aos utilizadores um resultado de pesquisa na sua língua, existe maior probabilidade de captarmos a sua atenção.
- Evitaremos duplicidades de conteúdo: se tivermos uma versão do nosso site em inglês para os Estados Unidos e outra diferente para a Inglaterra, o Google entenderá que se tratam de versões alternativas do conteúdo e não detetará estes conteúdos como duplicados (situação que poderia penalizar o nosso posicionamento).

## O que pode dar errado
- Faltando ligações de confirmação: Se a página A faz referencia para a página B, a página B deve referenciar de volta para página A. Se esta condição não for atendida em todas as páginas que usam anotações "hreflang", não vai ser interpretado corretamente.
- Códigos de idioma incorretas: Certificar que os códigos de linguagem usado identifica o idioma no formato ISO 639-1 e, opcionalmente, a região em ISO 3166-1 formato Alpha 2 para um URL alternativo. Não pode especificar apenas a região.
- Plugin qTranslate WordPress: porque está dizendo que todas as informações estão duplicadas.
