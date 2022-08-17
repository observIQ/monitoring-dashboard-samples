# Nginx Alerts for GKE

## High connections dropped alert
Connections dropped value is derived from the connections accepted minus the connections handled. This value should be near 0. When this value is rising, then this means you may have a resource saturation problem.

## High request rate alert
The request rate is derived from the requests metrics taken as a rate of every 5 minutes. This value should be monitored beforehand to understand what qualifies as a normal request rate so a threshold can be established. When request rate is above this threshold, then that means there is a large spike in traffic which logs can help diagnose if these are nefarious requests.

The "thresholdValue" can be adjusted depending on what is considered to be a high request rate.

## Low request rate alert
The request rate is derived from the requests metrics taken as a rate of every 5 minutes. This value should be monitored beforehand to understand what qualifies as a normal request rate so a threshold can be established. When request rate is below this threshold, then that means there is an environment problem that are limiting the request rates.

The "thresholdValue" can be adjusted depending on what is considered to be a low request rate.

### Creating notification Channels and User Labels

Whether these alert policies are being used as standalones or base templates for a deployment strategy like terraform, one thing that should be utilized is notification channels and user labels.

### User Labels

Supplying user labels could give extra identification information about the firing alert:

i.e.

```json
    "userLabels": {
        "datacenter": "central"
    }
```

#### Notification Channels

The ID of the notification channel to be notified.

```json
    "notificationChannels": [
        "projects/project-id/notificationChannels/1234567"
    ]
```
