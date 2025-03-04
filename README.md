[![Release](https://img.shields.io/github/release/giterlizzi/perl-URI-PackageURL.svg)](https://github.com/giterlizzi/perl-URI-PackageURL/releases) [![Actions Status](https://github.com/giterlizzi/perl-URI-PackageURL/workflows/linux/badge.svg)](https://github.com/giterlizzi/perl-URI-PackageURL/actions) [![Actions Status](https://github.com/giterlizzi/perl-URI-PackageURL/workflows/macos/badge.svg)](https://github.com/giterlizzi/perl-URI-PackageURL/actions) [![License](https://img.shields.io/github/license/giterlizzi/perl-URI-PackageURL.svg)](https://github.com/giterlizzi/perl-URI-PackageURL) [![Starts](https://img.shields.io/github/stars/giterlizzi/perl-URI-PackageURL.svg)](https://github.com/giterlizzi/perl-URI-PackageURL) [![Forks](https://img.shields.io/github/forks/giterlizzi/perl-URI-PackageURL.svg)](https://github.com/giterlizzi/perl-URI-PackageURL) [![Issues](https://img.shields.io/github/issues/giterlizzi/perl-URI-PackageURL.svg)](https://github.com/giterlizzi/perl-URI-PackageURL/issues) [![Coverage Status](https://coveralls.io/repos/github/giterlizzi/perl-URI-PackageURL/badge.svg)](https://coveralls.io/github/giterlizzi/perl-URI-PackageURL)

# URI::PackageURL - Perl extension for Package URL (aka "purl")

## Synopsis

```.pl
use URI::PackageURL;

# OO-interface

# Encode components in PackageURL string
$purl = URI::PackageURL->new(type => cpan, namespace => 'URI', name => 'PackageURL', version => 1.00');

say $purl;  # pkg:cpan/URI/PackageURL@0.0.1

# Parse PackageURL string
$purl = URI::PackageURL->from_string('pkg:cpan/URI/PackageURL@0.0.1');

# exported funtions

$purl = decode_purl('pkg:cpan/URI/PackageURL@0.0.1');
say $purl->type;  # cpan

$purl_string = encode_purl(type => cpan, namespace => 'URI', name => 'PackageURL', version => 1.00');
```

## Install

Using Makefile.PL:

To install `URI::PackageURL` distribution, run the following commands.

    perl Makefile.PL
    make
    make test
    make install

Using App::cpanminus:

    cpanm URI::PackageURL


## Documentation

 - `perldoc URI::PackageURL`
 - https://metacpan.org/release/URI-PackageURL


## Copyright

 - Copyright 2022 © Giuseppe Di Terlizzi
