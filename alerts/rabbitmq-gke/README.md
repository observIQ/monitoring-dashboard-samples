# RabbitMQ Alerts for Ops Agent

## High unacknowledged messages alert
When the message unacknowledged mean is higher than a threshold, then errors or performance issues may arise.

## High unroutable messages alert
When the unroutable message rate is greater than a threshold, then the consumers are not getting every message.

## Low delivered messages alert
When the rate of delivered messages is lower than a threshold, then there may be an issue with a producer or routing logic.

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
