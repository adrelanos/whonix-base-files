# Whonix base system miscellaneous files #

This package contains several important miscellaneous files, such as
/etc/issue, /etc/motd, /etc/dpkg/origins/whonix,
/etc/skel/.bashrc, /usr/bin/whonix, and others.

Sets the WHONIX environment variable to 1 as well.

Creates version file /var/lib/anon-dist/build_version.

Ships marker files:
* /usr/share/whonix/marker
* /usr/share/anon-dist/marker
## How to install `whonix-base-files` using apt-get ##

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `whonix-base-files`.

```
sudo apt-get install whonix-base-files
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/whonix-base-files). (Replace `package-name` with the actual name of this package.)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`whonix-base-files` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
