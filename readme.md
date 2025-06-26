Nagisa Reader
A decentralized manga reader designed to function not dissimilarly to the Fediverse. 

The core idea behind this is to provide a fully decentralized alternative to MangaDex that offers a user-friendly UI.
However, the nature of the idea enables Nagisa Reader to be used by really anyone that has comics to share, so long as they don't mind the UI being built for right-to-left reading. The downside being that moderation is impossible.

Aggregates are to host XML metadata detailing what chapters they contain and what series(es) those chapters belong to. This is simply the client end, which is designed to parse the data from whatever aggregate you point it to.
Note however that this requires explicit support from the aggregate- you can't just plug in any manga site. You have to point Nagisa Reader to the data for the aggregate, which they'll no doubt provide themselves.



The plan
I haven't started writing Nagisa Reader yet. But here's the idea as it is now.

1. Making a series list
The end user will have a cookie filled with a list of their saved aggregates. Upon loading Nagisa Reader, each aggregate is pinged for their series indexes. (List of titles.)
This information is pooled into a list of titles, prioritizing data from aggregates that appear earlier in the user's cookie in the case of duplicates. Once you have a list of titles, that data is then rendered as clickable entries on the user's end.

2. Making a chapter list
Repeat the prior, but reading chapter data from all aggregates' indexes regarding the series ID. The index lists chapters and the series each one belongs to, each encoded with their unique IDs.
Clicking an entry will take the user to the reader, set to load their selected chapter from their most-favored aggregate that offers it.
Note: For those making an aggregate, DO NOT recycle chapter IDs for different content. Chapter IDs are only to be shared when the same scanlation appears on another aggregate, in which case the end user's first able aggregate will be referenced. However, you are strongly encouraged to seek out an existing ID for a new series, rather than creating your own. This is to enable multiple aggregates' content to comine into one cohesive page.


3. Loading pages
I've not yet decided the specifics of how pages will be sorted out. However, I intend to allow the XML to go as far as to point to image files on another domain. In which case, multiple mirrors for those would be, again, allowed. I think it would be funny as hell if someone piggybacked off of a bootleg site to host their scanlations for free, and I want to enable such.
