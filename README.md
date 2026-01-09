# DirtyTag Photo QC

Web application per il Quality Control delle foto e configurazione migrazione inventario legacy.

![DirtyTag](assets/logo.png)

---

## 🔗 Accesso

**URL:** [https://federicoluigidorsi.github.io/](https://federicoluigidorsi.github.io/)

---

## 📋 Funzionalità

- ✅ Visualizzazione foto per SKU da Google Drive
- ✅ Selezione FRONT/BACK con click o tastiera
- ✅ Configurazione AI Mode (MANI / WORN / FLAT)
- ✅ Selezione Template per modalità FLAT
- ✅ Scelta piattaforme target (Vinted, Vestiaire, Catawiki)
- ✅ Progress tracking in tempo reale
- ✅ Zoom foto per dettagli
- ✅ Keyboard shortcuts per velocità

---

## ⌨️ Scorciatoie Tastiera

| Tasto | Azione |
|-------|--------|
| `F` | Seleziona foto come FRONT |
| `B` | Seleziona foto come BACK |
| `Enter` | Conferma e prossimo SKU |
| `Esc` | Chiude zoom foto |

---

## 🔧 Configurazione

### Token Airtable

Per utilizzare l'app è necessario un token Airtable con accesso alla base DirtyTag 2.0.

1. Vai su [airtable.com/create/tokens](https://airtable.com/create/tokens)
2. Crea un nuovo token con:
   - **Scopes:** `data.records:read`, `data.records:write`
   - **Access:** Base DirtyTag 2.0
3. Copia il token e inseriscilo al login

> Il token viene salvato localmente nel browser.

---

## 🔄 Flusso Operativo

```
1. Login con token
       ↓
2. Visualizza foto SKU
       ↓
3. Seleziona FRONT + BACK
       ↓
4. Configura AI Mode / Template / Piattaforme
       ↓
5. Conferma
       ↓
6. Prossimo SKU (automatico)
```

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (vanilla)
- **Font:** Roboto Mono (Google Fonts)
- **API:** Airtable REST API
- **Storage:** Google Drive (thumbnails)
- **Hosting:** GitHub Pages

---

## 📁 Struttura

```
FedericoLuigiDOrsi.github.io/
├── index.html          # Web App principale
├── assets/
│   └── logo.png        # Logo DirtyTag
└── README.md           # Questo file
```

---

## 🔗 Link Correlati

- **Documentazione Sistema:** [dirtytag-system/docs](https://github.com/FedericoLuigiDOrsi/dirtytag-system/tree/main/docs)
- **Workflow n8n:** [dirtytag-system/workflows](https://github.com/FedericoLuigiDOrsi/dirtytag-system/tree/main/workflows)
- **Manuale Operatore:** [OPERATOR_MANUAL.md](https://github.com/FedericoLuigiDOrsi/dirtytag-system/blob/main/docs/OPERATOR_MANUAL.md)

---

## 📊 Tabelle Airtable Coinvolte

| Tabella | Base | Uso |
|---------|------|-----|
| PHOTO_CANDIDATES | DirtyTag 2.0 | Lettura foto da revieware |
| OLD_INVENTORY | DirtyTag 2.0 | Scrittura configurazione migrazione |

---

## 🐛 Troubleshooting

### Le foto non si caricano
- Verifica connessione internet
- Controlla validità token Airtable
- Ricarica pagina (F5)

### Errore durante salvataggio
- Verifica che il token abbia permessi di scrittura
- Controlla che i campi Airtable esistano

### Nessuno SKU da processare
- Tutti gli SKU sono stati completati
- Eseguire W0.5_OLD_AUDITOR per nuovi SKU

---

## 📄 Licenza

Proprietario: DirtyTag © 2025

---

## 👤 Autore

Federico Luigi D'Orsi
