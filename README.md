
This plugin lets you extend the server block in your app's
`nginx.conf`. 

It comes from dokku PR#579, but does it as a plugin that can
be used with current dokku; it uses the approaches taken in the 
(very nice) 'dokku-custom-domains' and 
'dokku-nginx-vhosts-custom-configuration' plugins. 

# Usage

Do this:

    dokku config:set <app> NGINX_SERVER_DECORATION=nginx.inc.conf

If that file in your project root, now on your next
deploy, that file will be included from inside 
your app's `server{}` block, which should make it a
good place to put `location{}` overrides and such.

### LICENSE

MIT
