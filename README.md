# URL engagement monitor

This repository will soon contain scripts to monitor the engagement scores of URLs given a websites RSS feed, as used the paper XXX. Currently, only the Facebook engagement scores are supported, but additional social network sites can easily be added granted that they provide engagement scores for URLs. 

Given a list of RSS feeds, the monitor collects new URLs on the feeds in real-time. It then resolves the canonical URL, as [used by Facebook](https://developers.facebook.com/docs/sharing/webmasters/optimizing) to aggregate engagement across duplicate content, and adds the canonical URL to a queue. For a specified amount of time (default is 3 days), the engagement score for this URL will be collected repeatedly with a specified time intervall (default is 30 minutes). The output consists of two csv files for each unique domain: the URLs on the RSS feed with basic meta data (title, date, snippet), and the engagement scores for each unique canonical URL.


