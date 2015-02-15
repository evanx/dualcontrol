See https://github.com/evanx/vellum/wiki/DualControl

For (un)related articles, see https://github.com/evanx/vellum/wiki

Commmon utilities were copied from <a href="https://github.com/evanx/vellum">github.com/evanx/vellum</a> to <a href="https://github.com/evanx/vellumcore">github.com/evanx/vellumcore</a>, as a dependency for other projects, including this.

This was originally copied from <a href="https://github.com/evanx/vellum/tree/master/src/dualcontrol">vellum/src/dualcontrol</a>. However it is possible that more recent changes to the code were made there, for the purposes of the <a href="https://github.com/evanx/vellum/wiki/DualControl">Dual Control</a> article.

We use a JCEKS keystore to store data-encrypting keys, protected by split-knowledge passwords. We use client-authenticated SSL connections for custodians to submit partial passwords, to generate data-encrypting keys, and thereafter load a key from this keystore.

This code was integrated into a production system by myself in 2013, for the purposes of PCI DSS compliance, which was achieved. It is Apache-licensed to enable such "forks," for integration with proprietary production code.

On this subject, also see <a href="http://github.com/evanx/keyserver">github.com/evanx/keyserver</a> - a re-implementation of dualcontrol in Node.js. It provides a secure "vault" server with client-authenticated HTTPS access. It uses Redis to store encrypted data, and the encryption keys. Encryption keys are protected by split-knowledge passwords, hashed with PDKDF2, and encrypted using AES.

For technical articles and sample code: https://github.com/evanx/vellum/wiki
