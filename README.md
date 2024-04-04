# Julius AI-Conversatiebot

Dit document dient als handleiding voor het opzetten en gebruiken van de Julius Conversatiebot webpagina. Deze bot is ontworpen om gebruikers te betrekken bij een interactieve, gesproken conversatie met een digitale AI, gepositioneerd als een historisch figuur uit de Romeinse tijd.

## Vereisten

Om deze bot te kunnen gebruiken, dien je over een moderne webbrowser te beschikken die JavaScript ondersteunt. Daarnaast is een werkende microfoon nodig voor het opnemen van berichten. Bovendien dien je eigen API-keys te hebben voor OpenAI (GPT en Whisper) en ElevenLabs Text-to-Speech API's.

## Installatie en Gebruik

Om Julius Conversatiebot werkend te krijgen, moet je enkele essentiële configuraties uitvoeren met betrekking tot API-keys en voice settings.

### API-keys Toevoegen

Je dient je eigen API-keys te verkrijgen voor de volgende diensten:

- **OpenAI (GPT en Whisper)**: Registreren en API-key aanvragen via [OpenAI](https://openai.com/).
- **ElevenLabs Text-to-Speech**: Registreren en API-key aanvragen via [ElevenLabs](https://www.elevenlabs.io/).

Na verkrijging dien je de API-keys toe te voegen aan de JavaScript-code waar de volgende constanten staan:

- `const OPEN_AI_API_KEY = "jouw_OpenAI_API_key";`
- `const ELABS_API_KEY = "jouw_ElevenLabs_API_key";`

### Voice Settings en Voice ID

Binnen ElevenLabs dien je een `voice_id` te verkrijgen. Dit kun je doen door de beschikbare stemmen te bekijken en een keuze te maken die het beste bij je toepassing past. De `voice_id` voeg je dan als volgt toe aan de constante:

- `const ELABS_VOICE_ID = "jouw_ElevenLabs_voice_id";`

Daarnaast kun je de voice instellingen (`voice_settings`) aanpassen om de spraakuitvoer te optimaliseren. Deze instellingen omvatten:

- `stability`: Beïnvloedt de stabiliteit van de gesproken output.
- `similarity_boost`: Beïnvloedt hoe nauw de uitvoer overeenkomt met de stem van de gekozen voice_id.
- `style`: Stijlindex (als ondersteund door de gekozen stem) om variaties in spraakpatronen aan te brengen.
- `use_speaker_boost`: Versterkt de gelijkenis met de gekozen stem.

Voorbeeld:

```javascript
const ELABS_VOICE_SETTINGS = {
  stability: 0.35,
  similarity_boost: 0.75,
  style: 0,
  use_speaker_boost: false,
};
```

De `voice_settings` kunnen worden aangepast afhankelijk van je specifieke behoeften en de kenmerken van de gekozen stem.

### Hoe te beginnen

- **Starten**: Klik op de startknop om te beginnen. De startknop verdwijnt en de instructietekst wordt zichtbaar.
- **Praten**: Spreek na het zien van de rode opname-indicator. Druk op de spatiebalk wanneer je klaar bent met je bericht.
- **Antwoord afwachten**: Julius zal na het verwerken van je spraakbericht antwoorden. Het antwoord wordt omgezet in spraak en afgespeeld.

### Technische Details

- **Microfoontoegang**: De pagina vraagt toegang tot de microfoon om spraakopname mogelijk te maken.
- **Speech-to-Text & Text-to-Speech**: Spraak wordt omgezet naar tekst en verwerkt. Julius' antwoord wordt vervolgens omgezet van tekst naar spraak en afgespeeld.
- **Dynamische Verandering**: Afhankelijk van het volume van de spraak, zal het beeld van Julius veranderen om visueel aan te duiden dat hij praat.

## Externe Bibliotheken

- **lamejs** wordt gebruikt voor het converteren van audio naar MP3.
- **axios** wordt ingezet voor het uitvoeren van API-verzoeken.

## Licentie

Deze software valt onder de BSD-licentie. Zie het [LICENSE](LICENSE) bestand voor de volledige licentievoorwaarden.

## Bijdragen

Bijdragen aan deze code of suggesties voor verbeteringen zijn altijd welkom. Zorg er wel voor dat alle aanpassingen netjes gedocumenteerd zijn en voldoen aan de gestelde licentievoorwaarden.

## Contact

Voor vragen of opmerkingen kunt u contact opnemen met de ontwikkelaar: Youp Verkooijen.

## Disclaimer

Deze software wordt geleverd "zoals hij is", zonder garanties. Zie het [LICENSE](LICENSE) bestand voor de volledige disclaimer.

---

**Let op**: Het gebruik van AI en spraakherkenning kan onverwachte resultaten opleveren. Het is belangrijk om altijd gezond verstand te gebruiken bij interactie met Julius.
