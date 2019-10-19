# "The Counted" Plus+
## "The Counted" data (police homicides) from the Guardian with additional data points.
* "The Counted" is a data collection project of officer involved homicides from 2015-2016 in the US. The data was originally collected by the Guardian and published here: https://www.theguardian.com/us-news/series/counted-us-police-killings
* This data includes the original data plus latitude and longitude for where each death took place that was added using Google Locations API for [this project](https://github.com/joel-g/policewatch).
* **This repo is open for contributions to add news sources regarding each killing.**

## Contribution Instructions

1. Fork and clone this repo.
2. Open data.json with your editor.
3. Choose a person object and replace the `null` value of the `"sources"` key with an array of string(s) for news stories related to the death. Only adding one news article is fine but it must be in an array.
4. Open a pull request to have your contribution merged

*Example before:*

```json
  {
        "id": 1,
        "name": "Richard Jones",
        "age": 55,
        "sex": "Male",
        "race": "White",
        "month": "December",
        "day": 6,
        "year": 2016,
        "address": "3500 Ridgewood Dr",
        "city": "Hutchinson",
        "state": "KS",
        "cause": "Gunshot",
        "dept": "Hutchinson Police Department",
        "armed": "Firearm",
        "lat": 38.0927,
        "lon": -97.9095,
        "sources": null,
        "created_at": "2017-07-16 03:04:16.614685",
        "updated_at": "2017-07-16 03:22:21.379506"
    }
```
*Example after:*

```json
  {
        "id": 1,
        "name": "Richard Jones",
        "age": 55,
        "sex": "Male",
        "race": "White",
        "month": "December",
        "day": 6,
        "year": 2016,
        "address": "3500 Ridgewood Dr",
        "city": "Hutchinson",
        "state": "KS",
        "cause": "Gunshot",
        "dept": "Hutchinson Police Department",
        "armed": "Firearm",
        "lat": 38.0927,
        "lon": -97.9095,
        "sources": ["https://www.kwch.com/content/news/404980726.html"],
        "created_at": "2017-07-16 03:04:16.614685",
        "updated_at": "2017-07-16 03:22:21.379506"
    }
```

### Do's and Don'ts of contributions (read carefully, this can keep your PR from being mergerd)

* Do maintain original formatting. 
* Don't edit any data points other than `sources` (one exception is if you can find the names of any of the "Unknown")
* Don't use a file formatting tool that differs from VS Code's JSON formatter (if you reformat the whole file I can't tell what data you added and it will not be merged)
* Do favor local news accounts from the area the killing happened
* Do favor original reporting from the time of the death (avoid ediotialized accounts months or years later)
* Don't add biased news sources or unoriginal secondhand reporting from blogs


**Contributions using politically biased media from the following sources will not be merged:**
* Breitbart
* The Daily Wire
* The Blaze
* The Daily Beast
* Slate
* Vox
* Buzzfeed
* ANY opinion piece

This list may grow if contributors choose other biased media but these are examples.

**Examples of politically unbiased news sources:**
* BBC
* NPR (news not opinon)
* USA Today
* The Wall Street Journal

**Examples of news sources that lean politically that are not preferred but will still be allowed**
* New York Times (news only, not opinion)
* Fox News (news only, not opinion)
* The Washington Times
* The Guardian

### Whenever possible include a _local_ news source near where the killing happened as the first item in the array.
