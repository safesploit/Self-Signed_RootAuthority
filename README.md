# Repository of self-signed root authorities or master signing keys

Files in this repository should be validated before use.
Download the repository contents and validate using the following:



# Checksum Validation of Repositry: SHA512

    $ cd ~/.../Self-Signed_RootAuthority-main

    $ find -type f ! -iname "SHA512SUMS.new" -exec shasum -a 512 "{}" + > SHA512SUMS.new

    $ diff SHA512SUMS SHA512SUMS.new 


\n

The expected output of $diff is that if checksums (lines) match, then nothing is output!




# GPG Importing Software Signing Key and Verifying SHA512SUMS

Master Signing keyID: **0CB54A16295A59F7**

Software Signing keyID: **ADE59E4B52BF9D95**

_ADE59E4B52BF9D95 has been signed with 0CB54A16295A59F7_

## GPG Instructions

    $ gpg --keyserver [URL] --recv-key ADE59E4B52BF9D95
    $ gpg --verify SHA512SUMS

or,

    $ gpg --import ~/ADE59E4B52BF9D95.asc
    $ gpg --verify SHA512SUMS
