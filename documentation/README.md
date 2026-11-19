---
draft: false
doc_id: d-20260720-101826-994dd0
title: Processing
added_date: "2026-07-20 10:18:26"
last_updated: "2026-11-19"
summary: Project-owned documentation entry point, source/media boundaries and explicit website handoff.
parent_id: ""

---
# Processing

This folder documents the Java/Processing project. The repository root is the sketchbook and the Processing project owns its build, checks, renders and exports. [Sketchbook README](../README.md)

## Current Project Owners

| Question | Owner |
| --- | --- |
| How is the sketchbook arranged and run? | [Project README](../README.md) |
| How does InkEngine load presets and export? | [InkEngine README](../projects/InkEngine/README.md) and its source |
| Where are recovered experiments? | [recovered/](../recovered/) |
| Why were source, presets and external masters separated? | [Setup and design record](Project_Setup.md) |

The current project READMEs record Processing/Java mode and pinned ControlP5 requirements. The setup record preserves incorporation, rendering/preset ideas and recovery evidence; its incomplete sequence and old scope terminology are dated material.

## Project Media And Website Handoff

Work media and print masters belong beneath the configured Projects root at `processing/<project-id>/`. A GUI sketch receives its external base through its explicit ignored project-local configuration. The InkEngine example has `projects_base_dir` and exact `project_id: ink-engine`. The sketch checks that location before writing and reports configuration failures. [Configuration example](../projects/InkEngine/output-config.example.json) · [Output workspace](../projects/InkEngine/OutputWorkspace.java)

Tracked sketch assets and presets remain project source. External generated artwork has its own storage/recovery needs; retiring repository preview copies did not establish a backup or byte-equivalence guarantee.

A Catalogue Work can select the pipeline's `processing` media-source identity. Studio owns the exact Work selection and required media preparation, Refresh prepares Working output, Regenerate adopts Catalogue documents and Publish transfers completed selections. [Media-source configuration](https://github.com/dotlineform/dotlineform-site/blob/main/documentation/reference/Catalogue_Media_Pipeline_Config.md#work-media-sources) · [Catalogue workflow](https://github.com/dotlineform/dotlineform-site/blob/main/documentation/reference/Catalogue_Save_And_Refresh.md)

Docs source and managed attachments use their own configured Docs workspace and explicit collection ownership. [Docs source organisation](https://github.com/dotlineform/dotlineform-site/blob/main/documentation/reference/Source_Organisation.md)

## Review Boundary

Use project-owned requirements and agreed evidence when changing a sketch, helper or export. This documentation move ran no Processing compile, Java check, GUI export or media operation. Website test profiles and release commands do not become Processing lifecycle requirements.
