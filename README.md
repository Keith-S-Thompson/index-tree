This is `index-tree`, written by Keith Thompson, Keith.S.Thompson@gmail.com

It's a Perl script that generates index files for a specified
directory tree, storing information in a created `.index` directory.
For example, all `.c` files are listed in `.index/c`.

Invoke with `-help` to display the following usage message:

    Usage: index-tree [options] directory
    Generate index information for the specified directory and all its
    descendents, stored in .index subdirectory.
    Options may be abbreviated uniquely
    Options:
        -help          Show this message and exit.
        -skip-rcs      Ignore any RCS directories and their contents
        -skip-cvs      Ignore any CVS directories and their contents
        -skip-svn      Ignore any .svn directories and their contents
        -skip-hg       Ignore any .hg directories and their contents (Mercurial)
        -skip-git      Ignore any .git directories and their contents
        -skip-version-control
                       Ignore all of the above
        -ignore-case   Treat foo.C and foo.c as having the same suffix
        -debugging     Show debugging output