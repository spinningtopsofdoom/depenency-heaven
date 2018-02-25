
#Look at steps after changes
## After `git commit` and `git push`

!SLIDE

# Increment Version Number

!SLIDE

# Build artifact (e.g. jar)

!SLIDE

# Deploy artifact (e.g. maven, clojars)

!SLIDE

# Announce new version(optional)

!SLIDE

# Spreading new features requires

* Build Tool :(
* Always up Immutable Repository :( :(
* **Manual Deployment** x_x

!SLIDE

# What are the benefits of these manual steps?

## Stable memorable dependency, "How do I flap with Bird 1.4 (Bob Buzzard)?".

!SLIDE

# Thought Experiment
<br />
## Artifact => Source Cdoe
<br />
## Version Number => Commit Hash

!SLIDE

# Treat Libraries as source code
## Many potential Points of Failure

!SLIDE

* Adding library breaks current functionality
* Updating breaks working functionality
* Library load order matters
* Library needs tools to work
* Excessive amounts of Glue Code
