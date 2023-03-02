# 30 May 2022
I set up a basic MERN app with the intent of learning JavaScript frameworks. This is based of the "memories" project by JavaScript Mastery on YouTube.

## Design Overview

### Versioning
A.B.C

A = the year of the release
B = month of the release
C = release number of the period

Ex: 22.5.7

### Discussion
/server/routes/posts.js is interconnected with /server/controllers/posts.js so that the former object pulls from the latter to create a more organized file for quicker and simpler management.

The overall server software would be run on one machine and (currently) connect to the outside internet, specifically Mongodb Atlas Cloud Database, on port 5000. If this continued to be the database storage option we use, the production server would incur at minimum a $56 per month charge for operation. It may then be preferable to run a local mongo database on the same machine as is hosting the memories server software. This would however require a more robust machine. Because I do not forsee this project being commercially available, rather just being a closed tool for personal use, Atlas can continue to be used.
