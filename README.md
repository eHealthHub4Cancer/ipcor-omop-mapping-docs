# IPCOR Prostate Cancer Registry to OMOP CDM v5.4: mapping documentation

Project documentation for the standardisation of the IPCOR prostate-cancer
registry to the OMOP Common Data Model (v5.4), part of the **eHealth-Hub for
Cancer**.

**Live site:** https://ehealthhub4cancer.github.io/ipcor-omop-mapping-docs/

This repository holds the documentation only. The mapping pipeline is kept in a
separate repository, which is currently private; read access is available on
request.

## What is here

| Path | What it is |
|---|---|
| `index.html` | The documentation website (also served at the live link above). Covers the background, the source data, the OHDSI toolchain (WhiteRabbit, Rabbit-in-a-Hat, Athena, Usagi), what was and was not mapped, the data-quality loop, the clarifications with the IPCOR team, how to run the pipeline, and a variable-level summary. |
| `docs/IPCOR_OMOP_Mapping_Documentation.docx` / `.pdf` | The same documentation as a Word file and PDF. Read this first. |
| `docs/IPCOR_OMOP_Field_Level_Mapping_Specification.docx` / `.pdf` | The companion Rabbit-in-a-Hat specification: table by table and field by field, every source column mapped to its OMOP table and field, with the logic and the modelling notes. |
| `data/IPCOR_variable_mapping.csv` | The variable-level list: each core clinical variable, its OMOP table and concept, and its mapping status. |
| `assets/diagrams/` | The pipeline, architecture, run-flow and loop diagrams used in the documents, as SVG and PNG. |

## How the mapping was done

The work followed the standard OHDSI workflow. The source was profiled with
WhiteRabbit; the table-by-table ETL design was authored in Rabbit-in-a-Hat; each
field was mapped to a standard concept found in Athena; each categorical value
was mapped in Usagi and exported as a source-to-concept map; and the result was
validated with the OHDSI Data Quality Dashboard. Because IPCOR has no vocabulary
of its own, every concept was sourced from Athena and reviewed by hand.

## Contact

Jeremiah Akintomide, University of Limerick. akintomide.jeremiah@ul.ie

The eHealth-Hub for Cancer is a Strand II project funded under the North South
Research Programme (NSRP). The NSRP is a collaborative scheme funded through the
Government's Shared Island Fund. It is administered by the Higher Education
Authority (HEA) on behalf of the Department of Further and Higher Education,
Research, Innovation and Science. https://ehealth4cancer.ie/
