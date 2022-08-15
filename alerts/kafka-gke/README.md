# Kafka Alerts for Ops Agent

## Under replicated partitions alert
When there is an under replicated partition for an extended period of time (default is 1 minute), then the cluster is not healthy and cannot guarantee high availability.

## Change in number of ISRs alert
In sync replicas (ISRs) are required for proper failover. The number of in sync replicas should be static, unless the broker cluster is expanding or partitions are removed. If the number of in sync replicas deviates without the broker cluster being modified, you should investigate to maintain high availability.

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
