A quick&dirty port of OpenPGP.js to Google Apps Script
======================================================

The file [OpenPGP-v5.1.0.js](OpenPGP-v5.1.0.js) is the unmodified (OpenPGP.js)[https://openpgpjs.org/]
5.1.0 single-file JS library from https://unpkg.com/browse/openpgp@5.1.0/dist/openpgp.js.

The file [OpenPGP-v5.1.0.gs](OpenPGP-v5.1.0.gs) is a modified version of OpenPGP-v5.1.0.js with some
ad-hoc changes to make it work with Google Apps Script.

The file [Code.gs](Code.gs) is a simple example app that uses OpenPGP.gs to sign
a message.

The [openpgpgs branch](https://github.com/clairexen/OpenPGPgs/tree/openpgpgs) contains the
changes relative to the OpenPGP v5.1.0 release tag.
