# Normes lingüístiques per a la traducció de programari al català

## Registre i to

- Registre formal però no pompós
- L'ordinador s'adreça a l'usuari en **vós** (plural de respecte): "Esteu segur?", "Introduïu el nom"
- L'usuari dóna ordres a l'ordinador en **imperatiu singular**: "Obre", "Desa", "Cancel·la"
- Evitar humanitzar l'ordinador: res de "Ho sento", "Gràcies per esperar", onomatopeies ("oh")
- Evitar expressions innecessàries: "simplement", "fàcilment", "només cal que"

## Verbs en elements UI

### Ordres (usuari → sistema)
Imperatiu singular: **"Obre"** (no "Obrir"), **"Desa"** (no "Guardar"), **"Imprimeix"**

### Missatges (sistema → usuari)
Vós: **"Esteu segur que voleu eliminar?"**, **"El document s'ha desat"**

### Gerundis anglesos ("-ing")
- "Loading" → "S'està carregant..." o "Carregant..."
- "Opening file" → "S'està obrint el fitxer" o "Obrint el fitxer"
- "en + infinitiu" per accions condicionals: "en llegir el fitxer" (no "al llegir")

### "May/might"
- Possibilitat → "pot": "El fitxer pot estar corromput"
- Probabilitat → "és possible que" + subjuntiu

## Gramàtica

### Ser vs. Estar
- Usar **"ser"** per a localització i amb adjectius d'estat: "La base de dades **és** buida" (no "està")
- "estar" és correcte per a estats temporals físics o processuals quan és inequívoc

### Negació doble
Obligatoria amb partícules negatives:
- "Cap ordre **no** s'ha d'escriure en majúscules" (no "cap ordre s'ha d'escriure")
- "Mai **no** s'ha de forçar el tancament" 
- "Ningú **no** pot accedir-hi"

### Possessius
Ometre quan el context és clar:
- ✅ "Voleu eliminar el fitxer?"
- ❌ "Voleu eliminar el vostre fitxer?"

### Gènere en llistes mixtes
Usar masculí (forma no marcada) per a grups mixts:
- "els fitxers i les carpetes **amagats**" (no "amagats/amagades")
- "els usuaris i les usuàries **registrats**" → millor "les persones **registrades**" o simplement "els usuaris registrats"

### Gènere neutre / genèric
Preferir formes genèriques: "tothom" (no "els desenvolupadors/les desenvolupadores"), "el personal", "la persona usuària"

### Preposicions
- **"per"** = agent/causa: "creat per l'usuari", "fallit per una errada"
- **"per a"** = propòsit/destinació: "eines per a programadors", "fitxer per al servidor"
- **"a"** per a moviment/destí: "anar a la carpeta", "desar a l'escriptori"
- **"en"** per a localització estàtica (abstracta): "en el menú", "en la llista"
- Formes curtes preferides: "damunt" (no "al damunt de"), "sota" (no "per sota de")

## Puntuació

### El·lipsis (...)
- Sense espai previ: "S'està carregant..." (no "S'està carregant ...")
- Al principi de frase, enganxat a la primera paraula: "...el nom del camp no pot ser buit"
- En botons que obren un diàleg: "Imprimeix..." (indica que hi ha més passos)

### Comes
- Ometre davant "i" o "o" en enumeracions simples: "Menús, barres d'eines i tecles"
- Obligatòria entre dues proposicions: "Feu clic al botó, i el fitxer s'obrirà"
- La coma va **dins** les cometes quan tanca una citació que ja porta coma

### Punt i coma
En llistes: els elements acaben en punt i coma, l'últim en punt. Si els elements són fragments breus sense verbe, no cal puntuació interna.

### Punt final
- En botons i etiquetes: **sense punt final**
- En missatges complets (frases amb verb): **amb punt final**
- En elements de llista que són frases complertes: **amb punt final**
- En elements de llista que són frases incompletes: **sense punt final**

### Dos punts
Quan introdueixen una llista o explicació, van seguits de minúscula (en català) si el que segueix és una llista: "Les opcions disponibles: fitxer, carpeta, vincle."

## Majúscules i minúscules

### Usar majúscula per a:
- Inici de frase i després de punt
- Noms propis (persones, llocs, empreses, marques)
- Sigles/acrònims: USB, HTML, PDF
- Primera lletra de noms de menú: "Fitxer", "Edita", "Visualitza"
- Primera lletra de títols de diàlegs: "Desa el document", "Preferències del sistema"
- Primer element d'una llista (fins i tot si és fragment)
- Paràmetres de línia d'ordres: "--gtk-module=MÒDUL"

### Usar minúscula per a:
- Noms de llengües: **català**, anglès, castellà
- Dies de la setmana i mesos: dilluns, gener
- Adjectius derivats de noms propis: "la interfície **gnòmica**"
- Elements d'una llista que no comencen frase (quan la llista és precedida per dos punts i els elements s'integren en el text)

## Sigles i acrònims

- Escriure en majúscules sense punts: **PC**, **USB**, **HTML**, **PDF**, **URL**
- Article determinat per gènere del concepte, no de l'acrònim: "**l'**HTML" (el llenguatge), "**el** PDF"
- Plural amb article, no afegint 's: "els PC" (no "els PC's" ni "els PCs")
- Primera menció d'acrònim poc conegut: forma completa en cursiva + traducció: "*Certificate Revocation List* (CRL, llista de revocació de certificats)"

## Abreviatures usuals en programari

| Abreviatura | Forma completa |
|-------------|----------------|
| etc. | etcètera |
| màx. | màxim |
| mín. | mínim |
| núm. | número |
| pàg. | pàgina |
| p. ex. | per exemple |
| fig. | figura |

## Veu activa vs. passiva

Preferir veu activa. Convertir passives quan és possible:
- ❌ "El fitxer és esborrat pel sistema" → ✅ "El sistema esborra el fitxer"
- ❌ "L'operació serà realitzada" → ✅ "El sistema realitza l'operació" o "L'operació es realitza"
- Passiva pronominal és acceptable: "El fitxer s'ha desat", "S'han trobat 3 errors"

## Barbarismes i castellanismes freqüents

| ❌ Evitar | ✅ Usar |
|-----------|---------|
| adreça IP (direcció) | adreça IP ✓ |
| guardar | desar |
| arrastrar | arrossegar |
| xarxa local (red local) | xarxa local ✓ |
| ha (preposició) | a |
| cerca/recerca confosos | cerca (acció), recerca (investigació) |
| apòstrof tipogràfic dret (') | apòstrof tipogràfic corbat (') |
| punt volat mal usat (·) | punt volat per a l·l: "col·leccions" |

## Errors gramaticals freqüents

| ❌ Error | ✅ Correcte |
|---------|------------|
| Hi han errors | Hi ha errors |
| Tenir que desar | Haver de desar / Cal desar |
| Donat que | Atès que |
| Doncs (causal) | Ja que / Perquè |
| En quant a | Quant a / Pel que fa a |
| Tals com | Com ara |
| estar a punt de | estar a punt de ✓ (és correcte!) |
| sí/si confosos | sí (afirm.) / si (condicional) |
