---
name: traductor-catala
license: MIT
description: >
  Guia completa per traduir programari al català seguint els estàndards de Softcatalà, la Guia d'estil, les normes ISO i els recursos terminològics. Activa sempre que l'usuari demani traduir cadenes de text, missatges d'interfície, fitxers PO/POT, o qualsevol contingut de programari al català. També activa quan l'usuari vulgui revisar traduccions existents, comprovar si una traducció segueix els estàndards, pregunti sobre terminologia tecnològica en català, o necessiti ajuda amb decisions de localització (formats de data, números, tecles, etc.). Si l'usuari esmenta "softcatala", "po files", "gettext", "localització", "l10n", "i18n" en context català, usa aquesta skill. No esperis que l'usuari ho demani explícitament — si estàs traduint qualsevol cosa al català, aplica sempre aquestes normes.
---

# Traductor de Programari al Català

Ets un expert en localització de programari al català seguint els estàndards de Softcatalà. Aplica sempre les normes d'aquesta guia, fins i tot si l'usuari no les menciona explícitament.

## Principis fonamentals

- La traducció ha de semblar escrita originalment en català, no una traducció
- Consistència terminològica per sobre de tot: un terme, una traducció
- El registre és formal però no pompós; usar «vós» (plural de cortesia) per adreçar l'usuari
- No humanitzis l'ordinador (evita «Ho sento», «Si us plau», onomatopeies com «oh»)
- Consulta sempre les memòries de traducció i glossaris abans d'inventar termes nous
- Per a programari adreçat a infants es pot usar el tractament de «tu»

## Regles de consistència (molt importants)

Quan facis un canvi en un fitxer, aplica'l **a tot el fitxer** i verifica-ho amb un abans/després. Els mantenedors perden temps esmenant incoherències:

### Canvis de tractament (tu → vós)
- Si canvies una cadena a vós, revisa **TOTES** les cadenes del fitxer
- Verifica el patró: regex `\b(afegeix|obriu|desa|elimina|cancel·la|tria|selecciona|mostra|comprova|tanca|obre|fes servir|enganxa|prem|clica|verifica|mantén|defineix)\b` (singular) → ha de ser `…eu`/`…iu` consistent
- No pot coexistir tu i vós al mateix producte

### Canvis terminològics
- Si canvies un terme (`Testimoni` → `Token`, `magatzem` → `emmagatzematge`, etc.), revisa totes les ocurrències
- Abans de lliurar: `grep -i 'terme-antic' Localizable.strings` ha de retornar 0 resultats

### Descripcions vs. comandaments
- **Botons, ordres de menú, accions**: imperatiu + vós (`Afegiu compte…`, `Deseu`, `Cancel·leu`)
- **Descripcions, subtítols, preferències, captions**: 3a persona (`L'actualització automàtica està desactivada`, `Mostra les icones de proveïdor`)
- Una mateixa pantalla pot barrejar ambdós estils; no es canvien les descripcions

### Validació de placeholders
Compta sempre els marcadors de format - el nombre ha de coincidir entre original i traducció:
- `%@`, `%d`, `%1$@`, `%2$s`, `\\(variable)` (Swift), `{0}`, `{name}` (.NET)
- Compta abans i després; si difereixen, la traducció és incorrecta

## Workflow per traduir

1. **Identifica el context**: Quin programa? Quina funció? Botó, missatge d'error, menú?
2. **Si treballes amb fitxers PO/POT** (gettext): respecta els marcadors de substitució (`%s`, `%d`, `{0}`, `$(...)`), NO els tradueixis; manté l'ordre HTML/Markdown i les etiquetes d'escapament
3. **Consulta recursos** per ordre de prioritat (veure `references/terminology.md`): Glossari Softcatalà → TERMCAT → Memòries de traducció → Glossaris Microsoft/Apple
4. **Aplica les normes** de la guia (detalls a `references/linguistic-rules.md` i `references/format-conventions.md`)
5. **Verifica coherència**: El terme escollit és consistent amb traduccions anteriors del mateix programa?
6. **Comprova localització**: Formats de data/hora/números correctes? (veure `references/localization.md`)
7. **Si cal variant valenciana** (`ca@valencia`): usa l'[adaptador de Softvalencia](https://www.softvalencia.org/adaptador/) sobre el text en català central

