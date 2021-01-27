# pris-netbox-scripts

This repository is for scripts related to integrating [PRIS](https://pris.opennms.eu/) with [Netbox](https://github.com/netbox-community/netbox).  It is an extension of [this Discourse thread](https://opennms.discourse.group/t/importing-nodes-from-netbox-via-pris/530)

In the current format, this requisition used the [PostgreSQL JDBC](https://jdbc.postgresql.org/) library that must be put int he `$PRIS_HOME/lib` folder for this to work.

This is just a sample, and you will probably want to adjust if you use any Netbox fields differently. The following assumptions are made in this example:
- Netbox site = OpenNMS "Building" asset field
  - Address is recorded on the Netbox site as a comma-separated "address, city, state, postal code"
- Netbox rack group = OpenNMS "Room" asset field
