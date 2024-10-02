Note: the file `capella/README.txt` is included in the "Standalone
developer tools" package for Server builds prior to 7.6.4 (see
MB-50709). This package was initially intended for Capella customers,
hence the README being in the `capella` subdirectory.

Starting with 7.6.4, there are two separate tools packages - dev-tools,
which is the same as what came before; and admin-tools, which
additionally contains tools only necessary for users administering an
on-prem Couchbase Server instance (MB-63171). As the mechanisms for
building those packages are tightly integrated in the Server build, it
made more sense to have both packages' READMEs in the same location,
under `product-texts/couchbase-server`.

The upshot is that `product-texts/capella/tools/README.txt` and
`product-texts/couchbase-server/dev-tools/README.txt` are the same file.
The former should eventually be deleted, but it is still referred to by
Server builds older than 7.6.4 (such as 7.2.x) so it's best to leave it
alone for now.
