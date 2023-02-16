---
description: Stop listening for messages posted to the given channels
---

# UNSUBSCRIBE

## Syntax

    UNSUBSCRIBE [channel [channel ...]]

**Time complexity:** O(N) where N is the number of clients already subscribed to a channel.

Unsubscribes the client from the given channels, or from all of them if none is
given.

When no channels are specified, the client is unsubscribed from all the
previously subscribed channels.
In this case, a message for every unsubscribed channel will be sent to the
client.
