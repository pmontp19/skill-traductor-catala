# Convencions de format per a la traducció de programari al català

## Tipografia i cometes

### Cometes catalanes (guillemets)
Usar **« »** (cometes baixes/llatines) com a cometes principals en català:
- Per citar text en anglès dins text català: «file not found»
- Per destacar paraules o expressions: el concepte «drag and drop»
- Per calcs o préstecs: la funció «commit»

Jerarquia de cometes per a cites niades:
1. Externes: « »
2. Internes: " "
3. Tercers nivell: ' '

Exemple: «El missatge diu "l'operació 'desar' ha fallat"»

### Cursiva
- Títols de taules i figures en documentació
- Formes estrangeres sense traducció establerta: el terme *workflow*
- Primera menció d'acrònims desconeguts: *Certificate Revocation List* (CRL)

### Negreta
- Termes clau o importants dins paràgrafs de documentació
- Paraules a les quals es vol cridar l'atenció: Feu clic a **Desa**

## Guions

### Guió curt (-) — dièresi composta
Per unir prefixos que acaben en vocal quan la paraula seguent comença en s, r, o x:
- "posa-ratolins" (no "posaratolins")
- "mini-servidor" quan hi ha ambigüitat

### Paraules prefixades: sense guió
La norma general és sense guió:
- antivirus (no anti-virus)
- microprogramari (no micro-programari)
- multimèdia (no multi-mèdia)
- programari (no progr-amari — evident, però per recordar la norma)

### Guió llarg (—) — em dash
Per a incises i parentètiques en documentació llarga. En UI de programari, rarament necessari.

## Llistat d'elements (llistes)

### Llista de frases completes
- Primera lletra en majúscula
- Punt final a cada element
- Exemple:
  - El sistema comprova la connexió.
  - Es descarrega el fitxer.
  - S'instal·la l'actualització.

### Llista de fragments o elements breus
- Primera lletra en majúscula
- Sense puntuació al final (o punt i coma si l'estil ho requereix)
- Exemple:
  - Fitxers de configuració
  - Certificats SSL
  - Permisos d'usuari

### Consistència
Quan una llista barreja frases completes i fragments, estandarditza-la a un sol tipus.

## Símbols i unitats

### Unitats de mesura (SI)
- Espai entre número i unitat: **10 MB**, **3,5 GB**, **100 Mbps**
- Símbols sense punt ni plural: kB, MB, GB, TB (no "MBs", no "MB.")
- Unitats del sistema internacional: metres, quilòmetres (no milles)
- Velocitat de transmissió: Mbps, Gbps (no MB/s per a velocitat de xarxa)

### Abreviatures de mides de fitxer
| Símbol | Valor |
|--------|-------|
| B | byte |
| kB | kilobyte (1.024 B) |
| MB | megabyte |
| GB | gigabyte |
| TB | terabyte |
| Kbps, Mbps, Gbps | velocitat (kilobits, megabits, gigabits per segon) |

### Moneda
Símbol **després** del número, amb espai: **1.000 €** (no "$1.000" ni "1000€")

## Elements de codi i tècnics

### Noms de fitxer, ruta, codi
Usar `font monoespaiada` per a:
- Noms de fitxers: `config.ini`, `index.html`
- Rutes: `/home/usuari/.config/`
- Ordres: `sudo apt update`
- Variables: `$HOME`, `%USERPROFILE%`
- Paràmetres: `--verbose`, `-h`

### Paràmetres de línia d'ordres
El nom del paràmetre en MAJÚSCULES si és un valor que l'usuari substitueix:
- `--output=FITXER`
- `--port=PORT`

### Marcadors de format (format strings)
No traduir mai marcadors de substitució:
- `%s`, `%d`, `%1$s` (Python, C)
- `{0}`, `{nom}` (.NET, Python format)
- `$(variable)` (shell)
- `__TERME__`, `{TERME}` (alguns sistemes)

## Tecles i dreceres de teclat

### Notació de tecles
Majúscula per a noms de tecla: **Ctrl**, **Alt**, **Maj**, **Retorn**, **Esc**

### Dreceres de teclat
Format: **Ctrl+S**, **Alt+F4**, **Ctrl+Maj+P**
- Signe `+` entre tecles, sense espais
- Cada tecla amb inicial majúscula
- Si una tecla és una lletra, en majúscula: **Ctrl+A**

### Seqüències de menú
Usar `>` o `→` per a camins de menú:
- Fitxer > Desa com a...
- Edita → Preferències → Avançat

## Puntuació en elements UI

### Botons
- Sense punt final: **Desa**, **Cancel·la**, **Accepta**
- Amb el·lipsis si obren diàleg: **Imprimeix...**, **Cerca...**
- Amb fletxa si obren submenú: **Avançat ▸**

### Etiquetes de camp
- Sense punt final
- Amb dos punts si l'etiqueta és davant d'un camp d'entrada: **Nom d'usuari:**

### Missatges emergents / tooltips
- Concís, imperatiu o nominal
- Sense punt final si és fragment; amb punt si és frase completa

### Barres de progrés / estats
- Gerundi: "S'està descarregant...", "Verificant..."
- O nominal: "Descàrrega en curs...", "Verificació..."

## Enllaços externs

Quan s'enllaça a contingut no en català, indicar la llengua entre parèntesis:
- [Documentació oficial](https://example.com) (en anglès)
- [Referència tècnica](https://example.com) (en castellà)
