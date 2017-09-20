# ocp-on-osp
Heat Templates for Deploying OCP on OSP.

This is an extremely simplified version of the "official" OpenShift on
OpenStack heat templates that we use in the SA labs at Red Hat. It is
based on the OpenShift on OpenStack Reference Architecture, but only
includes components which are designed to be scaled. It has the following limitations:

1. Does not include network setup, ssh key setup, the bastion setup,
or the load balancer setup. For those, refer to the manual
instructions in the Reference Architecture.

2. Does not include a working DNS setup. In the labs, we use dnsmasq
on the bastion for that.

3. Does not include Floating IPs. We reuse the Floating IPs which are
pre-provisioned in the load balancer.

4. Most importantly, these templates only provision the instances and
their supporting storage. Once these heat templates are deployed, we run
the Ansible byo playbooks from the bastion host to install and scale
the hosts.


