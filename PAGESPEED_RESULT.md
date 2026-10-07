# Resultado do teste de performance

Data: 2026-10-06

## Nota importante

A API pública do Google PageSpeed Insights não conseguiu ser usada diretamente neste ambiente porque o site ainda está num preview privado e a API também devolveu limite/quota. Por isso, foi executado um teste local com Lighthouse, que é o mesmo motor usado pelo PageSpeed Insights.

## Resultado inicial

Antes da otimização, a versão com imagens embutidas no HTML estava pesada:

- Mobile Performance: 46/100
- Desktop Performance: 80/100

Principal problema: HTML com imagens em base64, deixando o documento principal com cerca de 2,2 MB.

## Otimização feita

- Transformei o `index.html` na versão recomendada para publicação.
- Troquei imagens embutidas por imagens externas otimizadas em WebP.
- Mantive carregamento preguiçoso nas imagens do menu.
- Mantive prioridade alta apenas na imagem principal.
- Mantive uma versão de ficheiro único em `index-portable.html`, mas ela não é recomendada para PageSpeed.

## Resultado final — Mobile

- Performance: 99/100
- Acessibilidade: 96/100
- Boas práticas: 96/100
- SEO: 100/100

Métricas principais:

- First Contentful Paint: 1,0 s
- Largest Contentful Paint: 2,0 s
- Speed Index: 1,0 s
- Total Blocking Time: 10 ms
- Cumulative Layout Shift: 0
- Interactive: 2,1 s
- Peso total carregado: 556 KiB

## Resultado final — Desktop

- Performance: 100/100
- Acessibilidade: 96/100
- Boas práticas: 96/100
- SEO: 100/100

Métricas principais:

- First Contentful Paint: 0,3 s
- Largest Contentful Paint: 0,6 s
- Speed Index: 0,3 s
- Total Blocking Time: 0 ms
- Cumulative Layout Shift: 0
- Interactive: 0,6 s
- Peso total carregado: 996 KiB

## Conclusão

O site está apto para passar num teste de velocidade, sobretudo quando publicado num alojamento com compressão automática, como Netlify, Vercel, Cloudflare Pages ou GitHub Pages.

Pontos que podem melhorar ainda mais:

- Criar versões menores das imagens por resolução, usando `srcset`.
- Publicar numa plataforma com Brotli/Gzip automático.
- Executar o PageSpeed Insights oficial quando o subdomínio público estiver ativo.
