# Tip Check — atualização 3.0.0

Esta versão corrige o principal problema observado nos testes: o OCR reconhecia o print, mas não conseguia transformar o texto do cartão do cliente em um destino utilizável.

### O que mudou

- OCR em 3 passagens:
  - imagem inteira;
  - região central/inferior;
  - região inferior, onde normalmente está o cartão do cliente.
- Ampliação da imagem antes do OCR.
- Conversão para escala de cinza e aumento de contraste.
- Reconhecimento mais tolerante de Eircodes, incluindo `D14Y265` e variações com espaço.
- Identificação de endereço por número + nome da rua.
- O postcode/Eircode passa a ser a chave principal do histórico.
- Texto OCR pode ser aberto em "Texto reconhecido (diagnóstico)" para conferir o que foi lido.
- Service Worker atualizado para `v3`.
- Banco local continua sendo preservado durante a atualização.

## Atualização no GitHub

Substitua:
- `index.html`
- `sw.js`
- `manifest.webmanifest`
- `install.html`
- `version.txt`

Mantenha seus:
- `icon-180.png`
- `icon-192.png`
- `icon-512.png`

Depois aguarde o GitHub Pages publicar a nova versão e abra o site novamente no Safari.
