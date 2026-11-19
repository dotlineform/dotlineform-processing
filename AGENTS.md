# Processing repository rules

- Use Processing 4.5.5 in Java mode with the bundled ControlP5 2.2.6 library.
- Preserve sketches in `recovered/` unless the task calls for changing them.
- Keep renders and print masters in the configured external workspace under `$DOTLINEFORM_PROJECTS_BASE_DIR/processing/<project-id>/`. Keep machine-specific output configuration out of Git.
- Run the relevant compile or Java check documented in the [README](README.md). Treat GUI rendering and Studio import as separate steps.
