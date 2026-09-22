# loteria-cards

Two pages for a Lotería night, one for the players and one for the caller. Everything is stored on the device: no accounts, nothing sent anywhere.

## The board — `index.html`

A play-along board for the iPad or phone. Someone calls the cards; you tap **Cantaron…**, pick the card, and it marks itself on every tabla where it appears.

- Pick the game each round: Clásico (4 in a row, 4 corners, or 4 in a square), or a single shape — La Equis, La Ele, El Marco, Rieles, Escalera, Centro, Siete Loco, Tabla Llena.
- Edit tablas square by square (doubles allowed, house rules), add up to six per person, or add a **printed tabla** by its juego name and number.
- Several people on one device, each with their own tablas; **Share** makes a link that carries a set of tablas to another phone.

## The caller — `cantor.html`

El Cantor replaces the deck and the person reading it.

- Shuffles the 54 cards and turns them over one at a time, reading each verse and name aloud in Spanish (the device's own voice). Tap ▶ to call on its own at a slow, normal or fast pace, or turn each card by hand.
- **Adivinanza** mode reads the verse with the card face down so the table can guess before it turns over.
- The **sábana** shows all 54 cards, lit in the order they were called.
- **Print tablas** makes a PDF of numbered tablas to print at home (one big or two per page, Letter or A4). A set — a *juego* — is built from its name, so `CANELA` tabla 7 is always the same tabla.
- **¡Lotería!** checks a claim: type the juego and tabla number and it shows the tabla with beans on the called cards, says whether it wins the current game and when it first did. For store-bought tablas, tap the cards the player reads out instead.
- Keeps a tally of who won each round.

## Files

- `deck.js` — the cards, their verses, the winning shapes, and the juego generator, shared by both pages. The generator is frozen: changing it would change every tabla already printed.
- The card images sit beside the pages.
