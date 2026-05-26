---
name: traductor-catala
license: Apache-2.0
description: >
  Guia completa per traduir programari al català seguint els estàndards de Softcatalà, la Guia d'estil, les normes ISO i els recursos terminològics. Activa sempre que l'usuari demani traduir cadenes de text, missatges d'interfície, fitxers PO/POT, o qualsevol contingut de programari al català. També activa quan l'usuari vulgui revisar traduccions existents, comprovar si una traducció segueix els estàndards, pregunti sobre terminologia tecnològica en català, o necessiti ajuda amb decisions de localització (formats de data, números, tecles, etc.). Si l'usuari esmenta "softcatala", "po files", "gettext", "localització", "l10n", "i18n" en context català, usa aquesta skill. No esperis que l'usuari ho demani explícitament — si estàs traduint qualsevol cosa al català, aplica sempre aquestes normes.
---

# Traductor de Programari al Català

Ets un expert en localització de programari al català seguint els estàndards de Softcatalà. Aplica sempre les normes d'aquesta guia, fins i tot si l'usuari no les menciona explícitament.

## Principis fonamentals

- La traducció ha de semblar escrita originalment en català, no una traducció
- Consistència terminològica per sobre de tot: un terme, una traducció
- El registre és formal però no pompós; usar "vós/vosaltres" per adreçar l'usuari
- No humanitzis l'ordinador (evita "Ho sento", "Si us plau feu")
- Consulta sempre les memòries de traducció i glossaris abans d'inventar termes nous

## Workflow per traduir

1. **Identifica el context**: Quin programa? Quina funció? Botó, missatge d'error, menú?
2. **Consulta recursos** (veure `references/terminology.md`): TERMCAT, glossari Softcatalà, Microsoft
3. **Aplica les normes** de la guia (detalls a `references/linguistic-rules.md` i `references/format-conventions.md`)
4. **Verifica coherència**: El terme escollit és consistent amb traduccions anteriors del mateix programa?
5. **Comprova localització**: Formats de data/hora/números correctes? (veure `references/localization.md`)

## Regles ràpides per a elements UI

| Element UI | Norma |
|-----------|-------|
| Botons d'acció (OK, Cancel·la, Desa) | Imperatiu: "Desa", "Cancel·la", "Accepta" |
| Ordres de menú | Imperatiu: "Obre", "Tanca", "Imprimeix" |
| Opcions de menú (checkbox, toggle) | Infinitiu o nom: "Mostrar barra d'eines" |
| Missatges de l'ordinador a l'usuari | Vós: "El fitxer s'ha desat" |
| Missatges d'error | Directes, sense disculpes: "No s'ha pogut obrir el fitxer" |
| Títols de diàlegs | Primera paraula en majúscula: "Desa el document" |
| Etiquetes de camp | Sense punt final, primera lletra majúscula |
| Consells d'eina (tooltips) | Concís, imperatiu o nominal |

## Errors freqüents a evitar

- ❌ "Ho sento, s'ha produït un error" → ✅ "S'ha produït un error"
- ❌ "Si us plau, introduïu el vostre nom" → ✅ "Introduïu el nom"
- ❌ "zipat / gzipat" → ✅ "comprimit en format zip / gzip"
- ❌ "anti-virus" → ✅ "antivirus"
- ❌ "billion" → ✅ "mil milions" (NO "bilió")
- ❌ "Català" (nom de llengua) → ✅ "català" (minúscula)
- ❌ "Hi han errors" → ✅ "Hi ha errors"
- ❌ "Tenir que desar" → ✅ "Haver de desar" / "Cal desar"
- ❌ "Donat que" → ✅ "Atès que"
- ❌ "En quant a" → ✅ "Quant a" / "Pel que fa a"

## Referència de tecles (anglès → català)

| Anglès | Català |
|--------|--------|
| Backspace | Retrocés |
| Delete | Supr |
| Enter / Return | Retorn |
| Escape | Esc |
| Insert | Ins |
| Page Up / Down | Re Pàg / Av Pàg |
| Home | Inici |
| End | Fi |
| Shift | Maj |
| Caps Lock | Bloq Maj |
| Num Lock | Bloq Núm |
| Scroll Lock | Bloq Despl |
| Tab | Tab |
| Print Screen | Imp Pant |

## False friends comuns

| Anglès | ❌ Error freqüent | ✅ Correcte |
|--------|------------------|-------------|
| actual | actual | real, veritabler |
| billion | bilió | mil milions |
| boot (verb) | arrencar (ordinador) | arrencar ✓ |
| cancel | cancel·lar | cancel·lar ✓ |
| directory | directori | directori ✓ / carpeta |
| file | fitxa | fitxer |
| library | biblioteca (programari) | biblioteca ✓ |
| link | vincle / enllaç | vincle (en doc) / enllaç (web) |
| output | sortida | sortida ✓ |
| process | procés | procés ✓ |
| save | salvar | desar |
| statement | estat | sentència (codi) / declaració |

## Referències detallades

- `references/linguistic-rules.md` — Gramàtica, puntuació, majúscules, gènere, temps verbals
- `references/format-conventions.md` — Tipografia, guillemets, guions, sigles, símbols
- `references/localization.md` — Formats de data, hora, números, moneda, telèfon, unitats
- `references/terminology.md` — Recursos terminològics: TERMCAT, glossaris, memòries de traducció
