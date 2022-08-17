
# Alerts for Memcached in GKE

## High Evictions

if `memcached_items_evicted_total/counter` increases by 1 or more that shows that items are being evicted due to high memory usage and should be a cause for concern.

## No Connections

if `memcached_current_connections/gauge` reaches 0 that should be cause for concern because memcached should always have at least 1 connection.

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

### Notification Channels

The ID of the notification channel to be notified.

```json
    "notificationChannels": [
        "projects/project-id/notificationChannels/1234567"
    ]
```
