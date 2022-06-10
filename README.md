A quick&dirty port of OpenPGP.js to Google Apps Script
======================================================

The file [OpenPGP-v5.3.0.js](OpenPGP-v5.3.0.js) is the unmodified [OpenPGP.js](https://openpgpjs.org/)
5.3.0 single-file JS library.

The file [OpenPGP-v5.3.0.gs](OpenPGP-v5.3.0.gs) is a modified version of OpenPGP-v5.3.0.js with some
ad-hoc changes to make it work with Google Apps Script.

The file [Code.gs](Code.gs) is a simple example app that uses OpenPGP.gs to sign
a message.

The [openpgpgs-v5.3.0](https://github.com/clairexen/OpenPGPgs/tree/openpgpgs-v5.3.0) branch contains the
changes relative to the OpenPGP.js v5.3.0 release tag.


Re-generating output files
--------------------------

```
V=v5.3.0
mkdir output

git checkout openpgpgs-$V
npm install
cp dist/openpgp.js output/OpenPGP-$V.gs
cp dist/openpgp.min.js output/OpenPGP-$V.min.gs

git checkout openpgpjs-$V
npm install
cp dist/openpgp.js output/OpenPGP-$V.js

git checkout main
cp output/OpenPGP-$V.{gs,min.gs,js} .
diff -u OpenPGP-$V.{js,gs} > OpenPGP-$V.js2gs.diff
```
