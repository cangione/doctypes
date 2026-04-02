# S1000D Schema Documentation

HTML reference documentation for S1000D 4.1 and 4.2 XML schemas, generated using the xs3p XSLT stylesheet.

## Overview

This directory contains complete HTML documentation for all S1000D 4.1 and 4.2 XML Schema Definition (XSD) files. Each schema has been converted to an interactive, browsable HTML reference with:

- **Element definitions** with type information and cardinality
- **Complex type hierarchies** with inheritance chains
- **Attribute specifications** including data types and constraints
- **Content model diagrams** showing element relationships
- **Cross-references** between related types and elements
- **Glossary** of schema components
- **Bootstrap-based responsive layout** for desktop and mobile

## Directory Structure

```
schema.docs/
├── S1000D_4.1/
│   ├── index.html                    (Main index — start here)
│   ├── appliccrossreftable.html
│   ├── brex.html
│   ├── ... (28 more schema files)
│   └── xlink.html
│
└── S1000D_4.2/
    ├── index.html                    (Main index — start here)
    ├── appliccrossreftable.html
    ├── brdoc.html                    (New in 4.2)
    ├── brex.html
    ├── ... (28 more main schema files)
    ├── xlink.html
    │
    └── lom_*.html                    (Learning Object Metadata schemas)
        ├── lom.html                  (Merged LOM schema)
        ├── lom_common_*.html
        ├── lom_extend_*.html
        ├── lom_unique_*.html
        └── lom_vocab_*.html
```

## Quick Start

### S1000D 4.1
- **Index**: `/Users/charlesangione/git.sgmlxml/doctypes/schema.docs/S1000D_4.1/index.html`
- **Total files**: 31 HTML documents
- **Total size**: 110 MB
- **Schemas**: 30 main data module schemas

### S1000D 4.2
- **Index**: `/Users/charlesangione/git.sgmlxml/doctypes/schema.docs/S1000D_4.2/index.html`
- **Total files**: 49 HTML documents
- **Total size**: 126 MB
- **Main schemas**: 32 data module schemas
- **LOM schemas**: 15 learning object metadata component schemas + 1 merged

## Key S1000D Schemas

| Schema | Purpose |
|---|---|
| **brex** | Business Rules Exchange — regulatory and structural rules |
| **pm** | Publication Module — core technical documentation container |
| **dml** | Data Manipulation Language — conditional content |
| **descript** | Description — narrative content modules |
| **proced** | Procedures — step-by-step tasks and maintenance procedures |
| **fault** | Fault Reporting — troubleshooting and diagnostics |
| **sb** | Service Bulletin — service notices and updates |
| **crew** | Crew Data — personnel and training information |
| **learning** | Learning Content — training and educational material |
| **ipd** | Illustrated Parts Data — parts catalogs with graphics |
| **comment** | Comments — editorial and workflow comments |
| **checklist** | Checklists — inspection and verification lists |
| **container** | Container — document packages and multi-module collections |
| **frontmatter** | Front Matter — cover pages and introductory content |
| **xcf** | Extended Configurability Framework — product variants |

## What's New in 4.2

- **brdoc.xsd**: New Business Rules Document schema
- **icnmetadata.xsd**: New illustration metadata schema
- **Extended LOM support**: Complete Learning Object Metadata specification with 15 sub-schemas
- Enhanced type definitions across core schemas

## How to Use

1. **For overview**: Open the `index.html` file in your version's directory in a web browser
2. **For specific schema**: Click on any schema name to open its documentation
3. **For type/element lookup**: Use your browser's Find function (Ctrl+F / Cmd+F) on the index page
4. **For details**: Each schema page includes:
   - Table of contents with alphabetical listings
   - Type hierarchy diagrams
   - Attribute constraints and validation rules
   - Example XML structures
   - Cross-references to related schemas

## Generation Details

**Tool**: xs3p (XML Schema Documentation Generator)
**XSLT Processor**: xsltproc 1.1.34
**Generated**: 2026-04-02
**Parameters**:
- `sortByComponent=true` — Alphabetical component ordering
- `printAllSuperTypes=true` — Full inheritance chains
- `printAllSubTypes=true` — All derived types
- `printGlossary=true` — Component glossary
- `searchIncludedSchemas=false` — Skip external includes
- `searchImportedSchemas=false` — Skip external imports

## File Statistics

### S1000D 4.1
- **30 main schemas** (appliccrossreftable, brex, checklist, comment, comrep, condcrossreftable, container, crew, dc, ddn, descript, dml, fault, frontmatter, ipd, learning, pm, prdcrossreftable, proced, process, rdf, sb, schedul, scocontent, scormcontentpackage, update, wrngdata, wrngflds, xcf, xlink)

### S1000D 4.2
- **32 main schemas** (all 4.1 schemas + brdoc, icnmetadata)
- **15 LOM component schemas** (common, extend, unique, vocab variants)
- **1 merged LOM schema** (lom.html — consolidated view)

## Documentation Features

Each schema documentation page includes:

- **Title and Overview** — Schema purpose and scope
- **Table of Contents** — Quick navigation to elements, types, groups
- **Global Elements** — Root and top-level element definitions
- **Complex Types** — Composite data types with element and attribute composition
- **Simple Types** — Restricted base types and enumerations
- **Attribute Groups** — Reusable attribute definitions
- **Type Hierarchy** — Base types and derived types
- **Content Model** — Visual representation of element nesting and cardinality
- **Attribute Specifications** — Data types, defaults, required/optional status
- **Glossary** — Definition index of all components
- **Source View** — Raw XSD fragment for each component

## Technical Notes

- HTML files are self-contained with embedded Bootstrap CSS
- Responsive design adapts to mobile, tablet, and desktop screens
- Cross-schema references are implemented as hyperlinks where possible
- Large schemas (> 5MB) are rendered as multi-thousand-line HTML documents
- All documentation is read-only and stateless

## Related Resources

- **S1000D Standard**: International specification for technical documentation
- **XML Schema (XSD)**: W3C standard for XML validation and documentation
- **xs3p**: XSLT stylesheet for rendering XSD as HTML (https://www.w3.org/2001/05/xmlschema-instance)

