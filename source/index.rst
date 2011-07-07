SleekXMPP
#########

SleekXMPP is an XMPP library for Python 3.1+ (and compatible with 2.6+), and
is featured in examples in `XMPP: The Definitive Guide <http://oreilly.com/catalog/9780596521271>`_ 
by Kevin Smith, Remko Tronçon, and Peter Saint-Andre. If you've arrived
here from reading the Definitive Guide, please see the notes on updating
the examples to the latest version of SleekXMPP.

SleekXMPP's design goals and philosphy are:

**Low number of dependencies**
    Installing and using SleekXMPP should be as simple as possible, without having
    to deal with long dependency chains.

    As part of reducing the number of dependencies, some third party modules are
    included with SleekXMPP in the ``thirdparty`` directory. Imports from this
    module first try to import an existing installed version before loading the
    packaged version.

**Every XEP as a plugin**
    Following Python's "batteries included" approach, the goal is to provide support
    for all currently active XEPs (final and draft). Since adding XEP support is done
    through easy to create plugins, the hope is also provide a solid base for
    implementing and creating experimental XEPs as well.
    
**Rewarding to work with**
    As much as possible, SleekXMPP should allow things to "just work" using sensible
    defaults and appropriate abstractions. XML can be ugly to work with, but it doesn't
    have to be that way. 

Roadmap for 1.0
===============

Development on SleekXMPP is currently focused on the 1.0 release which will
feature a stable, supported API. As such, some older APIs are changing or
being replaced in order to make the 1.0 API as reliable and extensible as
practical.

- Upgrade the current roster to interoperate with external data storage and
  work correctly for components. The work for this has already been done and
  can be experimented with now using the ``roster`` branch.
- Cleanup the stream initialization and stream features code. A first
  attempt at this has been made in the ``stream_features`` branch, but some
  more documentation and testing is required.
- Simplify handling ``Iq`` stanzas by introducing exceptions for error and
  timeout handling.

In addition, these features are desired for inclusion in 1.0, but might be
left for 1.1 or later.

- Finish cleaning up the major plugins, such as XEP-0060.
- Add handling for xml:lang attributes for multi-language support.

Active Branches
---------------
- ``develop`` - Contains what will be the next release of SleekXMPP.
- ``roster`` - Upgraded roster that works with components and external data storage.
- ``stream_features`` - Cleans up stream feature negotiation by using more stanza objects.
- ``exceptions`` - Experimental branch that introduces ``IqTimeout`` and
  ``IqError`` exceptions when using ``iq.send()`` style calls. Using this branch
  will likely break a lot of existing code that uses ``Iq`` stanzas.

Get the Code
=============
The latest source code for SleekXMPP may be found on 
`Github <http://github.com>`_ at http://github.com/fritzy/SleekXMPP. Releases are
found in the ``master`` branch, while the latest development version is in
the ``develop`` branch.

Development Releases
---------------------
- `Latest Develop Version <http://github.com/fritzy/SleekXMPP/zipball/develop>`_
- `External Roster (Based on Develop Version) <http://github.com/fritzy/SleekXMPP/zipball/roster>`_
- `Stream Features (Based on Develop Version) <http://github.com/fritzy/SleekXMPP/zipball/stream_feaetures>`_

Stable Releases
----------------
- `1.0 Beta5 <http://github.com/fritzy/SleekXMPP/zipball/1.0-Beta5>`_
- `1.0 Beta4 <http://github.com/fritzy/SleekXMPP/zipball/1.0-Beta4>`_
- `1.0 Beta3 <http://github.com/fritzy/SleekXMPP/zipball/1.0-Beta3>`_
- `1.0 Beta2 <http://github.com/fritzy/SleekXMPP/zipball/1.0-Beta2>`_
- `1.0 Beta1 <http://github.com/fritzy/SleekXMPP/zipball/1.0-Beta1>`_


Contents
========
.. toctree::
   :maxdepth: 2

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

Credits
=======
**Main Author:** Nathan Fritz
    `fritzy@netflint.net <xmpp:fritzy@netflint.net?message>`_, 
    `@fritzy <http://twitter.com/fritzy>`_

    Nathan is also the author of XMPPHP and Seesmic-AS3-XMPP, and is
    a member of the XMPP Council.

**Co-Author:** Lance Stout
    `lancestout@gmail.com <xmpp:lancestout@gmail.com?message>`_, 
    `@lancestout <http://twitter.com/lancestout>`_

**Contributors:**
    - Brian Beggs (`macdiesel <http://github.com/macdiesel>`_)
    - Dann Martens (`dannmartens <http://github.com/dannmartens>`_)
    - Florent Le Coz (`louiz <http://github.com/louiz>`_)
    - Kevin Smith (`Kev <http://github.com/Kev>`_, http://kismith.co.uk)
    - Remko Tronçon (`remko <http://github.com/remko>`_, http://el-tramo.be)
    - Te-jé Rogers (`te-je <http://github.com/te-je>`_)
    - Thom Nichols (`tomstrummer <http://github.com/tomstrummer>`_)


License (MIT)
=============
Copyright (c) 2010 Nathanael C. Fritz

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL
THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
