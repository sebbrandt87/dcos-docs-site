---
layout: layout.pug
navigationTitle: CLI References
title: CLI References
menuWeight: 60
notes: Code generated by docgen.go, DO NOT EDIT
enterprise: true
beta: true
origin: github.com/mesosphere/dcos-storage/cli/pkg/cmd/cmd_storage.go
excerpt: Manage storage volumes, volume profiles and volume providers.
---
#include /services/include/beta-software-warning.tmpl

## dcos storage

Manage storage volumes, volume profiles and volume providers.

### Synopsis

The DC/OS Storage Service (DSS) manages persistent storage in the DC/OS
cluster. This subcommand allows you to interact with the DSS in order to create
volume providers, volume profiles and volumes.

To get going you'll need to:
- configure a *volume provider* to expose storage capacity to the cluster.
- configure a *volume profile* that selects storage capacity from the provider.
- create a *volume* using the new profile.

We explain each of these concepts below.

A volume provider manages storage capacity from which individual volumes can be
carved. Some examples of storage are: LVM2 volume groups, the Amazon EBS
service, etc. In order to expose storage to the DSS you need to configure a
volume provider. Once you have created a volume provider its storage capacity
becomes available inside your DC/OS cluster. You can read more about volume
providers by running `dcos storage provider --help`.

Volumes are configured using volume profiles. Before you can create individual
volumes using your volume providers, you need to create volume profiles.
Administering a small number of volume profiles is simpler than configuring
every volume individually. A volume profile defines properties shared by all
its volumes such as RAID level, volume provider type (e.g., EBS, LVM2, etc.),
etc. Different volumes in the same profile can have different sizes, but they
cannot have different configurations. You can find out more information on
volume profiles by running `dcos storage profile --help`.

Once you've created a volume provider and a volume profile you are ready to
create a volume. Each volume belongs to a single volume profile. The volume
profile specifies which volume providers can create the volume as well as
volume properties such as RAID level and stripe size. The size of a volume is
given when it is created along with its name and volume profile. Read more
about volume provider by running `dcos storage volume provider --help`.

```bash
dcos storage [flags]
```

### Options

Name | Description
--- | ---
`--info` | Display binary info

### Options inherited from parent commands

Name | Description
--- | ---
`-h`,`--help` | Help for this command.
`--timeout` duration | Override the default request timeout. (default 55s)

