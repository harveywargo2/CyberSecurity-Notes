# References
- https://learn.microsoft.com/en-us/azure/sentinel/detect-threats-custom
- Custom Detection & Analytics References
	- https://learn.microsoft.com/en-us/azure/sentinel/detect-threats-custom
	- https://learn.microsoft.com/en-us/azure/sentinel/map-data-fields-to-entities
	- https://learn.microsoft.com/en-us/azure/sentinel/surface-custom-details-in-alerts
	- https://learn.microsoft.com/en-us/azure/sentinel/customize-alert-details
	- https://learn.microsoft.com/en-us/azure/sentinel/create-nrt-rules
	- https://learn.microsoft.com/en-us/azure/sentinel/ingestion-delay
	- https://learn.microsoft.com/en-us/azure/sentinel/detect-threats-built-in
- Setup & Data Connector References
	- https://learn.microsoft.com/en-us/training/modules/intro-to-azure-sentinel/
	- https://www.youtube.com/watch?v=fG1ECj96AXk&list=PLq4pKxhoJLnH2TdQl-5GFbz3R5T1V52SU
	- https://learn.microsoft.com/en-us/azure/sentinel/skill-up-resources
	- https://learn.microsoft.com/en-us/azure/sentinel/incident-investigation
- Azure Lighthouse References
	- https://learn.microsoft.com/en-us/azure/lighthouse/overview
	- https://www.youtube.com/watch?v=GULpLp9nqNQ
	- https://learn.microsoft.com/en-us/azure/lighthouse/concepts/architecture
- Ingestion Delay
	- https://learn.microsoft.com/en-us/azure/sentinel/ingestion-delay
- Entities 
	- https://learn.microsoft.com/en-us/azure/sentinel/map-data-fields-to-entities
	- https://learn.microsoft.com/en-us/azure/sentinel/entities-reference
	- https://learn.microsoft.com/en-us/azure/sentinel/entities
	- https://learn.microsoft.com/en-us/azure/sentinel/map-data-fields-to-entities
- Customization
	- https://learn.microsoft.com/en-us/azure/sentinel/surface-custom-details-in-alerts
	- https://learn.microsoft.com/en-us/azure/sentinel/customize-alert-details


# Limits 
- The size limit for an entire alert is _64 KB_
- Alerts that grow larger than 64 KB will be truncated. As entities are identified, they are added to the alert one by one until the alert size reaches 64 KB, and any remaining entities are dropped from the alert
- Set **Run query every** to control how often the query is run—as frequently as every 5 minutes or as infrequently as once every 14 days.
- Set **Lookup data from the last** to determine the time period of the data covered by the query—for example, it can query the past 10 minutes of data, or the past 6 hours of data. The maximum is 14 days.
- Rule Limit to 512
- Rule Engine only looks at TimeGenerated (Don't over write aka leave it as ingestion time)
- Rule engine can't talk to anything outside a light housed workspace
- No write to table capability
