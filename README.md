# DataStudio Lite

### Free Offline JSON, CSV & Markdown Data Converter

**Convert, format, preview, and download structured data directly in your browser. No server or API calls required.**

DataStudio Lite is a free, single-file browser application for working with JSON arrays, CSV data, and Markdown tables.

Whether you're preparing sample datasets, converting structured information, or formatting JSON for easier reading, DataStudio Lite provides practical conversion tools in one lightweight interface.

> **Language notice:** The application interface is in Korean (한국어). This README provides English-language documentation.

### [Launch the Free Live Demo](https://mcjin87-eng.github.io/datastudio-offline-converter/)

---

## Features

### Data Conversion

| Operation | Available in Lite |
|---|---|
| JSON → CSV | Yes |
| CSV → JSON | Yes |
| JSON → Markdown table | Yes |
| Beautify JSON | Yes |
| Minify JSON | Yes |

### Additional Tools

- **Editable input area** — Enter or paste JSON and CSV content.
- **Editable output area** — View and modify generated text.
- **Table preview** — Inspect conversion results in a table.
- **Sample data** — Explore the interface using provided examples.
- **Download output** — Download generated content.
- **Local processing** — Data conversion happens inside your browser.
- **Single-file application** — The app is contained in `index.html`.

DataStudio Lite does not require a backend server or external API calls for its supported operations.

## Quick Start

### Option 1: Use the Live Demo

Open:

**https://mcjin87-eng.github.io/datastudio-offline-converter/**

1. Open the application in your browser.
2. Enter or paste supported JSON or CSV data.
3. Select the conversion or formatting operation.
4. Review the generated output and table preview where applicable.
5. Edit or download the result as needed.

The interface controls are labeled in Korean.

### Option 2: Run Locally

