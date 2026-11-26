# kairo-site

Site da Kairos: cardápio digital que a cozinha atualiza pelo WhatsApp. **falou. mudou.**

Uma página estática (`index.html`) com duas demos que rodam no navegador, sem servidor:

- **Cardápio pelo WhatsApp:** escreva ou toque num áudio pronto ("acabou o salmão", "o poke agora é 45", "prato do dia é lámen, 39") e o cardápio da mesa muda na hora. O entendimento das mensagens é feito por regras simples em JavaScript, só para a demonstração; no produto é a IA.
- **Salão (plano completo, em breve):** mapa de mesas livres, ocupadas e a limpar, com fila e avisos para a recepção.

## Ver localmente

Abra `index.html` no navegador, ou rode `python3 -m http.server` nesta pasta e acesse http://localhost:8000.

## Publicar

Funciona direto no GitHub Pages (Settings → Pages → branch `main`, pasta `/`), Netlify ou Vercel.

## Antes de divulgar

- Trocar o link do botão "quero testar no meu restaurante" (`#ctaZap`) pelo `wa.me/55DDDNUMERO` do WhatsApp comercial.

## Direção visual e movimento

A página segue "uma noite de serviço": cada seção é marcada por um horário (21:15, 22:30, amanhã…), o kairós da marca. Regras de movimento (baseadas em emilkowalski/skills):

- Curvas próprias: `--ease-out: cubic-bezier(.23,1,.32,1)` e `--ease-in-out: cubic-bezier(.77,0,.175,1)`. Toque em botões: `scale(.97)` em 160 ms.
- Só três momentos animados de propósito: a entrada do hero, a cena "acabou o salmão" (toca uma vez e tem "ver de novo") e a linha do tempo de "como funciona", que se desenha uma vez. Nada de fade-in em toda seção.
- Hover só em `(hover:hover) and (pointer:fine)`. Animação só em `transform`, `opacity` e `filter`.
- Com `prefers-reduced-motion`, nada se desloca: tudo vira troca de opacidade e a cena já aparece no estado final.
