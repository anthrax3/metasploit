# Metasploit Repo Manifests

* Download and install Android's ["repo" script](https://source.android.com/source/downloading.html).

## To initialize your Metasploit repo.

* Insert the following in to `~/.ssh/config`

```
Host github.com
    HostName ssh.github.com
    User git
    IdentityFile ~/.ssh/id_rsa
```

* Create your workspace directory `mkdir ~/metasploit`
* Clone the manifests using `repo init -u git@github.com:rapid7/metasploit.git`
* Checkout the manifest branch you'd like to use:
    * `cd ~/metasploit/.repo/manifests`
    * `git checkout $BRANCH_NAME`
* Sync the repositories using `~/bin/repo sync`

* On intial checkout by repo the repositories will checkout the branch set in `default.xml` in a disconnected state.
 To make edits and commit changes to a repository use git commands to create a branch or checkout an existing
 branch in the repository tree.