1. Open the GitHub repository: [datastudio-offline-converter](https://github.com/mcjin87-eng/datastudio-offline-converter).
2. Select **Code → Download ZIP**.
3. Extract the downloaded archive.
4. Locate `index.html`.
5. Open `index.html` in a compatible web browser.

No development server, build process, or API credentials are required for the supported Lite operations.

The single-file application is designed to run locally without an internet connection.

## How to Use

### JSON to CSV

Enter a JSON array and select the JSON-to-CSV conversion operation.

Example input:

```json
[
  {
    "id": 1,
    "name": "Alex",
    "role": "Designer"
  },
  {
    "id": 2,
    "name": "Sam",
    "role": "Developer"
  }
]
```

Illustrative CSV representation:

```csv
id,name,role
1,Alex,Designer
2,Sam,Developer
```

The exact output formatting depends on the application's conversion logic.

### CSV to JSON

Enter CSV data and select the CSV-to-JSON operation.

Example input:

```csv
id,name,role
1,Alex,Designer
2,Sam,Developer
```

Illustrative JSON representation:

```json
[
  {
    "id": "1",
    "name": "Alex",
    "role": "Designer"
  },
  {
    "id": "2",
    "name": "Sam",
    "role": "Developer"
  }
]
```

CSV fields may be treated as text. Do not assume automatic numeric, date, or boolean type inference unless verified.

### JSON to Markdown Table

Convert a JSON array into Markdown-compatible table text.

Example input:

```json
[
  {
    "name": "Alex",
    "status": "Active"
  },
  {
    "name": "Sam",
    "status": "Pending"
  }
]
```

Illustrative Markdown output:

```markdown
| name | status |
| --- | --- |
| Alex | Active |
| Sam | Pending |
```

Markdown output can be reviewed and edited before reuse.

### Beautify or Minify JSON

Use the JSON formatting operations to make structured data easier to inspect or more compact.

**Beautify JSON**

Formats JSON with indentation and line breaks for readability.

**Minify JSON**

Removes unnecessary formatting whitespace to produce a more compact representation.

### Preview and Download

After conversion:

1. Review the generated output.
2. Inspect the table preview when available.
3. Make manual adjustments if needed.
4. Use the application's download function to save the output.

Always review converted data before using it in production workflows.

---

## Privacy & Local Processing

DataStudio Lite performs its supported conversion and formatting operations locally in the browser.

**Confirmed application behavior:**

- No application backend server is required.
- No external API calls are used for the supported Lite operations.
- Input data is processed in the browser rather than submitted to a conversion service.
- The application can be run locally from `index.html`.

### Important Privacy Considerations

Local processing reduces the need to transmit data to a third-party conversion service, but it is not a guarantee of complete security or confidentiality.

Browser extensions, device security, downloaded files, and the environment in which you run the application may affect the privacy of your information.

For sensitive or regulated datasets, follow your organization's data-handling policies and review the application code before use.

---

## Lite vs. PRO

DataStudio Lite provides free data conversion and JSON formatting functionality.

The separate PRO offering advertises additional developer-oriented data tools.

| Capability | DataStudio Lite | PRO Offering |
|---|---|---|
| JSON → CSV | Included | Not specified here |
| CSV → JSON | Included | Not specified here |
| JSON → Markdown table | Included | Not specified here |
| JSON beautify/minify | Included | Not specified here |
| Conversion result preview | Included | Not specified here |
| Type generators: Zod, TypeScript, Python | Not included | Advertised |
| Regex PII masking | Not included | Advertised |
| SQL dialect generator | Not included | Advertised |
| Mock data builder | Not included | Advertised |

PRO capabilities are listed according to the feature descriptions advertised in Lite. They have not been independently verified here.

### Explore DataStudio PRO

Interested in additional data-development tools?

Visit the creator's Gumroad storefront to explore the available PRO offering:

**[Explore the Gumroad Store](https://mcjinster.gumroad.com)**

The PRO edition is optional. DataStudio Lite remains free to use without purchasing an upgrade.

---

## Project Structure

```text
datastudio-offline-converter/
├── index.html     # Standalone browser application
└── README.md      # Project documentation
```

`index.html` contains the Lite application.

No development environment or package installation is required to run the single-file app.

## Deployment

### GitHub Pages

The intended GitHub Pages deployment uses the repository's `index.html` file.

For a standard branch-based deployment:

1. Open the repository's **Settings → Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose the appropriate branch, typically `main`.
4. Select the `/ (root)` folder.
5. Save the configuration.
6. Confirm that the published site loads and its conversion controls work.

Expected project URL:

**https://mcjin87-eng.github.io/datastudio-offline-converter/**

GitHub Pages is a static hosting service. DataStudio Lite's supported conversions run in the visitor's browser rather than on a separate application server.

### Local Use

GitHub Pages is not required for local operation.

Download `index.html` and open it directly in a compatible browser.

---

## Limitations

DataStudio Lite is intentionally focused on lightweight data conversion and formatting.

- **Korean interface:** The current application UI is in Korean.
- **JSON input:** JSON-to-CSV and JSON-to-Markdown workflows are intended for JSON arrays.
- **Data structures:** Complex nested objects and arrays may not translate cleanly into flat CSV or Markdown tables.
- **CSV interpretation:** Do not assume automatic data-type detection or support for every CSV dialect.
- **Formatting differences:** Output structure, escaping, and field handling depend on the implemented conversion logic.
- **Large datasets:** Browser performance may vary with input size and device resources.
- **Advanced tools:** Type generation, PII masking, SQL dialect generation, and mock data creation are not Lite features.
- **Security:** Local processing does not replace secure data-handling practices.

This application is a convenience tool, not a data validation, compliance, anonymization, or security service.

## Feedback & Contributions

Bug reports, documentation improvements, and suggestions are welcome through the repository's available GitHub collaboration features.

When reporting a conversion issue, provide a minimal, non-sensitive example that reproduces the behavior.

Do not submit private, confidential, or personally identifiable datasets in public GitHub issues.

Contributions and reuse remain subject to the project's applicable licensing terms.

## License

**No license is currently included in this repository.**

Although the source code is publicly visible, that does not automatically grant permission to copy, modify, redistribute, or commercially reuse it.

The project should not be treated as legally open-source software unless an appropriate license is explicitly provided.

## Frequently Asked Questions

**Is DataStudio Lite free?**

Yes. DataStudio Lite is a free browser-based application.

**Does it require an API key?**

No. The supported Lite conversion and formatting operations do not require API credentials.

**Is my input uploaded to a server?**

The application performs its supported operations locally and does not make server or API calls. This does not guarantee security against risks outside the application's control.

**Can I use it offline?**

Yes. The standalone HTML application is designed to run locally without an internet connection.

**Does it support Excel files directly?**

Direct XLSX import or export is not a confirmed Lite feature. Use supported JSON or CSV input.

**Does Lite include Zod, TypeScript, Python, SQL, or PII-masking generators?**

No. Those are advertised as separate PRO capabilities, not features of the Lite application.

**Can I modify and redistribute the code?**

No reuse or redistribution rights have been granted through an explicit repository license at this time. Contact the maintainer if you need permission.

---

## Get Started for Free

Convert JSON, CSV, and Markdown table data without setting up a backend or using an external conversion API.

**Free to use. Local by design. Focused on practical data conversion.**

**[Launch DataStudio Lite](https://mcjin87-eng.github.io/datastudio-offline-converter/)**

**[Explore the Optional PRO Offering](https://mcjinster.gumroad.com)**

*DataStudio Lite is a free tool with a Korean-language interface. PRO is a separate, optional offering.*
