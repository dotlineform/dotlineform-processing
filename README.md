# Processing

This repository is the Dotlineform Processing sketchbook. Set Processing's sketchbook location to the checkout root. Processing 4.5.5 in Java mode is the authoring and rendering environment.

## Structure

- `projects/` contains runnable sketches. Each sketch directory has the same
  name as its primary `.pde` file, as required by Processing.
- `recovered/` preserves source snapshots that have not yet been promoted into
  runnable projects.
- `libraries/` contains sketchbook libraries required by the projects.
  ControlP5 2.2.6 is currently pinned here.

Processing compiler output under `projects/**/out/` is ignored. Large inputs,
repeated renders, and print masters belong outside Git under
`$DOTLINEFORM_PROJECTS_BASE_DIR/processing/<project-id>/`. A GUI-launched
Processing application must receive that base through its explicit ignored
project-local configuration; it must not rely on shell environment inheritance
or fall back to the repository.

The project guide describes the sketchbook, external media and the Studio handoff. [Processing documentation](documentation/README.md)

## Projects

- `InkEngine` is the first recovered runnable project.

InkEngine uses exact project identity `ink-engine`. Its tracked
`output-config.example.json` is copied to the ignored
`data/output-config.local.json` and given the absolute external projects base.
The sketch validates that base and creates only `processing/` and
`processing/ink-engine/` beneath it when needed.

Historical InkEngine preview copies were retired from the repository after the
user confirmed that the wanted files had been copied into the external project
workspace. Git history remains the ordinary source-code recovery boundary; the
external work media has no repository backup or byte-equivalence guarantee.

The path helper has one Processing-independent verification command, run from
the repository root with Processing's bundled Java:

```sh
ink_engine_test_dir=$(mktemp -d /tmp/ink-engine-output-test.XXXXXX)
/Applications/Processing.app/Contents/app/resources/jdk/bin/javac \
  -d "$ink_engine_test_dir" \
  projects/InkEngine/OutputWorkspace.java \
  tests/OutputWorkspaceTest.java
/Applications/Processing.app/Contents/app/resources/jdk/bin/java \
  -cp "$ink_engine_test_dir" OutputWorkspaceTest
```

## Recovered Source

- `layer-permutations/` contains successive versions of the layer permutation
  experiments.
- `simple-composite/` contains the minimal three-image composite experiments.

Do not extract shared code or choose a canonical recovered version until the
relevant sketches have been understood and run.

## Licences

New Processing code and documentation owned by Mike Davies are available under MIT. Material previously released under CC0 in `dotlineform-site` retains that dedication. The bundled ControlP5 2.2.6 library by Andreas Schlegel retains its LGPL 2.1-or-later terms and source notices. [MIT](LICENSE) · [Historical CC0](LICENSES/CC0-1.0.txt) · [ControlP5 licence](libraries/controlP5/LICENSE)
