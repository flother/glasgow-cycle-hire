*A bike hire scheme similar to that found in London, Paris, and other
European cities is coming to Scotland's largest city, Glasgow. I've made
[a map showing the places provisionally marked as having bikes available
for hire] [map].*

---

In the spring of 2014 Glasgow City Council will be launching MACH — mass
automated cycle hire — first with 150 bikes and 30 stations with
expansion coming later in the year. The details have been lightly
reported in the press but a more thorough report was presented to the
city council on 10 October 2013. The [report is available on the city
council's website] [rpt].

The appendices to that report included a low-resolution map of locations
where bikes will be available to hire, but exactly where they are to be
was hard to discern. The map is accompanied by the text "Appendix 3 to
this report contains an index to the numbered locations", but appendix 3
is actually just a picture of a bike.

So I did what any grown man would do in the circumstances and made a
freedom of information request. The locations were eventually given to
me as a [tabulated list in a PDF file] [pdf] (included in this repo).

As accessible data goes, that's pretty piss-poor. Humans can read it of
course, but computers have a much harder job. What if we want to
show the locations on a map, for example?

There are much better ways to provide the data. This Git repository
contains each location as a latitude and longitude point, all stored in
a single [GeoJSON] [geo] file encapsulated in the Open Knowledge
Foundation's [Data Package format] [pkg]. GitHub allows GeoJSON files to
be [displayed as a map directly] [ghm] and I've also made [a full-screen
map] [map]. Providing the locations in this format makes them more
accessible, more visible, and easier to analyse.


Converting the locations to latitude/longitude points
-----------------------------------------------------

None of the locations given by the council are exact, but they vary
between relatively precise ("SPT site" at Kelvinbridge subway station)
and fairly vague (somewhere on the half-a-mile-long West Nile Street).
Where the locations were too vague to plot I used the low-resolution map
included in the report to try and pinpoint the true locations as best I
could. I would estimate the council's provisional locations are at worst
no further than 200 metres from my longitude and latitude points.


Commonwealth Games locations
----------------------------

Ten of the 30 stations come with the comment "CG2014 possible MACH
station location", indicating that these locations are specifically for
venues being used at the 2014 Commonwealth Games. I don't know if the
comments indicate anything more than this (i.e. more likely to make it
past provisional status, only in use during the games, politically
necessary, etc).


The locations are provisional
-----------------------------

In their response to my FOI request Glasgow City Council pointed out in
a fairly tedious, corporate, manner that the list of locations is
provisional. Or, in their words, the list is

> only indicative and no decisions have yet been made as to whether they
> will, or will not, become a Glasgow mass automated cycle hire (MACH)
> station location. The MACH implementation team within the council has
> still to discuss these loose draft locations with the new service
> provider [German company Nextbike] who was awarded the contract on
> Friday 22 November 2013. The draft list is a means to provide a
> starting platform for discussions with the new service provider and
> once the list has been confirmed then the normal route whereby
> information is provided to elected members will be followed.


The freedom of information request
----------------------------------

My original request, dated 14 October 2013:

> The submission documents associated with councillor Alistair Watson's
> executive committee report on the introduction of a bike hire scheme
> in Glasgow, dated 10 October 2013, are available on Glasgow city
> council's website. The appendices are combined into a single PDF, and
> appendix 2 (page 2) contains a map showing numbered locations for
> potential bike hire locations. The map is accompanied by the text
> 'Appendix 3 to this report contains an index to the numbered
> locations.' However, appendix 3 (page 3) doesn't contain any such
> index.
> 
> I would be grateful if you could provide the index to the numbered
> locations under the Freedom of Information (Scotland) Act 2002.

The council's response, due no more than 20 working days later, came
after 42 working days on 11 December 2013 accompanied with apologies and
the promise that an internal review had fixed the "technical oversight"
that had caused the delay. I'm a programmer, I understand these things
can happen. (I would have preferred a more detailed reason though.)


[map]: http://flother.is/2014/glasgow-bike-hire/
[rpt]: http://www.glasgow.gov.uk/councillorsandcommittees/submissiondocuments.asp?submissionid=65178
[pdf]: http://github.com/flother/glasgow-cycle-hire/raw/master/foi_station_list.pdf
[geo]: http://geojson.org/
[pkg]: http://data.okfn.org/standards/data-package
[ghm]: https://github.com/flother/glasgow-cycle-hire/blob/master/stations.geojson