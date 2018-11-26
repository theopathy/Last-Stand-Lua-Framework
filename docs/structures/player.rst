Struct: Player 
----------

For subdomains, this is a simple lookup of the project slug, using the subdomain
portion of the request's hostname. This doesn't require symlinks, but it shows
the basic logic that we need to replicate.

When a user navigates to ``http://pip.readthedocs.org/en/latest/``,
we know that they want the pip documentation.
So we simply serve them the documentation:

.. code-block:: lua

  String	name
  String	SteamID
  Float	        Health
  Object	Controller

.. warning::
 1. Struct is read only, use GetPlayer(Controller)
