---
tap: "netsuite"
version: "10-15-2015"

name: "netsuite_manufacturing_routing"
doc-link: https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2015_1/schema/record/manufacturingrouting.html
description: |
  The `{{ table.name }}` table contains info about manufacturing routings.

replication-method: "Full Table"
abstract: false

## Refer to _data/extraction/netsuite/netsuite-permissions.yml for permissions for this table/object.
key: "manufacturing-routing"

attributes:
  - name: "internalId"
    type: "integer"
    primary-key: true
    description: |
      The {{ table.name | remove: "netsuite_" | replace: "_"," " }} ID.

  - name: "Additional fields"
    description: |
      For a list of available attributes, refer to [{{ integration.display_name }}'s documentation]({{ table.doc-link }}){:target="new"}. **Note**: You will need to log into your {{ integration.display_name }} account to view the documentation.
---