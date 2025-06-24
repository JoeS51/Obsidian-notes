**Definition:**
Every request (read or write) receives a non-error response, even if it's not the most recent data

**What it means:**
- The system continues to respond, even if some data is out of sync
- No guaranteed freshness, but always responsive

**Example:**
You like a video, but due to a delay in syncing, you don’t see your like reflected right away. The server still responds with something — it doesn’t fail or error out.