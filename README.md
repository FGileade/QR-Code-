# Gerador de QR Code com Logotipo

Página web simples e independente (um único arquivo HTML, sem instalação nem dependências de build) para gerar QR Codes personalizados com um logotipo no centro.

## Funcionalidades

- Gera QR Code a partir de **link**, **e-mail** ou **usuário do Instagram**
- Permite inserir um logotipo/ícone que é sobreposto no centro do código
- Tamanho ajustável (200 a 600 px)
- Download do resultado em PNG
- Usa nível de correção de erro alto, para que o logotipo não comprometa a leitura do código

## Como usar

Abra o arquivo `index.html` diretamente no navegador — não é necessário instalar nada.

1. Escolha o tipo de conteúdo (Link, E-mail ou Instagram)
2. Preencha o campo com o endereço, e-mail ou usuário
3. (Opcional) Escolha uma imagem para usar como logotipo
4. Ajuste o tamanho, se desejar
5. Clique em **Gerar QR Code**
6. Clique em **Baixar PNG** para salvar a imagem

## Publicar online

### Vercel (recomendado)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/FGileade/QR-Code-)

Ou pela CLI:

```bash
npm install -g vercel
vercel login
vercel --prod
```

Como é um site estático (sem build, sem dependências), o Vercel detecta o `index.html` automaticamente — não é preciso configurar nada além do que já está no `vercel.json` deste repositório.

### GitHub Pages (alternativa)

1. Vá em **Settings → Pages** neste repositório
2. Em **Source**, selecione a branch `main` e a pasta `/ (root)`
3. Salve — o site ficará disponível em `https://fgileade.github.io/QR-Code-/`

## Tecnologia

- HTML, CSS e JavaScript puros
- [`qrcode-generator`](https://github.com/kazuhikoarase/qrcode-generator) (via CDN) para a geração do código
- Renderização e composição do logotipo feitas em `<canvas>`

## Licença

Distribuído sob a licença MIT — veja o arquivo [LICENSE](LICENSE).
