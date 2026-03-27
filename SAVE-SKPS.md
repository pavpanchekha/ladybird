# Save SKPs

Set `LADYBIRD_DUMP_SKP_DIR` to an existing directory before launching Ladybird.

Example with the usual run path:

```sh
mkdir -p /tmp/ladybird-skps
LADYBIRD_DUMP_SKP_DIR=/tmp/ladybird-skps ./Meta/ladybird.py run
```

Open a specific page:

```sh
mkdir -p /tmp/ladybird-skps
LADYBIRD_DUMP_SKP_DIR=/tmp/ladybird-skps ./Meta/ladybird.py run https://example.com
```

Run the built app directly:

```sh
mkdir -p /tmp/ladybird-skps
LADYBIRD_DUMP_SKP_DIR=/tmp/ladybird-skps Build/release/bin/Ladybird.app/Contents/MacOS/Ladybird https://example.com
```

SKPs are written as files like `frame-<n>-<width>x<height>.skp`.

Check that dumps were created:

```sh
ls -lh /tmp/ladybird-skps/*.skp
```

Current behavior: this dumps on render, not as a one-shot debug action.
