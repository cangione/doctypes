# Stylesheet Inventory

An inventory of all formatting stylesheets (XSLT, XSL-FO, and FOSI) included in this repository.

## Summary

| Type | Count | Description |
|---|---|---|
| XSLT | 310 | XSL Transformation stylesheets (.xsl) |
| XSL-FO | 8 | XSLT stylesheets producing XSL-FO output for PDF rendering |
| FOSI | 33 | Formatting Output Specification Instance (.fos, .fosi) |
| **Total** | **343** | |

XSLT and XSL-FO stylesheets are found only in the MIL-STD-40051 packages. All other military specifications use FOSI formatting exclusively.

---

## XSL-FO Stylesheets

XSL-FO stylesheets transform SGML/XML source into XSL Formatting Objects for PDF output via Apache FOP or similar processors.

### MIL-STD-40051-2C Version 6.0

| File | Size | Description |
|---|---|---|
| `40051C_6_0/xslfo-main-v6_0.xsl` | 126 KB | Main XSL-FO stylesheet |
| `40051C_6_0/xslfo-main-_NOFIGTAB_TOC_v6_0.xsl` | 132 KB | Main stylesheet without figure/table TOC |
| `40051C_6_0/xslfo-main-v6_0_log_land.xsl` | 91 KB | Logbook layout, landscape orientation |
| `40051C_6_0/xslfo-main-v6_0_log_port.xsl` | 91 KB | Logbook layout, portrait orientation |
| `40051C_6_0/cstyle-v6_0/xslfo-main-v6_0.xsl` | 124 KB | Contractor-style main stylesheet |
| `40051C_6_0/cstyle-v6_0/xslfo-main-_NOFIGTAB_TOC_v6_0.xsl` | 132 KB | Contractor-style without figure/table TOC |
| `40051C_6_0/cstyle-v6_0/xslfo-main-v6_0_logland.xsl` | 128 KB | Contractor-style logbook, landscape |
| `40051C_6_0/cstyle-v6_0/xslfo-main-v6_0_LOGBOOK.xsl` | 127 KB | Contractor-style logbook |

### MIL-STD-40051-2C Version 6.3

| File | Size | Description |
|---|---|---|
| `40051C_6_3/xslfo-main-v6_3.xsl` | 123 KB | Main XSL-FO stylesheet |
| `40051C_6_3/xslfo-main-_NOFIGTAB_TOC_v6_3.xsl` | 123 KB | Main stylesheet without figure/table TOC |
| `40051C_6_3/xslfo-main-v6_3_log_land.xsl` | 89 KB | Logbook layout, landscape orientation |
| `40051C_6_3/xslfo-main-v6_3_log_port.xsl` | 127 KB | Logbook layout, portrait orientation |

---

## XSLT Modular Templates

MIL-STD-40051 uses a modular architecture with 150+ XSLT templates per version, organized by content type. These are imported by the main XSL-FO stylesheets above.

### MIL-STD-40051-2C Version 6.0 — `40051C_6_0/cstyle-v6_0/`

165 modular templates covering:

| Category | Examples |
|---|---|
| **Page layout** | page-setup, page-sequences, headers, footers |
| **Content structure** | front-matter, body, rear-matter, appendices |
| **Text formatting** | paragraphs, lists, notes, warnings, cautions |
| **Tables** | table formatting, stepped tables, maintenance allocation |
| **Graphics** | figure handling, graphic scaling, callouts |
| **Technical content** | wire lists, parts data, torque values, lubrication |
| **Safety** | hazard warnings, safety summaries, first aid |
| **Navigation** | TOC generation, cross-references, index |
| **Special elements** | foldouts, change bars, revision tracking |

### MIL-STD-40051-2C Version 6.3 — `40051C_6_3/cstyle-v6_3/`

139 modular templates with the same categories, updated for version 6.3.

---

## FOSI Stylesheets

FOSI (Formatting Output Specification Instance) stylesheets are SGML-era formatting specifications used by composition engines such as Arbortext and XyVision to render SGML documents. Each FOSI corresponds to a specific military specification DTD.

### MIL-PRF-5096F — Inspection & Maintenance Manuals

| File | Size | Description |
|---|---|---|
| `5096F-AV6D0P0/5096F-AV6D0P0.fos` | 1.8 MB | Inspection and maintenance |
| `5096F-BV6D0P0/5096F-BV6D0P0.fos` | 1.2 MB | Acceptance and functional check |
| `5096F-BV8D0P0/5096F-BV8D0P0.fos` | 1.2 MB | Functional check flight procedures |
| `5096F-DV6aD1P0/5096F-DV6aD1P0.fos` | 1.9 MB | Work cards |
| `5096F-DV8D0P0/5096F-DV8D0P0.fos` | 1.9 MB | Workcards |

### MIL-PRF-5096J — Workcards

