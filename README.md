# PageSpeed API

An API to report on PageSpeed scores retrieved from the [Google PageSpeed Insights Tool](https://developers.google.com/speed/pagespeed/insights/).

## API Endpoints

### Get all scores
```
/
```

Retrieves all scores for pages that are being tracked in config.js.

### Get all pages
```
/pages
```

Retrieves a list of all pages that are being tracked.

### Get all current scores
```
/currentscore
```

Returns an array of the latest score for all pages that are being tracked.

### Get scores for a certain page
```
/scores?site={page}
```

Returns the scores for a specific page. The site value in the query string must be encoded.

### Get milestones for a certain page
```
/milestones/{strategy}/{siteId}
```

Returns the milestones for a specific page and strategy. Strategy can be either desktop or mobile. It also depends on what strategies are in the config.js. siteId corresponds to the id retrieved in the /pages call.
