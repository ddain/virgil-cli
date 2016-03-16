NAME
====

**virgil** -- command line tool for using Virgil Security full stack
functionality.

SYNOPSIS
========

**virgil** *command* \[*command\_opts*\] \[*command\_args*\]

DESCRIPTION
===========

The **Virgil** program is a command line tool for using Virgil Security
stack functionality:

-   encrypt, decrypt, sign and verify data;
-   interact with Virgil Keys Service;
-   interact with Virgil Private Keys Service.

COMMON COMMANDS
===============

**keygen**  
Generate Private Key with given parameters.

**key2pub**  
Extract Public Key from the Private Key.

**encrypt**  
Encrypt data for given recipients which can be defined by Virgil Keys
and by passwords.

**decrypt**  
Decrypt data for given recipient which can be defined by Virgil Public
Key or by password.

**sign**  
Sign data with Private Key.

**verify**  
Verify data and signature with Public Key.

IDENTITY SERVICE COMMANDS
=========================

**identity-confirm**  
Confirmation of the Identity. Returns validation\_token which is
required for operations with Cards and confirmed identity:  
1. [`card-create(1)`](../markdown/card-create.1.md);  
1. [`card-revoke(1)`](../markdown/card-revoke.1.md);  
1. [`public-key-revoke(1)`](../markdown/public-key-revoke).

**identity-validate**  
Validates the passed token. Checks whether validation\_token is valid.
It has time and usage limits.

KEYS SERVICE COMMANDS
=====================

**public-key-get**  
Get user's Virgil Public Key from the Virgil Keys service.

**public-key-revoke**  
Revoke Public Key’s data. Within one-to-many model we can have Cards
with a single Public key and connected with public-key-id. Instead of
deleting every Card one at a time we can delete all the Cards connected
with Public Key ID.

VIRGIL CARD SERVICE COMMANDS
============================

**card-create**  
Create a Virgil Card. Creates a Card with a confirmed Identity. This
means identity-verify; identity-confirm.

**card-get**  
Get user's Virgil Card from the Virgil Keys service.

**card-search**  
Search Card by email, search with criteria:  
1. Including Cards with unconfirmed Identity;  
1. Search for Cards which have signed some other Cards.  

**card-search-app**  
Search for Application Cards.

**card-sign**  
Sign a Virgil Card. We can start trusting another Card by signing it.

**card-unsign**  
Untrust a Virgil Card Cancel sign of an already signed Card.

**card-revoke**  
Revoke a Virgil Card by card-id.

PRIVATE KEYS SERVICE COMMANDS
=============================

**private-key-add**  
Add existing Private Key to the Private Keys Service.

**private-key-get**  
Get Private Key from the Virgil Private Keys Service.

**private-key-del**  
Delete Private Key object from the Private Keys Service.

SEE ALSO
========

[`keygen(1)`](../markdown/keygen.1.md),  
[`key2pub(1)`](../markdown/key2pub.1.md),  
[`encrypt(1)`](../markdown/encrypt.1.md),  
[`decrypt(1)`](../markdown/decrypt.1.md),  
[`sign(1)`](../markdown/sign.1.md),  
[`verify(1)`](../markdown/verify.1.md),  
[`identity-confirm(1)`](../markdown/identity-confirm.1.md),  
[`identity-valid(1)`](../markdown/identity-valid.1.md),  
[`public-key-get(1)`](../markdown/public-key-get.1.md),  
[`public-key-revoke(1)`](../markdown/public-key-revoke.1.md),  
[`card-create(1)`](../markdown/card-create.1.md),  
[`card-get(1)`](../markdown/card-get.1.md),  
[`card-search(1)`](../markdown/card-search.1.md),  
[`card-search-app(1)`](../markdown/card-search-app.1.md),  
[`card-trust(1)`](../markdown/card-trust.1.md),  
[`card-untrust(1)`](../markdown/card-untrust.1.md),  
[`card-revoke(1)`](../markdown/card-revoke.1.md),  
[`private-key-add(1)`](../markdown/private-key-add.1.md),  
[`private-key-get(1)`](../markdown/private-key-get.1.md),  
[`private-key-del(1)`](../markdown/private-key-del.1.md)