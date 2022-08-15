# Kafka Alerts for Ops Agent

## Under replicated partitions alert
When there is an under replicated partition for an extended period of time (default is 1 minute), then the cluster is not healthy and cannot guarantee high availability.

### Notification Channels
For all alerts, a notification channel needs to be set up or the alert will fire silently.

### User Labels
User labels can be used for these policies by modifying the userLabels fields of the policies. i.e.

```json
{ 
  "userLabels": {
    "datacenter": "central"
  }
}
```
