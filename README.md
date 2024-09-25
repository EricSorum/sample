# Ad Refresh Module

This is an example of original code I wrote on the job as web developer for Scranton-Gillette Communications in 2023.  This Drupal module allows website owners to control the rate at which Google ads refresh.  This module interacts with multiple levels of an application: the back end, front end, and the Google Ad API.

Notable files:

sgc_ad_refresh/src/Form
The module builds a settings page with PHP by first dynamically generating a list of all Google ad slots hosted on the site.  Users may assign an interval in number of seconds to each ad slot.  Users may also determine whether refresh should be disabled on certain ads or on entire pages.  The form saves these settings to the Drupal database.

sgc_ad_refresh/js/ad_refresh.js
The JavaScript calls the settings and refreshes each ad at the required interval, if the window is being viewed.

- Eric Sorum
