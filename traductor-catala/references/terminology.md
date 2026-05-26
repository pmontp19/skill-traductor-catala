# Recursos terminològics per a la traducció de programari al català

## Principi de consistència

**Una sola traducció per a cada terme**. La inconsistència (p. ex. usar "D'acord", "Accepta" i "Bé" indistintament per "OK") trenca la coherència de la interfície. Decideix un terme i usa'l sempre.

Quan s'estableix un terme per a un projecte, **documenta'l** i consulta les traduccions anteriors del mateix projecte abans de decidir.

## Fonts de consulta per ordre de prioritat

### 1. Glossari de Softcatalà (primera consulta)
- **HTML navegable**: https://static.softcatala.org/terminology/sc-glossary/
- **CSV descarregable**: https://static.softcatala.org/terminology/sc-glossary.csv
- Extret automàticament de les traduccions de Softcatalà
- Cobreix terminologia de programari lliure i codi obert

### 2. Glossari complet de programari lliure
- Cobreix tots els projectes amb memòries de traducció
- Mateixa URL base, fitxer diferent (CSV disponible)
- Útil per a termes específics d'ecosistemes com GNOME, KDE, LibreOffice

### 3. TERMCAT — Centre de Terminologia
- Web: https://www.termcat.cat/
- **Cercaterm**: motor de cerca de terminologia catalana oficial
- **Neoloteca** (2000–2010): neologismes tecnològics aprovats
- Font autoritzada per a termes nous o dubtosos
- Si el terme hi és, usar la forma de TERMCAT tret que Softcatalà hagi establert una alternativa

### 4. Memòries de traducció de Softcatalà
- Web: https://www.softcatala.org/recursos/memories/
- 306 projectes, ~14,3 milions de paraules traduïdes
- Formats disponibles: **PO** (Portable Object) i **TMX** (Translation Memory eXchange)
- Útil per veure com s'ha traduït un terme en context real
- Integrable a OmegaT, memoQ, Weblate, Poedit

### 5. Glossaris de Microsoft
- Disponibles gratuïtament per a traducció de productes Microsoft
- Útil per a termes que Microsoft ha establert en català
- Coherència amb l'ecosistema Windows

### 6. Glossaris d'Apple
- Accessibles a desenvolupadors registrats d'Apple
- Per a apps iOS/macOS, seguir la terminologia d'Apple quan escau

## Com accedir a les memòries de traducció

### Descàrrega individual per projecte
Cada projecte a https://www.softcatala.org/recursos/memories/ té:
- Enllaç de descàrrega TMX (`.tmx.zip`)
- Enllaç de descàrrega PO (`.po.zip` o carpeta `.tar.gz`)

### Col·leccions agregades
- **Totes les memòries**: ~10,5 milions de paraules
- **Només projectes Softcatalà**: ~2,78 milions de paraules (qualitat més controlada)

### Ús amb eines de traducció
- **OmegaT**: afegir fitxers TMX a la carpeta `tm/` del projecte
- **Weblate**: importar TMX des de l'administració del projecte
- **Poedit**: els fitxers PO es poden usar directament

### Ús programàtic (per a agents IA)
Per usar les memòries en un agent de traducció:
1. Descarregar el TMX zip des de la URL del projecte
2. Descomprimir: `unzip projecte.tmx.zip`
3. Parsejar el XML (TMX és XML estàndard):
   ```xml
   <tu>
     <tuv xml:lang="en"><seg>File not found</seg></tuv>
     <tuv xml:lang="ca"><seg>No s'ha trobat el fitxer</seg></tuv>
   </tu>
   ```
4. Indexar per segment source per a cerca eficient

## Termes tecnològics recomanats