| File | Size | Description |
|---|---|---|
| `5096J-DV9bD2P0/5096J-DV9bD2P0.fos` | 2.0 MB | Workcards |

### MIL-PRF-38314 — Operation and Associated Checklist

| File | Size | Description |
|---|---|---|
| `38314-BV8D0P0/38314-BV8D0P0.fos` | 1.4 MB | Space systems checklist |

### MIL-PRF-38769 — Work Unit Codes

| File | Size | Description |
|---|---|---|
| `38769D-BV6aD1P0/38769D-BV6aD1P0.fos` | 2.3 MB | Work unit codes (version D) |
| `38769G1BV9bD0P0/38769G1BV9bD0P0.fos` | 2.3 MB | Work unit codes (version G) |

### MIL-STD-38784 — General Style and Format

| File | Size | Description |
|---|---|---|
| `38784STD-BV7/38784STD-BV7.fos` | 1.3 MB | Baseline version 7 |
| `38784STD-BV7/38784STD-BV72.0.9a.fos` | 1.3 MB | Baseline version 7, patch 2.0.9a |
| `38784STD-BV8a/38784STD-BV8a.fos` | 105 KB | Baseline version 8a (compact) |
| `38784STD-BV8a/38784STD-BV8av8.fos` | 107 KB | Baseline version 8a, variant 8 |
| `38784STD-BV8a/38784STD-BV8a.fosi` | 1.3 MB | Baseline version 8a (compiled FOSI) |
| `38784STD-BV9/38784STD-BV9.fos` | 1.3 MB | Baseline version 9 |
| `38784STD-BV9a/38784STD-BV9a.fos` | 1.6 MB | Baseline version 9a |
| `38784STD-BV9b/38784STD-BV9b.fos` | 1.8 MB | Baseline version 9b |

### MIL-PRF-38807 — Illustrated Parts Breakdown

| File | Size | Description |
|---|---|---|
| `38807C-AV6D0P0/38807C-AV6D0P0.fos` | 1.0 MB | IPB (version C) |
| `38807D2AV9bD0P0/38807D2AV9bD0P0.fos` | 1.0 MB | IPB (version D) |

### MIL-PRF-83495B — General Equipment / Systems / Job Guide

| File | Size | Description |
|---|---|---|
| `83495B1AV6aD0P2/83495B1AV6aD0P2.fos` | 1.5 MB | General equipment |
| `83495B1BV6D0P0/83495B1BV6D0P0.fos` | 1.5 MB | General systems |
| `83495B1BV6aD0P1/83495B1BV6aD0P1.fos` | 1.5 MB | General systems |
| `83495B1CV6D1P0/83495B1CV6D1P0.fos` | 1.8 MB | Job guide |
| `83495B1CV6aD3P0/83495B1CV6aD3P0.fos` | 1.7 MB | Job guide |

### MIL-PRF-87929 — General Work Package

| File | Size | Description |
|---|---|---|
| `87929C-AV6aD1P0/87929C-AV6aD1P0.fos` | 2.5 MB | General work package (version C) |
| `87929D-AV9D0P0/87929D-AV9D0P0.fos` | 2.5 MB | General work package (version D) |

### MIL-PRF-9977K — Nonnuclear Munitions Manuals

| File | Size | Description |
|---|---|---|
| `9977K1CV6aD0P0/9977K1CV6aD0P0.fos` | 1.5 MB | Basic information manual |
| `9977K-DV6D0P0/9977K-DV6D0P0.fos` | 1.7 MB | Loading procedures manual |
| `9977K-GV6D0P0/9977K-GV6D0P0.fos` | 1.6 MB | Loading procedures manual |

### MIL-STD-3001 — Technical Manual Assembly

| File | Size | Description |
|---|---|---|
| `MILSTD3001/Milstd1.fos` | 1.6 MB | TM assembly formatting |
| `MILSTD3001/pmrim.fos` | 420 KB | PMRIM (Provisioning Master Record) |
| `MILSTD3001/pmrim_old.fos` | 420 KB | PMRIM (legacy version) |

### MIL-STD-40051-2C

| File | Size | Description |
|---|---|---|
| `40051C_6_0/40051C_6_0.fos` | 1.2 MB | Version 6.0 FOSI (alongside XSLT) |

---

## Standards Without Stylesheets

The following standards in this repository contain only schema definitions (DTD, XSD, RNG) and do not include formatting stylesheets:

- **DITA 1.2** — Use DITA-OT plugins for rendering
- **DITA 1.3** — Use DITA-OT plugins for rendering
- **S1000D 2.1 through 6.0** — Use external S1000D rendering tools
- **ATA iSpec 2200** — Uses external composition systems
- **ATA Spec 2300** — Uses external composition systems
- **GEIA-STD-0007-B** — Schema only
- **MIL-PRF-5096F (FV6D0P0)** — Checklist DTD for validation only, no FOSI
