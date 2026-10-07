# Nome e subdomínio do site

## Nome oficial
**Play Burguer Aradas**

## Subdomínio escolhido
**playburguer**

O endereço final ficará assim, quando indicar o domínio principal:

```text
playburguer.SEUDOMINIO.pt
```

Exemplos:

```text
playburguer.playburguer.pt
playburguer.restaurante.pt
playburguer.oseudominio.com
```

## Como ativar o subdomínio

Para o subdomínio funcionar online, precisa de ter um domínio comprado e acesso à zona DNS.

No painel DNS do domínio, crie um registo:

```text
Tipo: CNAME
Nome/Host: playburguer
Valor/Destino: destino fornecido pela plataforma de alojamento
```

Exemplos de destino, dependendo da plataforma:

- Vercel: `cname.vercel-dns.com`
- Netlify: o domínio `.netlify.app` do site
- GitHub Pages: `NOMEUTILIZADOR.github.io`

Depois, na plataforma onde publicar o site, adicione o domínio personalizado:

```text
playburguer.SEUDOMINIO.pt
```

> Nota: sem saber o domínio principal real, deixei o ficheiro `CNAME.example` como modelo. Quando souber o domínio, substitua `SEUDOMINIO.pt` pelo domínio verdadeiro e renomeie para `CNAME` se a plataforma exigir.
