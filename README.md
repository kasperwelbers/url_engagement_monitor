# The harsh reality of social media research

Somewhere around the beginning of 2018, Facebook greatly crippled research into news on Facebook by imposing strict limitations on the use of their API. As such, the script intended for this GitHub page (see below) no longer worked. However, the part where the engagement scores for URLs were retrieved might still work, so hopefully I'll soon get around to trying to salvage what might be saved.

# URL engagement monitor

This repository was intended (before the changes to the Facebook API) to publish the scripts to monitor the engagement scores of URLs given a websites RSS feed, as used in [Welbers & Opgenhaffen, 2018](https://journals.sagepub.com/doi/full/10.1177/1461444818784302). 

Given a list of RSS feeds, the monitor collects new URLs on the feeds in real-time. It then resolves the canonical URL, as [used by Facebook](https://developers.facebook.com/docs/sharing/webmasters/optimizing) to aggregate engagement across duplicate content, and adds the canonical URL to a queue. For a specified amount of time (default is 3 days), the engagement score for this URL will be collected repeatedly with a specified time intervall (default is 30 minutes). The output consists of two csv files for each unique domain: the URLs on the RSS feed with basic meta data (title, date, snippet), and the engagement scores for each unique canonical URL.





