## Setting up API Management Service

In this section, we will be setting up an APIM Instance in a private Virtual Network with the APIs and Developer portal only reachable from within the network.

The hostnames for the API and the Dev portal will be set up with SSL Certs obtained from a known CA authority (Let's Encrypt)

This will simplify things in the App Gateway without having to deal with CA certs since Let's Encrypt is a well known Certificate Authority.

