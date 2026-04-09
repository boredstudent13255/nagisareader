<h1>Nagisa Reader</h1>
<p>A decentralized manga reader designed to function not dissimilarly to the Fediverse.</p>

The core idea behind this is to provide a fully decentralized alternative to MangaDex that offers a user-friendly UI.
However, the nature of the idea enables Nagisa Reader to be used by really anyone that has comics to share, so long as they don't mind the UI being built for right-to-left reading. The downside being that moderation is impossible.

Aggregates are to host metadata detailing what chapters they contain and what series(es) those chapters belong to. This is simply the client end, which is designed to parse the data from whatever aggregate you point it to.
Note however that this requires explicit support from the aggregate- you can't just plug in any manga site. You have to point Nagisa Reader to the data for the aggregate, which they'll no doubt provide themselves.



<h3>The plan</h3>
I haven't started writing Nagisa Reader yet. But here's the idea as it is now.

1. Making a series list <br>
The end user will have a cookie filled with a list of their saved aggregates. Upon loading Nagisa Reader, each aggregate is pinged for their series indexes. (List of titles.)
This information is pooled into a list of titles, prioritizing data from aggregates that appear earlier in the user's cookie in the case of duplicates. Once you have a list of titles, that data is then rendered as clickable entries on the user's end.

2. Making a chapter list <br>
Repeat the prior, but reading chapter data from all aggregates' indexes regarding the series ID. The index lists chapters and the series each one belongs to, each encoded with their unique IDs.
Clicking an entry will take the user to the reader, set to load their selected chapter from their most-favored aggregate that offers it.
Note: For those making an aggregate, DO NOT recycle chapter IDs for different content. Chapter IDs are only to be shared when the same scanlation appears on another aggregate, in which case the end user's first able aggregate will be referenced. However, you are strongly encouraged to seek out an existing ID for a new series, rather than creating your own. This is to enable multiple aggregates' content to comine into one cohesive page.


3. Loading pages <br>
I've not yet decided the specifics of how pages will be sorted out. However, I intend to allow the metadata to go as far as to point to image files on another domain. In which case, multiple mirrors for those would be, again, allowed. I think it would be funny as hell if someone piggybacked off of a bootleg site to host their scanlations for free, and I want to enable such.

<h3>Planned Features:</h3>
Remember the end user's configurations, including saved domains. <br>
Allow the scanlator to set a page layout (manga-single, manga-double, manhwa, etc) and organize their pages or panels in an easy to understand way.<br>
Complete folder structure flexibility on the hoster's end. Hosters should be able to simply generate the proper metadata for a preexisting chapter, without worrying about renaming pages to adhere to a specific format. Anything from loading numbered pages in order (ex: 1.jpg, 2.jpg / 001.jpg, 002.jpg) to loading numbered pages with a prefix and suffix (ex: <b>series-ch1-pg</b>1<b>.jpg</b>, <b>series-ch1-pg</b>2<b>.jpg</b>) to specifying a URL for every single page in a chapter, all should be options the hoster has available to them. A local program for generating this metadata would likely be warranted.<br>
Legacy support for the hosting format that my rudimentary current reader uses. <br>
Allow users to pick from a selection of series covers, which would be provided by the hoster from a folder- or allow users to provide a link to a cover on the internet.
