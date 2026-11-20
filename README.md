# Colombo Design: site

Landing page estática (HTML, CSS e JS puros, sem build) de **colombodesign.com.br**.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `public/index.html` | O site. É o único arquivo que o navegador abre. |
| `img/` | Prints do portfólio |
| `favicon.svg`, `apple-touch-icon.png` | Ícone da aba e do celular |
| `og.jpg` | Imagem que aparece quando o link é compartilhado no WhatsApp e nas redes |
| `robots.txt`, `sitemap.xml` | Ajudam o Google a encontrar o site |
| `page.html` | Cópia de trabalho usada na prévia. Não precisa subir. |

## Publicar na Cloudflare Pages (grátis)

1. **GitHub:** crie um repositório (por exemplo `colombodesign-site`) e suba todos os arquivos desta pasta.
2. **Cloudflare:** acesse dash.cloudflare.com, abra **Workers & Pages**, clique em **Create** e depois em **Pages**, e escolha **Connect to Git**. Selecione o repositório.
3. **Configuração do build:** em Framework preset, escolha *None*. Deixe o Build command vazio e use `/` como Build output directory. Clique em **Save and Deploy**.
4. **Domínio:** no projeto do Pages, abra **Custom domains** e adicione `colombodesign.com.br` e `www.colombodesign.com.br`. A Cloudflare informa dois *nameservers*. Copie esses dois para o seu domínio no Registro.br, em **DNS** e depois em **Alterar servidores DNS**. A propagação leva de algumas horas até 1 dia.

A partir daí, cada alteração enviada ao GitHub vai ao ar sozinha em cerca de 1 minuto.

## Trocar o número do WhatsApp

No fim do `index.html`, altere a linha `var numero = "5551998974961";`. O formato é 55, depois o DDD e depois o número, sem espaços.

Publicação automática: cada envio para a branch main é publicado pela Cloudflare.

