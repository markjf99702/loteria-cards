# loteria-cards

A play-along Lotería board for the iPad or phone. Everything is stored on the device: no accounts, nothing sent anywhere.

## The board — `index.html`

Someone calls the cards; you tap **Cantaron…**, pick the card, and it marks itself on every tabla where it appears.

- Pick the game each round: Clásico (4 in a row, 4 corners, or 4 in a square), or a single shape — La Equis, La Ele, El Marco, Rieles, Escalera, Centro, Siete Loco, Tabla Llena.
- Edit tablas square by square (doubles allowed, house rules), add up to six per person, or add a **printed tabla** by its juego name and number.
- Several people on one device, each with their own tablas; **Share** makes a link that carries a set of tablas to another phone.

## The caller

[El Cantor](https://github.com/markjf99702/el-cantor) lives in its own repo. It calls the cards aloud in Spanish, prints numbered tablas that this board can load, and checks a ¡Lotería!. The board's Settings link to it at https://markjf99702.github.io/el-cantor/.

## Files

- `deck.js` — the cards, their verses, the winning shapes, and the juego generator.
  - The generator is frozen: changing it would change every tabla already printed.
  - El Cantor carries the same file; keep the two in step.
- The card images sit beside the page.
