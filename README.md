# ClipsNeko Linux Live CD
The ClipsNeko Linux Live/Rescue DVD.

## Build instructions
The first, you have to use one Arch-based Linux operating system.

The package required:
- base-devel
- archiso

Then clone this repository, as:
```
git clone https://github.com/ReSpringClipsNeko/ClipsNeko-LiveCD
cd ClipsNeko-LiveCD
```

Then setup the local source repository by look at the file [clipsneko-pkglist](./clipsneko-pkglist), find these packages in [our PKGBUILD repo](https://github.com/ReSpringClipsNeko/ClipsNeko-PKGBUILDS), build them and place **all required .pkg.tar.zst** to `/tmp/cnrepo/`, which `mkarchiso` can reach.

Use this command to build from `profile`, output the final image to `~/out` directory, work at `/tmp/clipsneko-tmp` for more efficient...
```
mkdir ~/out
sudo mkarchiso -v -w /tmp/clipsneko-tmp -o ~/out ./profile
```

## Acknowledgments
- [archiso](https://wiki.archlinux.org/title/archiso)

