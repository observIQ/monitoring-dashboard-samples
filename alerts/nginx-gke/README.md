# Nginx Alerts for Ops Agent

## High connections dropped alert
Connections dropped value is derived from the connections accepted minus the connections handled. This value should be near 0. When this value is rising, then this means you may have a resource saturation problem.

## High request rate alert
The request rate is derived from the requests metrics taken as a rate of every 5 minutes. This value should be monitored beforehand to understand what qualifies as a normal request rate so a threshold can be established. When request rate is above this threshold, then that means there is a large spike in traffic which logs can help diagnose if these are nefarious requests.

The "thresholdValue" can be adjusted depending on what is considered to be a high request rate.

## Low request rate alert
The request rate is derived from the requests metrics taken as a rate of every 5 minutes. This value should be monitored beforehand to understand what qualifies as a normal request rate so a threshold can be established. When request rate is below this threshold, then that means there is an environment problem that are limiting the request rates.

The "thresholdValue" can be adjusted depending on what is considered to be a low request rate.

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
