# Porsche Sales Intelligence — export estático para GitHub Pages

Este pacote contém uma cópia estática da dashboard com os dados já embutidos no `index.html`, caminhos relativos e o clipe fornecido pelo usuário. Não requer Node.js, banco de dados ou API. Para revisão antes de uma publicação pública, as fotos Porsche Newsroom/Porsche.com foram removidas e substituídas por espaços reservados; o slogan também foi trocado por uma chamada independente. O painel continua interativo, mas será preciso inserir imagens que você tenha autorização para redistribuir se quiser mostrar carros no hero e na prévia por modelo.

## Testar localmente

Descompacte o arquivo, entre na pasta extraída e execute `python3 -m http.server 8080`. Abra `http://localhost:8080` no navegador. Mantenha `index.html` na raiz e a pasta `public/` ao lado dele.

## Publicar com GitHub Pages

1. Crie um repositório vazio no GitHub e descompacte todos os arquivos deste pacote na raiz da cópia local.
2. No terminal, dentro dessa pasta, execute:

```bash
git init -b main
git add .
git commit -m "Publica dashboard independente"
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```

3. No GitHub, abra **Settings → Pages**. Em **Build and deployment**, escolha **Deploy from a branch**, selecione `main` e a pasta `/(root)`, depois salve. A disponibilidade do Pages para repositórios privados depende do plano e da configuração da conta.

O HTML usa caminhos `./public/...`, compatíveis com o endereço de projeto do GitHub Pages. Para atualizar, faça as alterações localmente, depois use `git add`, `git commit` e `git push`.

## Inserir imagens licenciadas

Substitua o bloco `.hero-photo-placeholder` em `index.html` por uma imagem local que você tenha direito de publicar, por exemplo `./public/images/hero.webp`. Para as imagens da prévia, atualize as entradas `src` e `fallback` de `previewVisuals` para arquivos licenciados dentro de `./public/images/model-previews/`. Não copie fotografias do Porsche Newsroom/Porsche.com para um repositório público sem autorização específica.

## Direitos e atribuição

Os [termos oficiais do Porsche Newsroom para imagens e vídeos](https://newsroom.porsche.com/en/images-videos.html) e o [documento completo de condições](https://newsroom.porsche.com/pdf/9b9ca046-fac8-4621-ac83-75f023fcb4e1?print) indicam que os materiais são protegidos, destinados a jornalistas como fontes de reportagens próprias, não destinados a uso comercial e não devem ser repassados a terceiros não autorizados. Por esse motivo, essas fotografias não estão incluídas neste ZIP. O clipe e seu pôster foram fornecidos pelo usuário; confirme que você tem os direitos de todos os elementos antes de publicá-los. O aviso de independência não substitui autorização legal.


## Dados incorporados

O `index.html` contém os 100 registros para permitir filtros e gráficos sem servidor. Se o repositório ou o site ficar público, qualquer pessoa poderá inspecionar e extrair os valores de modelo, Model Year, cidade/estado, forma de pagamento, data e preço. Confirme que a base pode ser divulgada; se não, use repositório privado quando disponível, remova/anonimize os campos sensíveis ou adote uma API/servidor com controle de acesso.
