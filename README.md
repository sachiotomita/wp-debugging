# WP Debugging

* Contributors: [Andy Fragen](https://github.com/afragen)
* Tags: debug, support
* Requires at least: 4.6
* Requires PHP: 5.4
* Tested up to: 5.0
* Stable tag: master
* Donate link: <https://thefragens.com/github-updater-donate>
* License: MIT

A debugging/support plugin for WordPress.

## Description

This plugin sets the following debug constants in `wp-config.php` on plugin activation and removes them on plugin deactivation. If your `wp-config.php` is not writable then nothing will happen. Debug constants per [Debugging in WordPress](https://codex.wordpress.org/Debugging_in_WordPress).
Default settings:

```php
define( 'WP_DEBUG_LOG', true );
define( 'SCRIPT_DEBUG', true );
define( 'SAVEQUERIES', true );
```

`@ini_set( 'display_errors', 1 );` is set when the plugin is active.

The Settings page allows the user to set the following.

```php
define( 'WP_DEBUG', true );
define( 'WP_DEBUG_DISPLAY', false ); // Default when not declared is true.
```

When the plugin is deactivated all the constants are removed. When the plugin is activated the default settings and any saved settings are restored.

[Query Monitor](https://wordpress.org/plugins/query-monitor/) and [Debug Quick Look](https://github.com/norcross/debug-quick-look) plugins are installed and activated as dependencies to aid in debugging and troubleshooting.

[Debug Bar](https://wordpress.org/plugins/debug-bar/) plugin is an optional dependency.

[GitHub Updater](https://github.com/afragen/github-updater) plugin is optional dependency for plugin updates.

## Development

PRs are welcome against the `develop` branch.
