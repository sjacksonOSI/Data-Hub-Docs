---
uid: data-transfer-statuses
---

# Data transfer statuses

The status and progress of a data transfer is shown in the `Transfer Overview` section of the **Manage Agent** tab. The following table lists these data statuses and their meanings.

|Data status | Meaning|
|---------|-----------|
| Sending Historical Data | Historical data is being sent. |
| Sending Streaming Data | PI point data is currently being streamed. |
| Backfilling Streaming Gap | Data streaming is resuming. Data will be backfilled from the interrupted time to now and will then continue with normal streaming.|
| Uncategorized Error  | Data transfer has been interrupted due to an unknown cause.|
| Streaming Error Consumer Removed | Due to an error during streaming, the consumer has been removed. |
| Streaming Error Update Queue Overflow | Agent not receiving streaming data from PI Data Archive.|
| Streaming Error Signup Dropped | Agent not receiving streaming data from PI Data Archive.|
| Streaming Error Producer Removed | Agent not receiving streaming data from PI Data Archive.|
| Streaming Error Unknown | An unknown error occurred during data streaming.|
| PI Point Type Change Detected | PI point type change was detected during data transfer. See [Point type change](xref:PItoDHSync#pi-point-type-change) for more information.|
| Creating Streams | Streams are in the process of being created.|
| Done | Data transfer is complete. Streams have been created.|
