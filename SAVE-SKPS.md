# Save SKPs

Use `--dump-skp` to load a page, dump a single full-page SKP, and exit.

Run the built app directly:

```sh
Build/release/bin/Ladybird.app/Contents/MacOS/Ladybird \
  --disable-http-disk-cache \
  --dump-skp /tmp/example.skp \
  https://example.com
```

The command:

- loads exactly one URL
- renders a full-page display list through the screenshot-style off-screen path
- waits briefly for a post-load paint to settle before capturing
- writes one `.skp` file to the path you passed
- exits when the dump finishes

Notes:

- `--dump-skp` is a headless one-shot mode.
- It cannot be combined with `--headless`.
