# MySQL Alerts for Ops Agent

## High slow queries rate
If the number of slow queries becomes high, it indicates performance issues. You may check the MySQL slow query logs to investigate the cause.

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
