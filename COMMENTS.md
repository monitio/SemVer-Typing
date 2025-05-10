This file is only useful to the people that might be making pull-requests or the developers.

---

Use the VERSIONING.md comments to replace the existing sha code and author with the variable.
You will need to add the version manually after the `v` as bumping it doesn't work.

---

`VERSIONING.md`:
```md
v | [${{ steps.extract_sha.outputs.short_sha }}](https://github.com/monitio/SemVer-Typing/commit/${{ github.sha }})

Triggered by committer: [@${{ github.actor }}](https://github.com/${{ github.actor }})

---
```
