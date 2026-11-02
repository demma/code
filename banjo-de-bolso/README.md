# Banjo de Bolso

App web instalável (PWA) para banjo de 5 cordas: dicionário de acordes, rolos (dedilhados), riffs e ritmos, com áudio sintetizado e tablatura animada.

## Estrutura
- `app.html`: fonte única do app (HTML + CSS + JS, sem dependências).
- `build.py`: gera `index.html` (PWA) a partir de `app.html`.
- `manifest.webmanifest`, `sw.js`, `icons/`: instalação e uso offline.

## Rodar localmente
```bash
python3 build.py
python3 -m http.server 8000   # abra http://localhost:8000
```

## Publicar (GitHub Pages)
Ative Pages no repositório apontando para a branch e sirva a pasta `banjo-de-bolso/`.
No celular, abra a URL e use "Adicionar à tela inicial".

## Como o conteúdo é gerado
- **Acordes**: calculados a partir da afinação (não digitados à mão). Toda combinação das cordas 4–1 com até 4 casas de abertura que cubra as notas obrigatórias do acorde; ordenadas por posição, nº de dedos e baixo na tônica.
- **Padrões**: mini-notação em `app.html` (`P3 I2 M1`, `h3:2`, `/3:4`, `B3-1`, `X4-1`, `P5+M1`, `-`).
