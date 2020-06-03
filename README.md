# Redbrick Management Tool

This tool is a holistic attempt of making a unified and modular set up for managing redbrick users.
The goals of the project are to allow the management of LDAP users and synchronizing this LDAP state with all of their redbrick assets.

### Current features to be replicated:
A current list of assets ther require tracking are the following:
 - Home dir creation, movement, and quota management.
 - Webspace creation, movement, and linkage to their home directory
 - Maillist creation, movement, and alias tracking

### Old/New features to be considered:
These behaviours will also have to be added to other systems such as VMs, and or other future services.

### Broken features that we need:
The tool should also be able to handle the end of year rollover. The rollover process can be defined as the following
A rollover requires that a users years paid be decremented by one. Negative and 0 year accounts need to be notified. 0 years paid can be given a year's grace, but negative year accounts need to be suspended. The login shell that does this already exists.

An account that's negative for 3 years (-3) and is of the type student and an account of 5 years old that is marked ass an associate account should be deemed inactive and their data cleared. Club and Soc accounts can be left but they should have a mechanism to regenerate them so that resurrecting dead socs is easier.

### Testing:
The big testing requirement is that we get 100% coverage on testing endpoints and helper functions for the API. That will allow any new clients to be updated and or added instantly with out much effort **TM**.

