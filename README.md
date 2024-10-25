# Ad Refresh Module

This is an example of original code I wrote on the job as a web developer for Scranton-Gillette Communications in 2023.  This Drupal module allows website owners to control the rate at which Google ads refresh.  This module interacts with multiple levels of an application: back end, front end, and the Google Ad API.

Notable files:

/src/Form/SettingsForm.php
The module builds a settings page with PHP by first dynamically generating a list of all Google ad slots hosted on the site.  Users may assign an interval in number of seconds to each ad slot.  Users may also determine whether refresh should be disabled on certain ads or on entire pages.  The form saves these settings to the Drupal database.

/src/EventSubscriber/EventSubscriber.php
This makes use of the Symfony framework's dependency injection, attaching the module's JavaScript library only on main requests, and when the request allows attachments.

/js/ad_refresh.js
The JavaScript first calls the settings to get the refresh intervals for each ad.  It will then refresh each ad through the Google Ad API, if the current window is active.

- Eric Sorum
