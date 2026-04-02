# Document Type Definitions Repository

A curated collection of document type definitions (DTDs, XML Schemas, RELAX NG) for technical publication standards used in aerospace, defense, and general technical documentation.

## Repository Structure

```
doctypes/
├── doctypes/           Schema and DTD collections by standard
├── entities/           Shared entity sets (ISO, EPS symbol libraries)
└── graphics/           Standard EPS graphics for technical illustrations
```

## Standards Included

### DITA (Darwin Information Typing Architecture)

#### DITA 1.2

OASIS DITA 1.2 document type shells. Formats: DTD, XSD.

| Category | Document Types |
|---|---|
| **Base** | `basetopic`, `basemap` |
| **Technical Content** | `topic`, `concept`, `task`, `generalTask`, `reference`, `ditabase` |
| **Maps** | `map`, `bookmap` |
| **Glossary** | `glossentry`, `glossgroup`, `glossary` |
| **Learning & Training** | `learningContent`, `learningAssessment`, `learningOverview`, `learningSummary`, `learningPlan`, `learningMap`, `learningBookmap` |
| **Machinery** | `machineryTask` |
| **Subject Scheme** | `subjectScheme`, `classifyMap` |
| **Conditional Processing** | `ditaval` |

**Domains:** abbreviate, classify, delay resolution, glossref, hazard statement, highlight, indexing, learning, learning interaction base, learning map, learning metadata, programming, software, task requirements, UI, utilities, XNAL.

#### DITA 1.3

OASIS DITA 1.3 document type shells. Formats: DTD, XSD, RNG.

All DITA 1.2 types plus:

| New in 1.3 | Description |
|---|---|
| `troubleshooting` | Problem-cause-remedy topic specialization |
| `learningGroupMap` | Organizes learning groups within a map |
| `learningObjectMap` | Organizes learning objects within a map |

**New domains:** delivery target attribute, DITAVAL reference, equation, learning 2, learning interaction base 2, markup, MathML, release management, SVG, XML.

**Embedded standards:** MathML 3.0, SVG 1.1 (full schema sets included).

---

### S1000D (International Specification for Technical Publications)

| Version | Schema Format | Notes |
|---|---|---|
| **S1000D 2.1** | SGML DTD, XML DTD, XSD | Legacy |
| **S1000D 2.2** | SGML DTD, XML DTD, XSD | Legacy |
| **S1000D 2.3** | SGML DTD, XML DTD, XSD | Legacy |
| **S1000D 3.0** | SGML DTD, XML DTD, XSD | Transitional |
| **S1000D 4.1** | XSD | XML-only |
| **S1000D 4.2** | XSD | XML-only |
| **S1000D 5.0** | XSD | Current |
| **S1000D 6.0** | XSD | Current |

S1000D is the international specification for the procurement and production of technical publications, widely used in aerospace, defense, and transportation. Versions 4.x and later are XML-only with XSD schemas; earlier versions include SGML DTDs for legacy compatibility.

---

### ATA (Air Transport Association)

| Standard | Schema Format | Description |
|---|---|---|
| **ATA iSpec 2200 (2003.1)** | SGML DTD | Information standards for aviation maintenance data. 18 module DTDs covering AIPC, AMM, CMM, IPC, SRM, WDM, and more. |
| **ATA Spec 2300 (2017.1)** | XML DTD, XSD | Aircraft data exchange standard. ~97 schema files organized across 10 topic-specific directories. |

---

### MIL-STD and Government Standards

| Standard | Schema Format | Description |
|---|---|---|
| **MIL-STD-3001** | SGML DTD | Documentation requirements and standards for military technical manuals. ~50 files including DTDs, entities, and FOSI formatting objects. |
| **GEIA-STD-0007-B** | XSD | Government Electronics & Information Technology Association standard for logistics product data. |

---

### Military Technical Manual DTDs (MIL-PRF / MIL-DTL Series)

SGML document type definitions for specific military performance and detail specifications. Each includes DTD, entity, processing configuration (DCF, BCF), and FOSI formatting files.

| Spec Number | Variants |
|---|---|
| **38314** | BV8D0P0 |
| **38769** | BV6aD1P0, BV9bD0P0 |
| **38784STD** | BV7, BV8a, BV9, BV9a, BV9b |
| **38807** | AV6D0P0, AV9bD0P0 |
| **40051C** | 6.0, 6.3 |
| **5096F** | AV6D0P0, BV6D0P0, BV8D0P0, DV6aD1P0, DV8D0P0, FV6D0P0 |
| **5096J** | DV9bD2P0 |
| **83495B1** | AV6aD0P2, BV6aD0P1, BV6D0P0, CV6aD3P0, CV6D1P0 |
| **87929** | AV6aD1P0, AV9D0P0 |
| **9977K** | DV6D0P0, GV6D0P0, CV6aD0P0 |

Variant codes follow the pattern: `[baseline version][amendment version][document type][page count]`.

---

## Entity Libraries

| Directory | Contents |
|---|---|
| `entities/big_EPS_symbols_v1` | Large-format EPS symbol entities |
| `entities/small_EPS_symbols_v1` | Small-format EPS symbol entities |
| `entities/local_big_EPS_symbols_v1` | Local overrides for large EPS symbols |
| `entities/local_small_EPS_symbols_v1` | Local overrides for small EPS symbols |
| `entities/supported_ISO_entities_v1` | ISO 8879 / ISO 9573 character entity sets |
| `entities/fosi` | FOSI (Formatting Output Specification Instance) entity definitions |

## Graphics Library

Standard EPS graphics used in military and aerospace technical manuals. Includes hazard symbols, schematic symbols, flag indicators, geometric shapes, and warning/caution icons.

## XML Catalogs

Each standard includes OASIS XML Catalog files (`catalog.xml`) for schema resolution. The root catalog at `doctypes/catalog.xml` chains to all sub-catalogs.

## License

DITA document types are copyright OASIS and distributed under the OASIS IPR policy. S1000D schemas are maintained by the ASD S1000D Council. Military specifications are public domain (U.S. Government works). ATA specifications are copyright Air Transport Association.
