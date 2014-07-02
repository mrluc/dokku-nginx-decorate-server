
This plugin lets you extend the server block in your app's
`nginx.conf`, by placing a file called `nginx.inc.conf` in
your app's root.

# Installation

    git clone git@github.com/mrluc/dokku-nginx-decorate-server /var/lib/dokku/plugins/nginx-decorate-server

# Usage

Add `nginx.inc.conf` in your app's root, and let plugins know
you have it by:

    dokku config:set <app> NGINX_SERVER_DECORATION=nginx.inc.conf

On your next deploy, that file will be included from inside 
your app's `server{}` block, which should make it a
good place to put `location{}` overrides and such.

# What's All This Then

This comes from dokku PR#579, and is written as a plugin that can
be used with current dokku; it uses the approaches taken in the 
useful 'dokku-custom-domains' and 
'dokku-nginx-vhosts-custom-configuration' plugins. 

### LICENSE

MIT
