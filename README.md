# Logger2

Logger2 is the successor to Logger, an internal app I developed and use to keep
track of when I last took medication.

Logger2 aims to handle that use case, but also many more. A brief feature / goal
overview:

* Data points associated with a series, which can have tags/categories
* Mood tracking (and other time-series-ish data)
* Backlogging data (ability to change timestamp when entering a point)
* Automatic data collection (integrate with your sleep tracking app)
* Customizable notifications based on data you've entered or external triggers
  (e.g. you've forgotten to take your meds or enter mood data, you aren't
  asleep even though it's 7 hours before your alarm)

## Overall design

* Record button configured to log data to a specific series
  * Widgets for entering data
  * Buttons optionally can be hidden based on conditions
* History view
  * Graphs
* Notifications triggers are Python. Access to:
  * Last point data/metadata for each series
  * Sunrise/sunset times
