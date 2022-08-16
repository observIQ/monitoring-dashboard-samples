# MySQL Alerts for Ops Agent

## Connection Errors
Connection errors mean a connection failed to be established. This indicates applications may be having trouble connecting to your MySQL database. See the `error` label on the time-series that triggers the alert for a more specific cause.

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
