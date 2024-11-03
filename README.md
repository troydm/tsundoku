# tsundoku
Simple Perl Dancer2 based Web EBook Server.
Tested only on *Linux* but should work on any *Unix* platform.
Requires only modern 5.10+ Perl version and ImageMagic with pdf/djvu reading capability installed.
Only uses DBI, DBM::SQLite, Dancer2 and Template::Toolkit CPAN dependencies

## NOTE

Make sure that you have read rights for PDF in /etc/ImageMagic-6/policy.xml configuration file

Like this:

    <policy domain="coder" rights="read" pattern="PDF" />


## WARNING

This serves pretty much any file via web from folder and sub-folders and wasn't heavily tested for security robustness so use it on your own risk.

## Installation

To install just run this command:

    $ sudo cpanm DBI DBD::SQLite Dancer2 Dancer2::Plugin::Auth::Extensible Template::Toolkit
    $ git clone https://github.com/troydm/tsundoku.git
    $ chmod +x ./tsundoku/tsundoku

## Usage

Go to your ebook folder and run tsundoku command

Following are examples on how to run tsundoku on different host/port:

    $ tsundoku
    $ tsundoku localhost:8080
    $ tsundoku 7080


## License

[MIT](http://opensource.org/licenses/MIT)
