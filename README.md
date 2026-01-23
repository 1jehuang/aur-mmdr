# AUR Packaging for mmdr

This repo contains the PKGBUILD for the prebuilt binary package.

To publish to AUR:
1) Ensure you have an AUR account and SSH key installed.
2) Clone the AUR repo and push these files.

Example:
```bash
ssh -T aur@aur.archlinux.org

# Create the package repo (first time only)
ssh aur@aur.archlinux.org setup-repo mmdr-bin

git clone ssh://aur@aur.archlinux.org/mmdr-bin.git
cp PKGBUILD .SRCINFO mmdr-bin/
cd mmdr-bin
makepkg --printsrcinfo > .SRCINFO
git add PKGBUILD .SRCINFO
git commit -m "Update to v0.1.0"
git push
```

If you prefer to build from source instead of using the binary, we can create a non-`-bin` package as well.
