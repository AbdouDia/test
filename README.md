# Manager Hotel Software
Development of a management software for the Ufuck Hotel.  It will allow hotel employees to manage the reservation of rooms, restaurants, swimming pool, conference room, etc.

## Features
See [specifications](cahier-de-charge.pdf)

## Workflow
For the development of the application  the team will consist of 2 frontend developers and 2 backend developers.

Once the team has been established, retrieve the project base from:
The git management of the project will be done on the git flow model. We distinguish the main branches, fixed and immutable:
 - **master** is the branch where everything is stable. Each commit corresponds to a stable release of the project that can be deployed in production and tagged accordingly (vX.Y.Z).
 - **develop** is the branch on which the actual development takes place.  We are preparing the changes for the next release in master.

Then the secondary branches that are made and unraveled over time:
  - **feature** part of **develop** and merges into **develop**.
  A **feature/xxx** branch is created when the We’re working on a particular feature.  When it is finished, we merge it into develop to add the stable feature to the scope of the next release.
    

  - **release** is part of **develop** and merges into **master** and **develop**.
  A **release/xxx** branch is created from develop when it reflects the desired state of the release (all scope features have been merged).  Thus, we can prepare the next release quietly, fix any bugs and continue the development in parallel.
  Once the release is ready (stable) we merge the branch into master, but also into develop to update the changes made.
    

 - **hotfix** starts from **master** and merges into **master** and **develop**/**release**.
 We create a **hotfix/xxx** branch when we want to fix a critical bug in production quickly.  It’s a bit like an unscheduled release.
 When the patch is developed, it is merged into master with the appropriate version number, as well as into develop (or the current release branch, if applicable) to update the changes made.
   
## Deadline
The software must be delivered at the latest the 21/05/2021.