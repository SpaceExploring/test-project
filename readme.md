# Project Titel

Een korte beschrijving van uw project.

## Inhoudsopgave

- [Beschrijving](#beschrijving)
- [Installatie](#installatie)
- [Gebruik](#gebruik)
- [code] (#code) (+comments om de functies te laten zien)
## Beschrijving

Dit project is een project met het doel om leuke dingen te laten zien over undertale. Het is ontworpen om je te laten verdiepen in de wereld van Undertale en er interesse in te krijgen.

## gebruik

Je start op een pagina met een introductie over zielen, door middle van het gebruik met de sterkste en meest unieke ziel op de hoofpagina Undertale-heartanimatie.html, met gebruik van de juiste kleuren om ze te laten zien. Ook komt er een Over-Undertale pagina voor informatie over de zielen en de krachten die ze beschikken.

## code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Animation</title>
    <style>
    * {
        margin: 0; /* Geen marge voor alle elementen */
        padding: 0; /* Geen padding voor alle elementen */
    }
       body {
    display: flex; /* Flexbox voor centeren */
    justify-content: center; /* Horizontaal centreren */
    align-items: center; /* Verticaal centreren */
    height: 100vh; /* Volledige hoogte van het venster */
    background-color: black; /* Zwarte achtergrond voor contrast */
}

.heart-container {
    position: relative; /* Relatieve positie voor hartcontainer */
    width: 100px;   /* Breedte van het hart */
    height: 100px;  /* Hoogte van het hart */
}

.heart {
    position: absolute; /* Absoluut gepositioneerd om binnen container te plaatsen */
    width: 100px;   /* Breedte van het hart */
    height: 100px;  /* Hoogte van het hart */
    background-color: red; /* Kleur van het hart */
    animation: flicker 1s infinite; /* Toepassen van flikkeranimatie */
    transform: rotate(-45deg) scaleY(1) scaleX(1); /* Combineren van transformaties */
    box-shadow: 0 0 50px red, 0 0 50px red; /* Rode schaduw toevoegen */
}

.heart::before,
.heart::after {
    content: ""; /* Lege inhoud voor pseudo-elementen */
    position: absolute; /* Absoluut gepositioneerd voor lobben */
    width: 100px;   /* Breedte van hartlobben */
    height: 100px;  /* Hoogte van hartlobben */
    background-color: red; /* Kleur voor lobben */
    border-radius: 50%; /* Ronde lobben maken */
}

.heart::before {
    top: -50px; /* Positie van de bovenste lob */
    left: 0;
}

.heart::after {
    left: 50px; /* Positie van de rechter lob */
    top: 0;
}

@keyframes flicker {
    0% { transform: rotate(-45deg) scaleY(1) scaleX(1); }
    25% { transform: rotate(-45deg) scaleY(1.2) scaleX(1.2); }
    50% { transform: rotate(-45deg) scaleX(1.2) scaleY(1.2);  }
    100% { transform: rotate(-45deg) scaleY(1) scaleX(1); }
    /*Maakt een flickerende animatie voor het heart dat varieert met grootte op bepaalde percentages, de paginas voor de zielen hebben dezelfde code maar met andere kleur rgb code voor de zielen uiterraat*/
}

.navbar {
    padding: 15px; /* Ruimte rond de inhoud */
    color: white; /* Tekstkleur */
    display: flex; /* Flexbox voor plaatsing */
    justify-content: center; /* Inhoud centreren */
    position: fixed; /* Vast aan de bovenkant */
    top: 0; /* Uitgelijnd aan de bovenkant */
    width: 100%; /* Volledige breedte */
}

h1 {
    font-size: 82px; /* Pas aan indien nodig */
    font-weight: bold; /* Voor benadrukken */
    color: white; /* Pas kleur aan indien nodig */
}
    </style>
</head>
<body>
    <div class="navbar">
        <h1>UNDERTALE</h1> <!-- Titel bovenaan -->
    </div>
    <div class="heart-container">
        <div class="heart"></div> <!-- Hartvorm -->
    </div>
    
</body>
</html>
