
This does what PR#579 does, but as a plugin, modifying the app's existing
`nginx.conf`.

Do this:

    dokku config:set <app> NGINX_SERVER_DECORATION=nginx.inc.conf

And if you include that file in your project root, now on your next
deploy, that file will be included from inside 
your app's `server{}` block, making it a
good place to put `location{}` overrides and such.

### LICENSE

MIT
