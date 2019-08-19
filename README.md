# Sample dashboards for Liberty
This repository contains the configuration files and dashboards required to set up the Elastic Stack for use with JSON logs from Liberty servers.
For more information see [“Analyzing logs with Elastic Stack”](https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/twlp_elk_stack.html) in the Liberty Knowledge Center.

### Kibana 7's NDJSON format
You may easily convert from *\*.json* to *\*.ndjson* format by using Kibana's smart export feature.
1. Import the was-kibana.json dashboard in the 'Saved Objects' section.
2. Click 'Export *x* objects' which will then download an *export.ndjson* file.
3. Navigate to the directory where you have installed the new ndjson file and use `while IFS= read -r line; do jq -s -c 'sort_by(.type, .id) | .[]' < "export.ndjson" > "was-kibana.ndjson"; done < "export.ndjson"` to sort the newly exported dashboard.
