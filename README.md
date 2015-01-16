flowdoh
=======

Ansible role to manage [flowdoh](http://sourceforge.net/projects/flowdoh/)
plugin for [nfsen](http://nfsen.sourceforge.net).

Requirements
------------

No external requirements.
Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

This role uses the following variables from the sfromm.nfsen role:

- **nfsen_user**:  The user that nfsen runs as.
* **nfsen_group**: The group id that nfsen runs as.
* **nfsen_backend_plugindir**: The path where nfsen backend plugins are
  installed.
* **nfsen_frontend_plugindir**: The path where nfsen frontend plugins
  are installed.

The variables specific to the *flowdoh* role are the following:

- **flowdoh_url**: URL to where *flowdoh* may be downloaded from.
- **flowdoh_version**: The name of the downloaded file.  For example,
  this may be /FlowDoh_1.0.2.tar.gz/.
- **flowdoh_src_dir**: The path to where *flowdoh* source will be
  downloaded to.
- **flowdoh_num_toptalkers**: The number of top talkers to look for.
- **flowdoh_num_flows_listed**: Number of flows to list in frontend.
- **flowdoh_email_address**: Email address to send alerts to.
- **flowdoh_email_subject**: Email subject to use for alerts.
- **flowdoh_email_alerts**: Whether to send email alerts.
- **flowdoh_alert_bytes_percent**: Threshold for bytes to alert at.
- **flowdoh_alert_packets_percent**: Threshold for packets to alert at.
- **flowdoh_alert_flows_percent**: Threshold for flows to alert at.

Dependencies
------------

Depends on sfromm.nfsen.  At this time, this dependency is not made
explicit in meta/main.yml.

Example Playbook
----------------

Example:

    - hosts: servers
      roles:
      - { role: sfromm.nfsen }
      - { role: sfromm.flowdoh }

License
-------

GPLv2

Author Information
------------------

See https://github.com/sfromm
