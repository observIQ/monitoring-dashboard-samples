# Alerts for PostgreSQL in GKE

## Database Size Too Large
If the database is growing larger than expected, it may signal excess data being stored or excess records not being properly removed by an application.
By default, this alert triggers when the database's size exceeds 100 GB.


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
        "projects/project-id/notificationChannels/1234567
    ]
```
