# Timestamped

In this repository I give the hash and encrypted version of files for which I want to be able to proof their existence at some point.
`hashes.txt` contains the SHA256 hash of the unencrypted files.
The encrypted files are encrypted using GPG, with a different password for each file.

Checklist for timestamping a file:

1. Copy the file to the timestamped directory
2. Execute `sha256sum <filename> >> hashes.txt` to create the hash
3. Generate and store a passphrase in keepass
4. Execute `gpg -c <filename>` to create the encrypted file
5. Add `hashes.txt` and `<filename>.gpg` to git and commit
6. Push to github