### Termes d'UI generals
| Anglès | Català recomanat | Notes |
|--------|-----------------|-------|
| OK | D'acord / Accepta | "D'acord" en diàlegs; "Accepta" en preferències |
| Cancel | Cancel·la | Amb punt volat |
| Apply | Aplica | |
| Close | Tanca | |
| Open | Obre | |
| Save | Desa | NO "guarda" ni "salva" |
| Save As | Desa com a | |
| New | Nou/Nova | Acord en gènere |
| Edit | Edita | (menú); "edita" (botó) |
| Delete | Elimina / Suprimeix | "Elimina" per a elements; "Suprimeix" per a contingut |
| Print | Imprimeix | |
| Find | Cerca | NO "busca" |
| Replace | Substitueix | |
| Help | Ajuda | |
| Settings / Preferences | Configuració / Preferències | "Configuració" per a sistema; "Preferències" per a app |
| File | Fitxer | NO "arxiu" (fals amic del castellà) |
| Folder / Directory | Carpeta / Directori | "Carpeta" en UI; "directori" en terminal |
| Copy | Copia | |
| Cut | Retalla | |
| Paste | Enganxa | |
| Undo | Desfés | |
| Redo | Refés | |
| Select All | Selecciona-ho tot | |
| Refresh | Actualitza | |
| Update | Actualitza | |
| Install | Instal·la | Amb punt volat |
| Uninstall | Desinstal·la | |
| Download | Descarrega | |
| Upload | Puja | (al servidor) |
| Log in / Sign in | Inicia la sessió | |
| Log out / Sign out | Tanca la sessió | |
| Register | Registra't | |
| Password | Contrasenya | |
| Username | Nom d'usuari | |
| Search | Cerca | |
| Filter | Filtra | |
| Sort | Ordena | |
| View | Vista / Visualitza | "Vista" com a nom; "visualitza" com a verb |
| Tools | Eines | |
| Window | Finestra | |
| Tab | Pestanya | |
| Menu | Menú | |
| Toolbar | Barra d'eines | |
| Status bar | Barra d'estat | |
| Sidebar | Barra lateral | |
| Panel | Tauler | |

### Missatges del sistema
| Anglès | Català recomanat |
|--------|-----------------|
| File not found | No s'ha trobat el fitxer |
| Access denied | Accés denegat |
| Operation completed | L'operació s'ha completat |
| Error occurred | S'ha produït un error |
| Loading... | S'està carregant... |
| Saving... | S'està desant... |
| Please wait... | Espereu... |
| No items found | No s'ha trobat cap element |
| Are you sure? | Esteu segur? |
| This action cannot be undone | Aquesta acció no es pot desfer |

### Termes de programació / dev
| Anglès | Català |
|--------|--------|
| Repository | Repositori |
| Branch | Branca |
| Commit | Comissió (tècnic) / *commit* (en context dev) |
| Pull request | Sol·licitud d'incorporació |
| Bug | Error / Defecte |
| Feature | Funcionalitat |
| Release | Versió / Llançament |
| Deploy | Desplegament / Desplegar |
| Build | Compilació / Construir |
| Debug | Depurar / Depuració |
| Log | Registre |
| Cache | Memòria cau |
| Thread | Fil d'execució |
| Process | Procés |
| Library | Biblioteca |
| Framework | Marc de treball (o *framework* si no hi ha alternativa clara) |
| API | API (no traduir) |
| Interface | Interfície |
| Database | Base de dades |
| Query | Consulta |
| Server | Servidor |
| Client | Client |
| Request | Sol·licitud / Petició |
| Response | Resposta |

## Quan no hi ha traducció establerta

1. Consultar en ordre: glossari Softcatalà → TERMCAT → Microsoft/Apple glossaries
2. Si no hi ha terme, proposar-ne un de nou a la llista de correu de terminologia de Softcatalà
3. Mentre s'espera, usar el terme anglès en cursiva: *drag and drop*
4. No inventar neologismes evidents com "zipat", "gzipat", "pinged" — usar descripcions: "comprimit en format zip"

## Llista de correu de terminologia

Per a dubtes terminològics i propostes de termes nous:
- Llista de Softcatalà per a terminologia (consultar la web de Softcatalà per a l'adreça actual)
- Aportar: el terme anglès, context d'ús, proposta de traducció amb raonament
