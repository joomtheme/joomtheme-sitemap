# JoomTheme Sitemap

A professional XML sitemap package for Joomla 6.x by JoomTheme.

JoomTheme Sitemap generates a clean XML sitemap for Joomla websites with a dashboard scanner, physical sitemap.xml writer, dynamic sitemap fallback, smart SEO priorities, custom URL support and built-in exclusion filters.

## Features

- Joomla 6.x compatible package
- Dashboard sitemap scanner
- One-click sitemap rebuild
- Sitemap cache purge action
- Physical sitemap.xml writer
- Dynamic sitemap endpoint fallback
- Frontend SEF URL support
- Automatic duplicate URL prevention
- Automatic exclusion of administrator, login, register, logout, raw and non-indexable URLs
- Smart SEO priority handling
- Custom URL support
- Exclude pattern support
- Sitemap index support for large websites
- English and Turkish language files
- Joomla update server support
- JED-ready package structure

## Package Contents

The package installs:

- com_jtsitemap — Administrator component
- plg_system_jtsitemap — System plugin

Install the package ZIP, not the individual component or plugin ZIP, unless you know exactly what you are doing.

## Requirements

- Joomla 6.x
- PHP 8.3 or newer
- MySQL 8.0.13+ or MariaDB 10.4+
- Writable Joomla root folder is recommended for physical sitemap.xml generation

## Installation

1. Download the latest package ZIP.
2. Go to Joomla Administrator.
3. Open System → Install → Extensions.
4. Upload and install pkg_jtsitemap_1.0.7.zip.
5. Go to Components → JoomTheme Sitemap.
6. Click Rebuild Sitemap.
7. Open your sitemap URL:

   https://your-domain.com/sitemap.xml

## Recommended robots.txt Entry

Add this line to your robots.txt file:

    Sitemap: https://your-domain.com/sitemap.xml

## Dashboard

The component dashboard provides:

- Sitemap status
- Sitemap endpoint
- Sitemap URL
- Cached URL count
- Last build date
- Physical file status
- System plugin status
- Rebuild Sitemap button
- Purge Sitemap Cache button
- robots.txt sitemap line
- Support information

## Cache and Generated Files

JoomTheme Sitemap stores generated sitemap URLs in a database cache table.

When you click Purge Sitemap Cache, the extension also removes generated physical sitemap files such as sitemap.xml and sitemap chunk files. This is intentional and helps prevent old, broken or outdated sitemap files from staying online.

After purging the cache, click Rebuild Sitemap to generate a fresh sitemap.

## Smart SEO Priorities

JoomTheme Sitemap applies smart default priorities:

| Page Type | Priority |
|---|---:|
| Homepage | 1.0 |
| Products / Shop pages | 0.9 |
| Product detail pages | 0.9 |
| Support documentation | 0.7 |
| Contact / About pages | 0.6 |
| Policy pages | 0.3 |

These values help keep important commercial and product pages weighted above utility pages.

## Default SEO Exclusions

The generator automatically excludes non-indexable or unsafe URLs such as:

- /administrator
- /api
- /tmp
- /cache
- Login pages
- Register pages
- Logout pages
- Search popup pages
- Raw output URLs
- JSON output URLs
- tmpl=component
- URLs containing task, token or return parameters
- Raw index.php?option=com_content fallback URLs

## Custom URLs

You can add custom URLs from the component options.

Format:

    URL|YYYY-MM-DD|changefreq|priority

Example:

    https://example.com/custom-page|2026-04-29|weekly|0.8

Only the URL is required.

## Exclude Patterns

You can exclude URLs using one pattern per line.

Examples:

    /search-popup
    */login*
    */register*
    /private-section/

Supported matching types:

- Plain contains matching
- Wildcard matching
- Regex patterns wrapped in /.../

## Update Server

The package includes Joomla update server metadata.

Update Server URL:

    https://joomtheme.com/updates/jtsitemap/update.xml

Changelog URL:

    https://joomtheme.com/updates/jtsitemap/changelog.xml

Download URL:

    https://joomtheme.com/downloads/jtsitemap/pkg_jtsitemap_1.0.7.zip

## Changelog

### 1.0.7

#### Added

- Joomla update server metadata
- Changelog metadata
- Dashboard support box
- Smart SEO priority handling
- Default SEO exclusions
- English and Turkish language updates

#### Changed

- Package manifest now includes update server and changelog URLs.
- Dashboard layout improved for JED-ready distribution.

#### Fixed

- Prevented administrator URLs from appearing in sitemap output.
- Prevented raw index.php?option=com_content fallback URLs from appearing in sitemap output.
- Improved sitemap cache filtering.

## Development

Clone the repository:

    git clone https://github.com/joomtheme/joomtheme-sitemap.git
    cd joomtheme-sitemap

Tag a release:

    git add .
    git commit -m "Release 1.0.7"
    git tag v1.0.7
    git push origin main --tags

## Repository

https://github.com/joomtheme/joomtheme-sitemap

## Support

Website: https://joomtheme.com

Email: support@joomtheme.com

## Author

JoomTheme  
https://joomtheme.com

## License

GNU General Public License version 2 or later.

See LICENSE.txt for details.
