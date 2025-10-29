# Data Lake Gen2

Downloaded product2.json and uploaded it to blob storage then enabled hierarchical namespace and support Azure Data Lake Storage Gen by upgrading to Data Lake Gen2

## What I learned:
Turning on hierarchical namespace makes folders behave like real directories. It also lets you do folder actions safely (all at once, without errors) and gives you file-permission controls like those in Linux. Adding a second file post-upgrade confirms seamless continuity: existing blobs still work, and new ones gain hierarchical benefits such as directory ACLs (Access Control Lists). Was able to apply least-privilege security at folder granularity, rename safely, and speed recursive listings versus scanning thousands of prefixed blob names.


