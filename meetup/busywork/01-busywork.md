
# How do we publicize changes?
## Changes mean after `git commit` and `git push`

!SLIDE

# Increment Version Number
## Go from `1.1.0` to `1.2.0`

!SLIDE

# Build artifact
## Compile `bird.utopia` to `bird-utopia-1.4.0.jar`

!SLIDE

# Deploy artifact
## Deploy to Maven with GPG credentials

!SLIDE

# Announce new version
## Post on mailing list, slack announcement, `CHANGES.md`

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
## Use source code as artifact
<br />
## Instead of JAR we use Source Cdoe
<br />
## Instead of Version Number we use a Commit Hash

!SLIDE

# Treat Libraries as source code
## Adding a library is as easy as pointing to a Github project

!SLIDE

# Many potential Points of Failure
* Adding library breaks current functionality
    * Monkey Patching, Namespace conflicts
* Updating library breaks previous functionality
    * Old functionality removed, changed
* Library load order matters
    * Global mutable state
* Library needs tools to work
