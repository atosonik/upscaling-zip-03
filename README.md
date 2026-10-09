# upscaling-zip-03

Zip piece 3 of 3 from https://github.com/atosonik/upscaling.git.

Each `.zip` file is under GitHub's 100 MB limit. Together they stay under 500 MB.

## Restore the project

Download every `upscaling-zip-*` repo listed in `SPLIT.json` and unzip all of the archives into one folder:

```bash
mkdir upscaling && cd upscaling
find /path/to/upscaling-zip-repos -name '*.zip' -exec unzip -n {} \;
python chunker.py merge
python pack_app.py --unpack
```

`unzip -n` keeps the first copy of a path. The zip pieces do not overlap.
