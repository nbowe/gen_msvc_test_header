gen_msvc_test_header
====================
Google Test is a great testing framework for C++,
but it doesnt play nicely with msvc and static libraries.
see http://code.google.com/p/googletest/wiki/Primer#Important_note_for_Visual_C++_users

This python script can be used to generate a header from a static library.
This header has appropriate pragmas to force the linker to link in all the tests from the static library.


Usage
-----
> gen_msvc_test_header.py libfile headerfile
Then just include that header in your test harness.

I recommend you run this as a post build step for your static library.


TODO
----
 * upload a py2exed version for those people that dont have python installed.
 * add extra test frameworks. Ive had this same problem with other ones in the past
