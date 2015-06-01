# What is this?

A single file which allows you to write:

    log::debug << "Hello world!" << std::endl;
    log::info << "What do you think? I'm Gaya?" << std::endl;

Moreover, there is a `VERBOSITY` level you can set to for example `INFO` which subsequently renders all calls to `log::debug` to `/dev/null`.

How does it then display this?

    [18:32:43] INFO: Hello world!

If you also want to print the name of the process or the date, adjust the file accordingly.

## Does it work in all cases?

There are probably some corner cases which don't work. However, a lot will work. It's no problem to write code statements for example:

    log::debug << flag ? "blah" : "foo" << std::endl;

There might be some issues with literals when writing them to `/dev/null`.
    
    log::debug << 4 << std::endl;

Feel free to submit issues, but make sure they won't make it many more lines of code. The beauty is in the fact that only a few defines are required right now.

# Copyrights

The copyrights (2015) belongs to the team of Distributed Organisms B.V. and are provided under an noncontagious open-source license:

* Authors: Anne van Rossum
* Date: 17 Apr. 2015
* License: LGPL v3+, Apache, or MIT, your choice
* DoBots B.V., http://www.dobots.nl
* Rotterdam, The Netherlands


