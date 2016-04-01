# Develop via proxy

Configuration files for painless development work behind Kantar's proxy. Covers:

* Curl
* Git
* NPM
* Bower

These proxy URIs contain persistent authentication not associated with any given user whose password does not expire, so should be safe to use as is for posterity.

Place these files in `~/etc` (Unix / Mac) or `C:\Users\username` (Windows), then replace the strings `username` and `password` as appropriate.

## Make sure:

* Not to wholesale replace existing files where you may have set up for eg Git, NPM (such as credentials / user preferences): merge or copy-paste the relevant properties.

## Troubleshooting

If this isn't working, try to eliminate the possibility of conflicts before filing an issue or writing more configuration:

* On *nix, you may have overriding global [SSH configuration]( http://linux.die.net/man/5/ssh_config).
* Some tools will look for configuration files in the local folder and walk the tree upwards, using the closest property definition - so an `https` or `url` directive in a `.gitconfig` file in the local folder may be overriding or invalidating higher order configuration
