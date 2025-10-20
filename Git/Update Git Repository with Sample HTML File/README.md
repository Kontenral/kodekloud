# Update Git Repository with Sample HTML File
The Nautilus development team has initiated a new project development, establishing various Git repositories to manage each project's source code. Recently, a repository named `/opt/apps.git` was created. The team has provided a sample `index.html` file located on the `jump host` under the `/tmp` directory. This repository has been cloned to `/usr/src/kodekloudrepos` on the `storage server` in the `Stratos DC`.

Copy the sample `index.html` file from the `jump host` to the `storage server` placing it within the cloned repository at `/usr/src/kodekloudrepos/apps`.

Add and commit the file to the repository.

Push the changes to the `master` branch.

## 1. Copy the sample `index.html` file from the `jump host` to the `storage server`
`ssh natasha@ststor01`

`sudo scp /tmp/index.html natasha@ststor01:/tmp`

`sudo cp /tmp/index.html /usr/src/kodekloudrepos/apps`


## 2. Add and commit the file to the repository.
`git add .`
`git commit -m "add index.html"`
`git push`

## 3. Push the changes to the `master` branch.
`git branch`
`git push`


