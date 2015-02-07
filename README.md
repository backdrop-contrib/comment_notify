Comment Notify
=============

Comment Notify is a lightweight tool to send notification e-mails to visitors about new, published comments on pages where they have commented. Comment Notify works for both registered and anonymous users.

Providing comment notifications for anonymous users is an important tool in bringing anonymous users back to your site, which helps convert anonymous users to registered users. Anonymous comment notification is a critical tool in building a blog comment community; all the major blogging platforms include this functionality.

Features
========

* Mail registered and anonymous users about comment follow-ups
* Allow users to unsubscribe from notifications on a specific post with a single click
* Allow registered users to preset their follow-up setting in their profile
* Users can choose to get notifications about all comments on a node or just replies to their comment
* Registered authors can get notifications about comments on their nodes
  Note: Since it only notifies you about published comments, this is not a solution to notify admins when they need to moderate comments on their site

Installation
------------

1. Enable the module from the Modules admin page from "Modules": `/admin/modules`

2. Grant permission to use this module from "People > Permissions": `/admin/people/permissions#module-comment_notify`

3. Set permissions for commenting as per usual from "People > Permissions": `/admin/people/permissions#module-comment`

4. Configure the settings for comments for content types from Structure > Content types > [Your content type] > Edit: "Comment settings": `/admin/structure/types/manage/[your_content_type]`, for example, `/admin/structure/types/manage/page`

 - Look for "Anonymous commenting" and set to either: "Anonymous posters may leave their contact information" OR "Anonymous posters must leave their contact information"

5. Configure this module at Configuration > People > Comment Notify: `/admin/config/people/comment_notify`

 - Determine which content types to activate it for
 - Determine which subscription modes are allowed
 - Configure the templates for the e-mails

6. Set your node-notify settings per user (optional)

The module includes a feature to notify the node author of all comments on their nodes. To enable this go to "My account" > Edit (e.g. `user/1/edit`) and change the settings there, i.e., "Comment follow-up notification settings".

Template Translation
--------------------

Notification templates are passed through t() before being added to the email's body. Therefore, for you to translate them to other languates you need to:

1. Enable the Locale module.

2. Choose a node in which you are not the auther and has comments and comment on it. This will send an email to the author and other commenters.

3. Open the Translation Interface, located at    `admin/config/regional/translate/translate`

4. Search for the template strings and add the translations.

Optional Modules
----------------

Performance: If you notice that your site is very slow when submitting
new comments it is possible that the problem is with sending the mails.
One option is to use the Queue Mail module
http://drupal.org/project/queue_mail

Compatibility Note
------------------

Comment Notify is not built to work on sites where other notification related modules are installed (modules like Actions, Notify, Subscriptions, and Organic Groups are popular examples). If you install both Comment Notify and one of these other mail modules on your site in addition to Comment Notify it may send duplicate messages and/or have user interface elements that will appear to be duplicates and confuse your site visitors.

The suggested configuration in these instances is to separate Comment Notify and whatever other mail module you have installed. Common ways to separate them are by content type or user permissions.

License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for complete text.

Current Maintainers
-------------------

This module is currently seeking maintainers.

Credits
-------

Ported to Backdrop by Herb v/d Dool (https://github.com/herbdool/)

This module was originally written for Drupal (https://drupal.org/project/comment_notify). Drupal maintainers are: [greggles](https://www.drupal.org/u/greggles).
