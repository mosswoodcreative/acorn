# Cluster Runner Setup

- http://www.clusterrunner.com/
- http://www.clusterrunner.com/docs/installation/
- Create digital ocean droplet to act as primary
-- Set up local user
- Create digital ocean droplet to act as replica
-- Set up ssh keys from primary to replica using this: http://www.linuxproblem.org/art_9.html
-- Also set up keys from replica back to primary (the replica uses ssh to get the project code)

# Viewing test results

- https://www.npmjs.com/package/junit-viewer

# Known issues

- ```clusterrunner deploy``` uses the current username for the ssh username. For me that means running the command locally as root.
-- Solution: Make sure you create a user on the replica that has the same name is your local username.
-- From the docs: "At this time the master and slaves must all use the same type of operating system. We plan to add support for heterogeneous environments in the future."
