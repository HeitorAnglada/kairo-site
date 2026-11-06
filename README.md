# kairo-site

Site da Kairo: cardápio digital que a cozinha atualiza pelo WhatsApp. **falou. mudou.**

Uma página estática (`index.html`) com duas demos que rodam no navegador, sem servidor:

- **Cardápio pelo WhatsApp:** escreva ou toque num áudio pronto ("acabou o salmão", "o poke agora é 45", "prato do dia é lámen, 39") e o cardápio da mesa muda na hora. O entendimento das mensagens é feito por regras simples em JavaScript, só para a demonstração; no produto é a IA.
- **Salão (plano completo, em breve):** mapa de mesas livres, ocupadas e a limpar, com fila e avisos para a recepção.

## Ver localmente

Abra `index.html` no navegador, ou rode `python3 -m http.server` nesta pasta e acesse http://localhost:8000.

## Publicar

Funciona direto no GitHub Pages (Settings → Pages → branch `main`, pasta `/`), Netlify ou Vercel.

## Antes de divulgar

- Trocar o link do botão "quero testar no meu restaurante" (`#ctaZap`) pelo `wa.me/55DDDNUMERO` do WhatsApp comercial.