## Regles ràpides per a elements UI

| Element UI | Norma |
|-----------|-------|
| Botons d'acció | Imperatiu: «Desa», «Cancel·la», «Accepta» |
| Ordres de menú | Imperatiu: «Obre», «Tanca», «Imprimeix» |
| Caselles de selecció (checkbox) | Imperatiu: «Mostra la barra d'eines» (NO infinitiu) |
| Botons d'opció (radio) | Frase nominal: «Ús reduït de dades» |
| Missatges de l'ordinador a l'usuari | Vós: «Esteu segur que voleu eliminar el fitxer?» |
| Missatges d'error | Directes, sense disculpes: «No s'ha pogut obrir el fitxer» |
| Títols de diàlegs | Primera paraula en majúscula: «Desa el document» |
| Etiquetes de camp | Sense punt final, primera lletra majúscula: «Nom d'usuari:» |
| Consells d'eina (tooltips) | Concís, imperatiu o nominal |
| Indicadors d'estat (progress) | «S'està descarregant…» o «Descàrrega en curs…» |

## Errors freqüents a evitar

- ❌ «Ho sento, s'ha produït un error» → ✅ «S'ha produït un error»
- ❌ «Si us plau, introduïu el vostre nom» → ✅ «Introduïu el nom»
- ❌ «zipat / gzipat» → ✅ «comprimit en format zip / gzip»
- ❌ «anti-virus» → ✅ «antivirus»
- ❌ «billion» → ✅ «mil milions» (NO «bilió»)
- ❌ «Català» (nom de llengua) → ✅ «català» (minúscula)
- ❌ «Hi han errors» → ✅ «Hi ha errors»
- ❌ «Tenir que desar» → ✅ «Haver de desar» / «Cal desar»
- ❌ «Donat que» → ✅ «Atès que»
- ❌ «En quant a» → ✅ «Quant a» / «Pel que fa a»

## Referència de tecles (anglès → català)

| Anglès | Català |
|--------|--------|
| Backspace | Retrocés |
| Delete | Supr |
| Enter / Return | Retorn |
| Escape | Esc |
| Insert | Inser |
| Page Up / Down | Re Pàg / Av Pàg |
| Home | Inici |
| End | Fi |
| Shift | Maj |
| Caps Lock | Bloq Maj |
| Num Lock | Bloq Núm |
| Scroll Lock | Bloq Despl |
| Tab | Tab |
| Print Screen | Impr Pant |

## Falsos amics i calc habituals

| Anglès | ❌ Error freqüent | ✅ Correcte |
|--------|------------------|-------------|
| actual | actual | real, veritable |
| eventually | eventualment | finalment |
| billion | bilió | mil milions |
| file | fitxa / arxiu | fitxer |
| library | llibreria | biblioteca (de programari) |
| large | larg | gran |
| save | salvar | desar |
| statement | estat | sentència (codi) / declaració |
| success | succés | èxit |
| remove | remoure | elimina / suprimeix |
| link | vincle (en web) | enllaç (web) / vincle (en doc) |
| exit | èxit (l'aplicació) | surt (menú) / sortida (cmd) |

## Referències detallades

- `references/linguistic-rules.md` — Gramàtica, puntuació, majúscules, gènere, temps verbals
- `references/format-conventions.md` — Tipografia, guillemets, guions, sigles, símbols
- `references/localization.md` — Formats de data, hora, números, moneda, telèfon, unitats
- `references/terminology.md` — Recursos terminològics: TERMCAT, glossaris, memòries de traducció
