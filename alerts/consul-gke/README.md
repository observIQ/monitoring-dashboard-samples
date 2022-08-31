# Consul Alerts for GKE

## Long GC pause alert
When the total GC time exceeds 2 seconds per minute (about 33 million nanoseconds / second), Consul's performance may degrade. This may indicate that Consul is running out of memory.

## Unhealthy cluster alert
When this alert triggers, the local server cluster is considered unhealthy by autopilot. This could indicate a degradation of resources on the host, or could indicate failed leadership elections.


### Creating Notification Channels and User Labels

It is strongly recommended to add notification channels and user labels to the alert policies. The notification channel will set the notification destination if the alert policy is triggered. User labels are used for categorization, and can be used to indicate the severity level.

### User Labels

Supplying user labels could give extra identification information about the firing alert:

i.e.

```json
    "userLabels": {
        "Severity": "Warning"
    }
```

### Notification Channels

The ID of the notification channel to be notified.

```json
    "notificationChannels": [
        "projects/project-id/notificationChannels/1234567"
    ]
```
