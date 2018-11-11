# wazo-libsrtp-packaging

Debian packaging for [libsrtp](https://github.com/cisco/libsrtp) used in Wazo.

## Upgrading

To upgrade tempora:

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Refresh patches
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../srtp_*.orig.tar.gz  --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.

