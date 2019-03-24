Shuttle Tracker has an updated appearance. Instead of a menu in the top-left corner, there is now a tab bar at the bottom with three sections: Map, Schedules, and Settings.

The map view is the standard Leaflet map that is the default view when users view Shuttle Tracker.

Schedules shows links to PDFs of the route schedules from the Parking and Transportation Office. In the future, this could show a friendlier view after we figure out parsing the schedules.

Settings allows users to configure several Shuttle Tracker options, such as sending location updates (Fusion), bus button, and estimated times of arrival. These are directly linked to the Vuex store and changes are persisted in the client's HTML5 localstorage. We can add other settings easily in the future. Since they're in Vuex, it is easy for other parts of the application to react to changes to their values.

We also changed the color of the West Campus route to blue in order to make it easier for colorblind users to differentiate between West and East routes.
