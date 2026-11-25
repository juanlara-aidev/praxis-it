# Praxis — Edizione Italiana

Ciao, sono **Juan**. Ho creato Praxis perché quando apri il tuo editor e vuoi costruire un progetto SaaS, lo abbia pronto in meno di un minuto, senza litigare con la configurazione.

Questa è l'**edizione italiana**: l'interfaccia e tutti i contenuti che Praxis inietta nel tuo progetto (la metodologia, le Skills, i template) sono in italiano. Il tuo agente di Claude Code lavora in italiano insieme a te.

> ¿Parli spagnolo? C'è anche l'edizione in spagnolo: [juanlara-aidev/praxis](https://github.com/juanlara-aidev/praxis).

---

## Cos'è Praxis

Praxis è un'estensione per **VS Code** (funziona anche su Cursor, Windsurf e Antigravity) che:

- Inietta uno **stack completo** Next.js + Supabase + Tailwind + AI SDK in un progetto vuoto, già pronto.
- Aggiunge la **metodologia agentica** (`.claude/` con Skills, hook e template di PRP) che trasforma il tuo editor in un sistema di produzione di software con Claude Code.
- Gestisce le tue **Skills** e i tuoi **MCP** da una barra laterale, con un click.

Tu dici **cosa** vuoi costruire. L'agente decide **come**.

---

## Usi Codex, GLM o DeepSeek?

Praxis mantiene lo stesso contratto del progetto quando li avvii da Launchpad: istruzioni portabili, Skills e MCP autorizzati in `.mcp.json`. GLM e DeepSeek aprono il **pannello visuale di Claude Code** già configurato per quel modello (la tua chiave resta cifrata nell'editor, mai nel tuo progetto); Codex apre il suo terminale con le stesse connessioni. Non vengono modificati i file globali dei tuoi agenti e Doctor segnala una connessione incompatibile senza mostrare segreti.

---

## Come si installa

Apri il terminale del tuo editor (oppure il terminale del tuo sistema) e incolla **una** di queste righe, a seconda del tuo sistema:

**macOS / Linux**
```bash
curl -fL -o /tmp/praxis.vsix "https://github.com/juanlara-aidev/praxis-it/releases/latest/download/praxis.vsix" && code --install-extension /tmp/praxis.vsix --force
```

**Windows (PowerShell)**
```powershell
$tmp="$env:TEMP\praxis.vsix"; iwr "https://github.com/juanlara-aidev/praxis-it/releases/latest/download/praxis.vsix" -OutFile $tmp; code --install-extension $tmp --force
```

**Windows (cmd)**
```cmd
curl -fL -o "%TEMP%\praxis.vsix" "https://github.com/juanlara-aidev/praxis-it/releases/latest/download/praxis.vsix" && code --install-extension "%TEMP%\praxis.vsix" --force
```

> Usi **Cursor**, **Windsurf** o **Antigravity**? Sostituisci `code` con `cursor`, `windsurf` o `antigravity` nel comando.

Quando finisce, ricarica la finestra: `Cmd/Ctrl+Shift+P` → **Ricarica la finestra**. Vedrai l'icona di Praxis nella barra laterale.

---

## Come si aggiorna

Aggiornare è **eseguire lo stesso comando un'altra volta**. Oppure premi il pulsante **Aggiorna** nella barra laterale di Praxis: apre un terminale con il comando già pronto. Niente di più.

---

## Profili account: lavora con l’account IA di ogni cliente

Se lavori per più clienti e ognuno ha il suo account di Claude o di Codex, un **profilo** ti permette di usare quello di ciascuno senza mescolarli. Il lavoro di un cliente consuma l’account del cliente e il tuo continua a consumare il tuo. Le tue Skills, le tue impostazioni e la cronologia delle sessioni sono condivise tra i profili, quindi non devi riconfigurare niente.

Se non crei nessun profilo, non cambia nulla: Praxis si vede e funziona come sempre, con il tuo account di sempre (compare come **Predefinito**).

Un profilo cliente usa l’account IA del cliente, ma **non i suoi connettori né le sue app** (Gmail, Drive, Calendar, Notion… del suo Claude o del suo ChatGPT). Non vengono caricati dentro il suo profilo, così non vedi né tocchi cose sue per sbaglio. I connettori del tuo account restano nel tuo profilo predefinito.

### Come creare un profilo

1. Apri il menu **⋯** del pannello di Praxis e scegli **Account IA…**.
2. Scegli **Crea profilo…** e dagli il nome del cliente. Usa lettere e numeri, almeno 2 caratteri.
3. Fatto. In alto nel pannello compare un pulsante con l’iniziale del profilo. Da lì si fa tutto il resto.

### Come avviare la sessione del cliente

Apri il pulsante del profilo e scegli **Accedi a Claude** o **Accedi a Codex**:

- **Claude**: Praxis ti mostra un link. Aprilo sul computer dove si trova l’account del cliente (può essere quello di un’altra persona), autorizza, copia il codice che ti dà e incollalo nella finestra che appare. Il codice non si vede sullo schermo.
- **Codex**: Praxis ti mostra un link e un codice breve. Apri il link, scrivi il codice e autorizza. Se ti chiede di attivare il codice del dispositivo, si attiva nelle impostazioni di sicurezza dell’account ChatGPT.

Quando finisce, Praxis ti avvisa con l’email (mascherata) e il piano di quell’account. Così sai di essere entrato nell’account giusto.

### Se preferisci importare una sessione che esiste già

Con **Importa una sessione…** scegli se è di Claude o di Codex e indichi il file della sessione. Praxis la salva nel profilo senza mostrartela e ti dice a quale account appartiene. Se il file non è una sessione di quel programma, non viene salvato nulla.

### Come collegare un progetto a un profilo

Dentro il pulsante del profilo scegli **Usa sempre in questo progetto**. Da quel momento, ogni volta che apri quella cartella, Praxis usa quel profilo senza che tu glielo chieda. Il collegamento resta solo sul tuo computer, non viene scritto nulla dentro il progetto. Quando vuoi toglierlo, usa **Scollega**.

### Come cambiare profilo in 2 clic

Clic sul pulsante del profilo in alto, clic sul profilo che vuoi usare. Il pannello mostra l’email e il piano di ogni account, e le barre di utilizzo sono quelle dell’account che hai scelto.

### Cosa copre e cosa no

Un profilo copre tutto ciò che Praxis avvia per te: Claude e Codex dal pannello, i sub-agenti (gli aiutanti che lavorano per te), GLM e DeepSeek, il pannello ufficiale di Claude Code (tranne su Windows, vedi sotto) e i terminali nuovi che apri in quel progetto (i terminali sono le finestre dove si scrivono i comandi).

Quello che **non** copre:

- **L’estensione di Codex per VS Code.** È di un’altra azienda e Praxis non può cambiarle l’account. Continua a usare il tuo account di sempre.
- **Il pannello ufficiale di Claude su Windows.** Lì usa sempre il tuo account predefinito, perché Windows non permette a Praxis di cambiargli l’account. Il terminale e gli agenti di Praxis usano invece il profilo. Su Mac, Linux e WSL il pannello ufficiale usa il profilo.
- **I terminali che erano già aperti.** Chiudili e aprine uno nuovo dopo aver cambiato profilo.
- **La barra di utilizzo di Codex con un account di profilo.** Compare solo quando Codex risponde in quel momento. Se non risponde, vedi che è connesso, senza barre.

> 💡 Se su Windows una modifica fatta dentro un profilo non arriva al tuo account di sempre, è normale: lì alcuni file vengono copiati invece di essere condivisi. Le modifiche vanno dal tuo account di sempre verso il profilo, non il contrario.

### Se qualcosa non va

- **«Non trovo ancora Claude Code su questo computer»**: avvia Claude dal pannello una volta e riprova.
- **«Alcuni file di questo profilo entrano in conflitto con quelli del tuo account principale»**: non è stato cambiato né perso nulla. Apri una issue su GitHub e lo controlliamo (il link è qui sotto).
- **Eliminare un profilo** (**Elimina questo profilo…**) cancella le sue sessioni su questo computer. I tuoi progetti e il tuo account di sempre non cambiano.

---

## Se qualcosa non funziona

Non ti preoccupare, può succedere. Apri una issue su GitHub e descrivi cosa è successo 👉 [github.com/juanlara-aidev/praxis-it/issues](https://github.com/juanlara-aidev/praxis-it/issues).

Un paio di cose che risolvono il 90% dei casi:
- **L'estensione non appare**: chiudi l'editor e riaprilo.
- **Dice che la tua sessione è scaduta**: chiudi Claude Code e riaprilo.
- **Il pulsante non risponde**: ricarica la finestra (`Cmd/Ctrl+Shift+P` → Ricarica la finestra).

---

Fatto da **Juan Lara** · Per la community **VibeCoders**
