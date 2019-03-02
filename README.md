# Doc migration notes

## Task list

This is by no means exhaustive, and will start by tracking what is happening in the immediate future or has recently happened.

### Phase 1: mirror SVN to Git, use Git for builds.

* [x] Add doc-base repo to gitolite-admin (en, de, already there).
* [x] Update authors.map in gitolite-admin.
* [x] Limit commit karma during migration phase.
* [x] Create git-svn repos of SVN repos (doc-base, en, de, to start with).
  Do this on SVN server and use file:// paths, so it doesn't take *forever*.
* [x] Keep git-svn repos up-to-date as new SVN revisions come in.
  Probably just a cron for simplicity.
* [ ] Set up repos on GitHub php org.
* [ ] Enable GH mirroring in gitolite-admin.
* [ ] Update docs.php.net to build from git repos
* [ ] Update rsync.php.net to build from git repos

### Phase 2: updating other tooling and preparing users

* [ ] Add .gitignore (see git-svn show-ignore/create-ignore)
* [ ] Update revcheck and other tools on docs.php.net
* [ ] Get online editor (edit.php.net) ready for git
* [ ] Update and/or draft docs on using git for the docs
* [ ] Announcements (more than one!) that change is coming

### Phase 3: transitioning

* [ ] Disable SVN for docs and update rejection message if someone tries to commit to SVN
* [ ] Update gitolite-admin for doc repos (commit emails, etc.)
* [ ] Grant everyone git commit karma
* [ ] Flip the switch for online editor (if we make it work with git)
