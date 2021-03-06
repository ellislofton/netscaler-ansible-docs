# Using generic Ansible modules

The NetScaler Ansible modules try to accomodate the most frequently
changing items of the NetScaler configuration. Things that change from
day to day operations.

In this section we investigate how to leverage Ansible standard modules
to configure NetScaler to cover the cases where the user needs to use
Ansible for a NetScaler configuration entity that does not have a
specialized Ansible module.

We make use of the Ansible uri module mainly to issue NITRO API requests
to NetScaler.

The solutions we present here do have drawbacks compared to the use of
specialized NetScaler Ansbile modules, such as not having a check mode
operation, having to check for NITRO errors and handle them accordingly,
and also having to account for particularities that a configuration
entity may have.

All these issues are taken care of in the NetScaler specific modules but
in the solutions we present here the user has to deal with all of these.

The source files referenced in the following sections along with more
examples can be found on this [github repository](https://github.com/citrix/ansible-nitro-api-calls).

## References

* [NITRO API overview](http://docs.citrix.com/en-us/netscaler/12/nitro-api/nitro-rest.html)
* [NITRO API reference](https://developer-docs.citrix.com/projects/netscaler-nitro-api/en/12.0/)