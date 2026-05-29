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

## Come si installa

Praxis ha bisogno di una **membership attiva di SinergIA**. Se ancora non ce l'hai, te la spiego più sotto.

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

## La membership di SinergIA

Praxis è per la community di **VibeCoders**. Quando apri l'estensione, ti chiede la tua email — la stessa con cui sei entrato in SinergIA — e verifica che la tua membership sia attiva.

Se ancora non fai parte della community, entra qui 👉 [skool.com/sinergia](https://www.skool.com/sinergia).

---

## Se qualcosa non funziona

Non ti preoccupare, può succedere. Scrivimi su **SinergIA** e lo sistemiamo insieme.

Un paio di cose che risolvono il 90% dei casi:
- **L'estensione non appare**: chiudi l'editor e riaprilo.
- **Dice che la tua sessione è scaduta**: chiudi Claude Code e riaprilo.
- **Il pulsante non risponde**: ricarica la finestra (`Cmd/Ctrl+Shift+P` → Ricarica la finestra).

---

Fatto da **Juan Lara** · Per la community **VibeCoders**
