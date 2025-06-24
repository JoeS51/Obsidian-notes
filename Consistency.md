**Definition:**
Every read receives the most recent write, or an error

**What it means:**
- All nodes see the same data at the same time
- After a write, any read will return that latest value

**Example:**
You post a comment on a Youtube Video. 
With *strong consistency*, if someone else refreshes the page, they *must* see your comment immediately