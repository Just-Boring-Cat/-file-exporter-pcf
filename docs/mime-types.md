# Common MIME Types

Use the MIME type that matches the file you want to export.

The control does not validate against a MIME whitelist. It exports whatever text content and metadata the maker provides. The list below is a practical example set, not a hard allowlist.

| Category | Extension | MIME type | Example use |
| --- | --- | --- | --- |
| Plain text | `txt` | `text/plain` | notes, logs, simple exports |
| CSV | `csv` | `text/csv` | table exports |
| TSV | `tsv` | `text/tab-separated-values` | spreadsheet-style exports |
| JSON | `json` | `application/json` | config or integration payloads |
| XML | `xml` | `application/xml` | XML integrations |
| HTML | `html` | `text/html` | markup exports |
| Markdown | `md` | `text/markdown` | documentation-like exports |
| JavaScript | `js` | `application/javascript` | script file exports |
| TypeScript | `ts` | `application/typescript` | TypeScript source exports |
| CSS | `css` | `text/css` | stylesheet exports |
| SVG | `svg` | `image/svg+xml` | vector markup |
| YAML | `yaml` | `application/yaml` | YAML config |
| SQL | `sql` | `application/sql` | SQL queries and scripts |
| SQL | `sql` | `text/x-sql` | alternate SQL labeling |
| Python | `py` | `text/x-python` | Python source files |
| C# | `cs` | `text/x-csharp` | C# source files |
| C# | `cs` | `text/plain` | fallback plain-text source export |
| Java | `java` | `text/x-java-source` | Java source files |
| Shell | `sh` | `application/x-sh` | shell scripts |
| PowerShell | `ps1` | `text/plain` | PowerShell scripts |
| INI | `ini` | `text/plain` | config files |
| Log | `log` | `text/plain` | log exports |
| PDF | `pdf` | `application/pdf` | only if the content is already valid PDF data |

## Practical rule

- If the content is text, use a text-based MIME type
- If another system will consume the file, use the MIME type that system expects
- For Power Automate or SharePoint flows, the MIME type is useful metadata but the actual file bytes usually come from the `base64` output
- When in doubt, `text/plain` is a safe fallback for text-based exports
