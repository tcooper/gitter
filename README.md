#Go-Gitter for GitHub & BitBucket -- v.0.1

A lazy way to create, migrate, and update repos on GitHub and BitBucket.

Built on REST APIs from GitHub API v3 and BitBucket API v1.0. Written in Ruby.

Feel free to fork, comment, contribute, spoon, or spatula...especially if there's a better way of doing something!!!

##Screenshots:
###Create
![create](https://github.com/dderiso/gitter/raw/master/screenshots_for_github/create.png)
![create2](https://github.com/dderiso/gitter/raw/master/screenshots_for_github/create2.png)
###Update
![update](https://github.com/dderiso/gitter/raw/master/screenshots_for_github/update.png)
Note, you can also specify a custom message or leave blank for the default commit message: "updates via gitter"
###Migrate from one Repo Provider to Another
![migrate](https://github.com/dderiso/gitter/raw/master/screenshots_for_github/migrate.png)
![migrate2](https://github.com/dderiso/gitter/raw/master/screenshots_for_github/migrate2.png)

##Usage:
    Usage: gitter [options]
	    -n, --name [name]                Set the name of the new repo
	    -r, --repo-hub [provider]        Where do you want this repo? GitHub = g, Bitbucket = b
	    -c, --create                     Create new repo
	    -m, --migrate                    Migrate existing repo to new provider
	    -u, --update [optional message]  Update existing repo with custom or default commit message
	    -l, --language [language]        Set language of the new repo
	    -d, --debug                      Print commands for inspection, doesn't actually run them
	    -h, --help                       Prints this little guide

##Examples:
    create new repo: 				gitter -c -r b -l javascript -n node_app
    migrate existing to GitHub: 	gitter -m -r g -n node_app
    create repo and migrate to it: 	gitter -c -m -r b -l javascript -n node_app
    update any repo: 				gitter -u "made it work" or gitter -u

##Notes:
* You will prompted for your Github/BitBucket password, but it wont print out or be saved in history
* Username for repo is ($USER) by default, you can change this on line 8
* New repos are private by default
* Doesn't like symbols for language (ex. use 'c' instead of 'c++')
* Updating a repo has commit message 'updates via gitter' by default

