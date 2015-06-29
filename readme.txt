=== Knowledgebase ===
Contributors: Ajay, webberzone
Donate link: https://ajaydsouza.com/donate/
Tags: knowledgebase, FAQ, frequently asked questions, knowledge base, support, documentation
Requires at least: 3.8
Tested up to: 4.3
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

The easiest way to create a Knowledgebase or FAQ on your WordPress blog.

== Description ==

As the name suggests, [Knowledgebase](https://webberzone.com/plugins/knowledgebase/) will allow you to create a simple Knowledgebase on your WordPress blog.

I felt the need to write up this simple plugin after I tried several free plugins out there, but none seemed to fit my purpose. In the spirit of open source, I'm releasing this to everyone who might find it useful.

= Main features: =

* Uses a custom post type `wz_knowledgebase` with a slug of `wzkb` ensuring your data always stays even if you choose to delete this plugin
* Uses Categories ( `kbcategory` ) to automatically draw up the knowledgebase
* Additionally, tags ( `kbtags` ) can also be used for each knowledgebase article. This helps to view listings by tag
* Shortcode `[[knowledgebase]]` will allow you to display the knowledgebase on any page of your choosing. I prefer creating one with the slug `knowledgebase`
* Inbuilt styles to display the knowledgebase beautifully
* Supports unlimited level of categories

= Contribute =

Although, Knowledgebase is fully functional, there are many features that I plan to add to this plugin as it develops. This includes inbuilt templates for articles, live search and also an options page that let's you customise some options.

If you have an idea, I'd love to hear it. Knowledgebase is also available on [Github](https://github.com/WebberZone/knowledgebase). You can [create an issue on the Github page](https://github.com/WebberZone/knowledgebase/issues) or, better yet, fork the plugin, add a new feature and send me a pull request.

== Installation ==

1. Upload `knowledgebase` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Create a new page or edit an existing one and add the shortcode `[knowledgebase]` to set up this page to display the knowledgebase
4. Visit `Knowledgebase &raquo; Add New` to add new Articles to the knowledgebase
5. Visit `Knowledgebase &raquo; KB Category` to add new categories to the knowledgebase. Alternatively, you can add new categories from the meta box in the Add New page

The plugin supports unlimited levels of category hierarchy, however, the recommended setting for creating the knowledge base is to create a top level category with the name of the knowledgebase and sub-level categories for each section of this knowledgebase. Check out the Category view screenshot as an example.


== Frequently Asked Questions ==

If your question isn't listed here, please post a comment at the <a href="http://wordpress.org/support/plugin/knowledgebase">WordPress.org support forum</a>. I monitor the forums on an ongoing basis. If you're looking for more advanced support, please see <a href="http://ajaydsouza.com/support/">details here</a>.

Alternatively, [create an issue on the Github page](https://github.com/WebberZone/knowledgebase/issues).

= Shortcode =

You can display the knowledgebase anywhere in your blog using the `[knowledgebase]` shortcode. The recommended option is to add this to a dedicated page called *Knowledgebase*. The plugin takes one optional attribute `category`:

`[knowledgebase category="92"]`

*category* : Category ID for which you want to display the knowledge base. You can find the ID in the KB Category listing under Knowledgebase in the WordPress Admin.

= Disabling default styles =

If you'd like to disable the default styles that come inbuilt with the plugin, just add this to your theme's **functions.php**

`wp_deregister_style( 'wzkb_styles' );`

= Using your own templates for archives and search =

Knowledgebase comes inbuilt with a set of custom templates to display archives of the articles, category archives as well as search results. You can easily override any of these templates by creating your own template in your theme's folder

1. Articles archive: archive-wz_knowledgebase.php
2. Category archive: taxonomy-wzkb_category.php
3. Search results: search-wz_knowledgebase.php


== Screenshots ==

1. Knowledgebase Menu in the WordPress Admin
2. Knowledgebase Viewer Facing with Default styles
3. Knowledgebase Category view in the WordPress Admin


== Upgrade Notice ==

= 1.1.0 =
* Multisite support, new archive templates, changed KB slugs and more;
Check out the changelog for detailed information


== Changelog ==

= 1.1.0 - 29 June 2015 =
* New: Network activate now works on multisite
* New: Main archive displays the Knowledgebase. You can override the default template by adding a file `archive-wz_knowledgebase.php` in your theme folder
* New: Category archive displays the knowledgebase for the specific category. You can override the default template by adding a file `taxonomy-wzkb_category.php` in your theme folder
* New: Major rewrite of knowledgebase HTML markup and default styles. If you're using your own custom styles, then you will need to remove
* Modified: Custom post type slug changed to `knowledgebase` from `wzkb`
* Modified: Custom post type archives and category archives changed to `kb-articles`. Tag archives changed to `kb-tags`
* Modified: Duplicate code cleanup
* Fixed: If term has no children terms, then directly display the articles under it

= 1.0.0 - 17 May 2015 =
* Initial release


