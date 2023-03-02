# 30 May 2022
I set up a basic MERN app with the intent of learning JavaScript frameworks. The project is based of the "memories" project by JavaScript Mastery on YouTube. The reason for this basis is that in the end when the POAM Database is finished, one will interact with it as if it is a kind of Social Media. POAMs are created for the purpose of systematically executing Information Assurance Vulnerability Management. It requires the ability to create POAM items with certain properties (Columns), some of which are changable and some are unchangable, show who to contact to discuss said POAM items, and store POAM items in a central location so all Analysts with jurisdiction on the applicable Information Systems may collaborate on all POAM items.

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
