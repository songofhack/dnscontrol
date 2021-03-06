---
name: DnsProvider
parameters:
  - name
  - nsCount
---

DnsProvider indicates that the specifid provider should be used to manage
records for this domain. The name must match the name used with [NewDnsProvider](#NewDnsProvider).

The nsCount parameter determines how the nameservers will be managed from this provider.

Leaving the parameter out means "fetch and use all nameservers from this provider as authoritative". ie: `DnsProvider("name")`

Using `0` for nsCount means "do not fetch nameservers from this domain, or give them to the registrar".

Using a different number, ie: `DnsProvider("name",2)`, means "fetch all nameservers from this provider,
but limit it to this many.

See [this page]({{site.github.url}}/nameservers) for a detailed explanation of how DNSControl handles nameservers and NS records.

