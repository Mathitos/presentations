---
marp: true
theme: payfy-theme
footer: " "
---
<!-- _class: lead -->
# Protocolos de comunicação
### por Matheus Anzzulin
---
<!-- _class: image-left -->
## UDP
  *(User Datagram Protocol)*

  - Sem Ordem
  - Sem garantia de entrega ( at most once )

![funny image](https://thumbs.gfycat.com/VibrantEmbellishedJaeger-max-1mb.gif)

---
<!-- _class: image-right -->
## TCP
  *(Transmission Control Protocol)*

  - three way handshake ( SYN,SYN-ACK,ACK )
  - Garantia de entrega (at least once)
  - Ordenado
  - Sincronizado (Menos Perfomatico)

![funny image](https://c.tenor.com/oTwrhPPOuP8AAAAM/safety-first-jake-peralta.gif)

---
<!-- _class: image-left -->
## Web Socket
 - pode começar de ambos os lados
 - implementado em cima de tcp

![funny image](https://c.tenor.com/oTwrhPPOuP8AAAAM/safety-first-jake-peralta.gif)
---
![websocket diagram](https://assets-global.website-files.com/5f3c19f18169b62a0d0bf387/60f278d188056a50c045f4bd_Architecture%20diagram%20for%20Websocket-02%20(1).jpg)

## XMPP
*(Extensible Messaging and Present Protocol)*
