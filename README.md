> note: this site is currently in setup phase!

radsecproxy is a generic RADIUS proxy that in addition to usual RADIUS UDP transport, also supports TLS (RadSec), as well as RADIUS over TCP and DTLS. The aim is for the proxy to have sufficient features to be flexible, while at the same time to be small, efficient and easy to configure.

The proxy was initially made to be able to deploy RadSec (RADIUS over TLS) so that all RADIUS communication across network links could be done using TLS, without modifying existing RADIUS software. This can be done by running this proxy on the same host as an existing RADIUS server or client, and configure the existing client/server to talk to localhost (the proxy) rather than other clients and servers directly.

There are however other situations where a RADIUS proxy might be useful. Some people deploy RADIUS topologies where they want to route RADIUS messages to the right server. The nodes that do purely routing could be using a proxy. Some people may also wish to deploy a proxy on a site boundary. Since the proxy supports both IPv4 and IPv6, it could also be used to allow communication in cases where some RADIUS nodes use only IPv4 and some only IPv6.
