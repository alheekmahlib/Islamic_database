# Quran Font ZIP (Git LFS)

This folder is intended to store the Quran font ZIP file via Git LFS. The file is large (>50MB), so it must be committed using Git LFS due to GitHub's size limits.

## Why Git LFS?
- GitHub warns about files over ~50MB and blocks files over 100MB.
- Git LFS stores large files efficiently and avoids bloating the repository.

## One-time setup
```bash
# Install LFS (only needed once per machine)
git lfs install
```

## Tracking ZIPs in this folder
The repository is configured to track ZIP files in this folder via `.gitattributes` using this pattern:

```
Islamic_database/quran_database/Quran[[:space:]]Font/*.zip filter=lfs diff=lfs merge=lfs -text
```

If you need to set it locally as well, you may run:

```bash
git lfs track "Islamic_database/quran_database/Quran Font/*.zip"
# Commit the attributes file if it changed
git add .gitattributes
git commit -m "Track Quran Font ZIPs with Git LFS (local)"
```

Note: The pattern uses `[[:space:]]` in `.gitattributes` to match the space in "Quran Font", but when using `git lfs track` command, you can use quotes or escape the space as shown above.

## Add the ZIP file
Place your ZIP file into this folder (any filename ending with `.zip`), then commit and push:

```bash
# Example filename: Quran_Font.zip
git add "Islamic_database/quran_database/Quran Font/Quran_Font.zip"
git commit -m "Add Quran Font ZIP via Git LFS"
git push
```

> Note: This PR does not include the ZIP itself. You should add it locally and push via LFS.

## External reference (optional)
If you are sourcing the file externally, a reference link was provided:
- Google Drive: https://drive.google.com/file/d/1VVysZzrPmSXwJUENB0rrREkRpJaYf6UP/view?usp=sharing
