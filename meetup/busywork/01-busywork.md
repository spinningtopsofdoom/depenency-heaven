
How does new functionality reach Clojure developers right now

* Make changes to code base
* Commit changes
* Increment version
* Build artifact (e.g. jar)
* Deploy artifact to master computer (e.g. maven, clojars)
* Add updated dependency to project

!SLIDE

These steps require a build tool and immutable archive to deploy to

* Increment version
* Build artifact (e.g. jar)
* Deploy artifact to master computer (e.g. maven, clojars)

!SLIDE

Manual step for library / tool maintainer

!SLIDE

So to access new functionality of a library

* Create new functionality
* Test new functionality
* Commit new functionality
* Build Tool
* Immutable archive
* Manually make new version name
* Manual deployment step to immutable archive

!SLIDE

Create Value

* Create new functionality
* Test new functionality
* Commit new functionality

!SLIDE

Overhead and busywork

* Build Tool
* Immutable archive
* Manually make new version name
* Manual deployment step to immutable archive

!SLIDE

Why do we have anything besides the first three items?

Major functionality of version release stable memorable dependency. You can search for "How do I flap with Bird 1.4 (Bob Buzzard)".

!SLIDE

Just treat libraries as extra source we're putting into our project

For example adding `spectre` to  project `foo.bar` should be exactly the same as taking the source files of `spectre` and dropping them into our source directory
