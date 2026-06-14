# Scroll Experience — Istruzioni

## Struttura del progetto

```
scroll-site/
├── index.html        ← Pagina principale
├── config.json       ← File di configurazione
├── assets/           ← Cartella per le immagini
│   ├── image_1.jpg
│   ├── image_2.jpg
│   └── image_3.jpg
└── README.md
```

## Configurazione (config.json)

### Cambiare i colori

```json
"css": {
  "primary": "#A41623",    ← colore primario (es. rosso)
  "onPrimary": "#FFFFFF"   ← colore a contrasto (es. bianco)
}
```

### Aggiungere/modificare sezioni

```json
"pageConfig": {
  "sections": [
    { "text": "Il tuo testo qui" },
    { "imagePath": "./assets/mia_foto.jpg" },
    { "text": "Altro testo..." }
  ]
}
```

Le sezioni alternano automaticamente testo e immagini.
Se un'immagine non viene trovata, viene mostrato un placeholder.

## Animazioni scroll

Le animazioni si attivano automaticamente grazie a CSS Scroll-Driven Animations.
- **Testo**: fade-in progressivo all'entrata in viewport
- **Immagini**: clip-path reveal dal basso + leggero effetto parallax

Compatibili con Chrome/Edge 115+, Firefox 110+. Su browser più vecchi il contenuto rimane visibile senza animazioni.
