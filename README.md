# RiiConnect24 Mail Scripts
These are the production-grade scripts we use at RiiConnect24. There aren't any propietary addons; what you see here is what we are running.

Schema is available in the `mysql` folder.

Scripts are available in the `php` folder.

Pruning scripts are in `clean` folder. Run these every so often to ensure the database does not get filled up.

# Setup
1. Patch your nwc24msg.cfg; we have tools on our GitHub to do that.
2. In the `php` folder, run `composer update` to install Sentry, as required.
3. Use RiiConnect24's very vulnerable IOS patch that allows any server to work because we seem to not understand how to do `res` properly and nobody wanted to work on it after we released. Oh well.
4. Import the schema, and run the scripts on your server - see below for replacing.

# config.php
- `USER`, `PASS`, `DATABASE` - MySQL login details.
- `password` - API Key for SendGrid
- `domain` - Domain for SendGrid verification
- `interval` - Interval to send to the Wii to have it check in for mail
- `sentryurl` - The URL Sentry gave you in your setup, to use for error logging.
# Credits
- thejsa for MySQL code and all of send.php's working send code.
- spotlight_is_ok for pushing for this type of stuff to be OSSed. :heart:
- Larsenv for pushing the team to get it to work.
- PokeAcer for arranging the entire project.

# Help Out!
Want to help out?
- The Mail system has _no_ security due to the IOS patch. This needs to be figured out.
- Automatic patcher for server(s).
- Interconnectivity between servers so that we don't fracture the community.
