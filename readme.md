# Inventaire des logiciels libres
## Gouvernement du Québec

Inventaire 2017 des logiciels libres utilisés dans l'administration publique québécoise

Disponible à l'interne: <https://di.collaboration.gouv.qc/bibliotheque/documents/2018/03/inventaire-des-logiciels-libres>

## Visualisation des données
Quelques graphiques sont disponibles. Voir cette [démonstration préliminaire](https://src-yusucsprbo.now.sh/).

## Extraction des données
Le [script d'extraction de données](https://github.com/millette/ll-gouv-qc) à partir du PDF génère la structure suivante:

```
[
  {
    "type": "Accès et contrôle de poste de travail à $
    "nom": "Putty",
    "installations": "500+",
    "low": 500,
    "high": 1000,
    "org": "Centre de services partagés du Québec"
  },
  {
    "type": "Accès et contrôle de poste de travail à $
    "nom": "Putty",
    "installations": "500+",
    "low": 500,
    "high": 1000,
    "org": "Revenu Québec"
  },
  ...
]
```

# Vega demo

[Vega][] is a visualization grammar, a declarative language for creating, saving, and sharing interactive visualization designs. With Vega, you can describe the visual appearance and interactive behavior of a visualization in a JSON format, and generate web-based views using Canvas or SVG.

veeg will generate this file structure:

```
src
├── css
│   ├── main.css
│   └── normalize.css
├── data
│   ├── data.json
│   ├── spec.json
│   └── spec-lite.json
├── js
│   ├── vendor
│   │   ├── jquery-3.2.1.min.js
│   │   └── modernizr-3.5.0.min.js
│   ├── main.js
│   └── plugins.js
├── favicon.ico
├── humans.txt
├── icon.png
├── index.html
├── LICENSE.txt
└── site.webmanifest
```

Based on [html5-boilerplate][]. Vega resources are found in ```data/``` and its JavaScript code in ```src/js/main.js```.

## Available scripts
Lint JavaScript code with [standardjs][]:
```
yarn lint
```

Launch development web server with [browser-sync][]:
```
yarn dev
```
Your site should be available at <http://localhost:3000/>.

Convert Vega-Lite spec to Vega with [Vega-Lite][]:
```
yarn vl2vg
```

[html5-boilerplate]: <https://github.com/h5bp/html5-boilerplate>
[standardjs]: <https://standardjs.com/>
[browser-sync]: <https://browsersync.io/>
[Vega-Lite]: <https://vega.github.io/vega-lite/>
[Vega]: <https://vega.github.io/vega/>
