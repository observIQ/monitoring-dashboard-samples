# Alerts for Zookeeper in GKE

## High Average Latency

If `prometheus.googleapis.com/avg_latency/gauge` is 100ms or higher, it shows that the server can't keep up with demand and performance improvements should be sought after.

## High fsync Duration

If the fsync duration is above an amount dependent on your environment it could show there is an issue writing to files.

## Low Open File Descriptors

If `prometheus.googleapis.com/open_file_descriptor_count/gauge` is about to hit `prometheus.googleapis.com/max_file_descriptor_count/gauge` zookeeper will not be able to handle any new requests and will fail to connect new clients.

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
