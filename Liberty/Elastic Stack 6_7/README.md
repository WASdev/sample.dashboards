# Sample configurations and dashboards for Liberty using Elastic Stack 6 and 7
For more information see [“Analyzing logs with Elastic Stack”](https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/twlp_elk_stack.html) in the Liberty Knowledge Center.

## kibana6_7_traffic

Prior to Open Liberty 20.0.0.8, access logs that were included in the JSON logs used a fixed set of fields. Open Liberty 20.0.0.8 adds the option for you to use the fields specified in the `accessLogging` `logFormat` attribute in the JSON logs.

The traffic dashboard depends on the default access log fields. If you want to use our traffic dashboard, include the default set of access log fields in your access log format `('%h %H %A%B %m %p %q %{R}W %s %U')`

You can also build your own custom dashboards (or modify ours) in Kibana if you want to take advantage of the non-default fields.
