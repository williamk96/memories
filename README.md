# 30 May 2022
I set up a basic MERN app with the intent of using it to practice making POA&M tickets. This is to accomplish two things: 1) getting back into JavaScript and 2) getting more familiarized with POA&Ms as defined by the National Institute of Standards and Technologies. The project is based of the "memories" project by JavaScript Mastery on YouTube. The reason for this basis is that in the end when the POAM Database is finished, one will interact with it as if it is a kind of Social Media. POAMs are created for the purpose of systematically executing Information Assurance Vulnerability Management. It requires the ability to create POAM items with certain properties (Columns), some of which are changable and some are unchangable, show who to contact to discuss said POAM items, and store POAM items in a central location so all Analysts with jurisdiction on the applicable Information Systems may collaborate on all POAM items.

Right now, I am 32 minutes into the 7.5 hour course and already see where I would need to begin making changes to the memories project to reflect the POAM project.

## Design Overview

### Versioning
A.B.C

A = the year of the release
B = month of the release
C = release number of the period

Ex: 22.5.7

### Discussion
/server/routes/posts.js is interconnected with /server/controllers/posts.js so that the former object pulls from the latter to create a more organized file for quicker and simpler management. As long as the function names in the latter object remain the same, I can alter the methods of the functions to serve the POAM project's needs.

The overall server software would be run on one machine and (currently) connect to the outside internet, specifically Mongodb Atlas Cloud Database, on port 5000. If this continued to be the database storage option we use, the production server would incur at minimum a $56 per month charge for operation. It may then be preferable to run a local mongo database on the same machine as is hosting the POAM server software. This would however require a more robust machine. Because I do not forsee this project being commercially available, rather just being a closed tool for personal use, Atlas can continue to be used.

### Project Steps

At this time, the project is divided into a few major steps:

1. follow the guide at: https://www.youtube.com/watch?v=VsUzmlZfYNg to learn about the MERN stack and create the memories project while updating a git repoository and taking notes about it's design
2. iteratively update middlewares and dependencies while reworking the codebase to reflecting changes in the stack; final product should be the same app, but run on an up-to-date and secure tech stack
3. Redesign the app with subtasks such as: empty the database cluster of any test data and rework the models to reflect a POAM model; update the react objects to reflect important POAM characteristics like impact level, whether it it open or closed, and the number of updates it has
4. create a docker container image for the app, test the container in a fedora VM, and fix issues until you have an image deployment model for the software; also create the functionality which would allow for a cloud deployment or a local deployment
5. create a test environment using various flavors of linux to confirm system compatibility while altering variables such as minimum vCPUs, RAM, and storage
6. create a working docs page for future deployment
7. deploy POAM software and docs page in a private cloud for a short experimental run of the software
8. add project to my personal portfolio