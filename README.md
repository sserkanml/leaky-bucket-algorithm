# Leaky Bucket Algorithm

The Leaky Bucket algorithm is a traffic shaping algorithm used to control the flow of data in a network. It regulates the rate at which data is allowed to flow in a controlled manner. If the incoming data rate exceeds a certain limit, excess data is either dropped or delayed.

## How it Works

- The algorithm uses a "leaky bucket" as a buffer to hold a maximum amount of data that can be transmitted in one second.
- Each incoming data packet is added to the bucket.
- If the bucket is full, excess data is either dropped or delayed.
- Every second, data is removed from the bucket at a fixed rate (max rate).

The Leaky Bucket algorithm is used to control sudden bursts of traffic and to ensure a steady flow of data.

## Implementation in Python

```python
import time

class LeakyBucket:
    def __init__(self, capacity, rate):
        # Initialize the leaky bucket with given capacity and rate
        # ...
    
    def _update_tokens(self):
        # Update the number of tokens in the bucket
        # ...
    
    def allow_request(self, tokens_requested):
        # Check if the request can be allowed or denied
        # ...

# Example Usage
bucket = LeakyBucket(capacity=10, rate=1)

for _ in range(15):
    if bucket.allow_request(1):
        print("Request allowed.")
    else:
        print("Request denied. Wait for a moment.")
        time.sleep(1)
```
