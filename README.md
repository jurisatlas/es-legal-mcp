# Spain Legal Research MCP Server (`es-legal-mcp`)

**[Español](#lang-es) | [English Documentation](#english-documentation)**

---

<a id="lang-es"></a>
## Servidor MCP de Legislación y Jurisprudencia (`es-legal-mcp`) — Español

### Acerca de este repositorio

Este repositorio proporciona un servidor Model Context Protocol (MCP) que conecta su asistente de IA (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline, Continue.dev o Antigravity) directamente con los portales legislativos oficiales y las bases de datos judiciales para **Spain** (primera instancia, tribunales superiores / apelación y tribunales supremos o constitucionales).

### Instalación rápida (Selección de aplicación de IA)

1. **Descarga:** Haga clic en **`<> Code` -> `Download ZIP`** y descomprima la carpeta en su equipo.
2. **Ejecución:** Haga doble clic en **`Click_Here_To_Install_Windows.bat`** (Windows) o **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Selección de cliente IA:** Marque las aplicaciones de IA que utilice (Claude, Cursor, Windsurf, VS Code, Antigravity), pulse instalar y reinicie su aplicación de IA.

**Nota de seguridad:** El instalador opera en modo de solo lectura y no accede ni modifica sus archivos personales.

### Jerarquía judicial y fuentes oficiales

| Instancia judicial | Órganos jurisdiccionales cubiertos |
|:---|:---|
| **Primera instancia** | Juzgados de Primera Instancia e Instrucción, Juzgados de lo Mercantil, de lo Penal, de lo Social & de lo Contencioso-Administrativo |
| **Segunda instancia (Apelación y Tribunales Superiores)** | 50 Audiencias Provinciales, 17 Tribunales Superiores de Justicia (TSJ of Autonomous Communities) & Audiencia Nacional (AN) |
| **Tribunales Supremos y Constitucionales** | Tribunal Supremo (TS) & Tribunal Constitucional de España (TC) |

- **BOE Datos Abiertos REST API (boe.es/datosabiertos):** [https://www.boe.es](https://www.boe.es) (`boe.es`, `congreso.es`)
- **CENDOJ (Centro de Documentación Judicial — TS, AN, 17 TSJ, 50 Audiencias Provinciales & Juzgados):** [https://www.poderjudicial.es/search/indexAN.jsp](https://www.poderjudicial.es/search/indexAN.jsp) (`poderjudicial.es`, `tribunalconstitucional.es`, `boe.es`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Spain (ES)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Spain**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Juzgados de Primera Instancia e Instrucción, Juzgados de lo Mercantil, de lo Penal, de lo Social & de lo Contencioso-Administrativo |
| **Tier 2 — Regional / Cantonal / Appellate** | 50 Audiencias Provinciales, 17 Tribunales Superiores de Justicia (TSJ of Autonomous Communities) & Audiencia Nacional (AN) |
| **Tier 3 — Supreme & Constitutional** | Tribunal Supremo (TS) & Tribunal Constitucional de España (TC) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** BOE Datos Abiertos REST API (boe.es/datosabiertos) — [https://www.boe.es](https://www.boe.es)
  - *Indexed Legislation Domains:* `boe.es`, `congreso.es`
- **Court Decisions & Jurisprudence Archives:** CENDOJ (Centro de Documentación Judicial — TS, AN, 17 TSJ, 50 Audiencias Provinciales & Juzgados) — [https://www.poderjudicial.es/search/indexAN.jsp](https://www.poderjudicial.es/search/indexAN.jsp)
  - *Indexed Judicial & Open Case Law Domains:* `poderjudicial.es`, `tribunalconstitucional.es`, `boe.es`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Spain. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Spain. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Spain. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "es-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/es-legal-mcp/archive/refs/heads/main.zip",
        "es-legal-mcp"
      ]
    }
  }
}
```
</details>
