# Full Stack Open Osa 3: Frontend

Tämä repositorio sisältää Full Stack Open Osa 3 -projektin frontend -koodin. 

Frontend on rakennettu käyttäen Reactia ja Viteä.

## Ominaisuudet

- **Listaa kaikki henkilöt:** Saatavilla endpointissa `GET /api/persons`. Palauttaa kaikki puhelinluettelossa olevat henkilöt JSON-muodossa.
- **Näytä yksittäinen henkilö:** Saatavilla endpointissa `GET /api/persons/:id`. Palauttaa tietyn henkilön ID:n perusteella.
- **Lisää uusi henkilö:** Saatavilla endpointissa `POST /api/persons`. Lisää uuden henkilön puhelinluetteloon.
- **Poista henkilö:** Saatavilla endpointissa `DELETE /api/persons/:id`. Poistaa henkilön ID:n perusteella.
- **Näytä luettelon tiedot:** Saatavilla endpointissa `GET /info`. Näyttää puhelinluettelon henkilöiden lukumäärän ja pyyntöhetken ajan.

## Projektin rakenne

**src/**: Sisältää frontendin lähdekoodin. 

**dist/**: Sisältää tuotantoversion rakennustiedoston 'build' -komennon ajamisen jälkeen. 

### Vaatimukset

- [Node.js](https://nodejs.org/) (versio 14 tai uudempi)
- [npm](https://www.npmjs.com/) (yleensä asennettu Node.js:n mukana)


### Asennus

1. Kloonaa repositorio:

   ```bash
   git clone <repositoryn url>
   cd fullstackopen_ah_3_frontend
   ```
   

2. Asenna riippuvuudet:

   ```bash
   npm install
   ```
       

4. Kehitysympäristössä ajaminen

    ```bash
    npm run dev
    ```

Tämä käynnistää Vite-kehityspalvelimen


### Tuotantoversion rakentaminen

Frontendin tuotantoversion rakentaminen: 

```bash
npm run build
```


Tämä komento luo `dist/`-kansion, joka sisältää tuotantoversion. 


### Julkaisu

Muokkaukset frontendin puolella saadaan scriptien avulla Backendin puolelta seuraavilla komennoilla: 

   ```bash
   npm run build:ui
   ```

   Jonka avulla poistetaan backendistä olemassa oleva `dist`-hakemisto ja luodaan frontendin projektin puolella uusi tuotantoversio (`npm run buid`) sekä kopioidaan uusi `dist` -hakemisto backendin puolelle. 


ja

   ```bash
   npm run deploy:full
   ```

   Tämä komento Rakentaa frontendin tuotantoversion, lisää sen GitHubiin ja deployaa sen Renderiin