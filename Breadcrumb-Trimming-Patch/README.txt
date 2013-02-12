Breadcrumb Trimming Patch
-------------------------

Summary
-------
These patches are built for Drupal 7 and is used to dynamically trim your sites
breadcrumbs to some maximum length, defined by you on the settings page.

The logic behind this module works like this:
* Get total length for breadcrumbs are definied in the breadcrumbtrimming_nodehierarchy_7.x-2.x.patch file
* Get total number of breadcrumbs for that node
* Set allowed space for each breadcrumb and allocate that space dynamically.
  This allows for the maximum amount of characters to be used, but never go over
  the limit that was set by the user.
	
Requirements
------------
* Drupal 7
* Node Hierarchy 7.x-2.x (http://drupal.org/project/nodehierarchy)
* Delta 7.x-3.x (http://drupal.org/project/delta)

Installation
------------
Patch the nodehierarchy module (within the nodehierarchy folder)
* patch -p1 < breadcrumbtrimming_nodehierarchy_7.x-2.x.patch

Patch the delta module (within the delta folder)
* patch -p1 < breadcrumbtrimming_delta_7.x-3.x.patch

Author
------
Craig Vanderlinden
    Drupal.org - VanD
    Twitter - cvanderlinden
    Website - cvanderlinden.com