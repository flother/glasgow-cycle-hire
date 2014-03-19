*A bike hire scheme similar to that found in London, Paris, and other
European cities is coming to Scotland's largest city, Glasgow. I've made
[a map showing the proposed locations of bike hire stations] [map].*

---

In May 2014 Glasgow City Council will be launching MACH — mass
automated cycle hire — 400 bikes and 31 stations, with an extra six
stations during the Commonwealth Games. Details have slowly been
filtering out, starting with a [report presented to the city council's
Executive Committee on 10 October 2013] [oct] and followed by a [second
report on 19 March 2014 to the Sustainability and the Environment Policy
Development Committee] [mar].

The appendices to the first report included a low-resolution map of
where bikes were to be available to hire, but exactly where was hard to
discern. Eventually a Freedom of Information request got me the
locations as a [tabulated list in a PDF file] [pdf] (included in this
repo, although the locations have since changed).

The second report included much improved details on the locations,
including a higher-resolution raster map and a list of the nearest
street address for each location. It's still pretty piss-poor as
accessible data goes, and this Git repository attempts to make a better
job of it.

The repo contains each location as a latitude and longitude point, all
stored in a single [GeoJSON] [geo] file encapsulated in the Open
Knowledge Foundation's [Data Package format] [pkg]. GitHub allows
GeoJSON files to be [displayed as a map directly] [ghm] and I've also
made a [full-screen map] [map]. Providing the locations in this format
makes them more accessible, more visible, and easier to analyse.


Commonwealth Games locations
----------------------------

Six of the 37 stations are temporary locations that will only be in use
during the 2014 Commonwealth Games. Each of these locations includes the
property `permanent: false`; all other permanent stations include the
property `permanent: true`.


Location accuracy
-----------------

While the nearest street address is given for each bike hire location
it's still not completely clear where exactly the bikes will be sited.
I've made educated guesses for each one (e.g. picked the nearest large
empty section of pavement or an existing bike rack) but we should assume
that the bikes are to be within a 100-metre radius of the longitude and
latitude provided, rather than at exactly that spot.

In their response to my original FOI request back in December 2013,
Glasgow City Council pointed out in a fairly tedious, corporate, manner
that the list of locations is provisional. Or, in their words, the list
is

> only indicative and no decisions have yet been made as to whether they
> will, or will not, become a Glasgow mass automated cycle hire (MACH)
> station location. The MACH implementation team within the council has
> still to discuss these loose draft locations with the new service
> provider [German company Nextbike] who was awarded the contract on
> Friday 22 November 2013. The draft list is a means to provide a
> starting platform for discussions with the new service provider and
> once the list has been confirmed then the normal route whereby
> information is provided to elected members will be followed.

Although council officers have since undertaken site surveys of the
updated locations I would assume they're still provisional. We'll only
know for sure once the scheme is up-and-running.


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
after 42 working days on 11 December 2013, accompanied with apologies
and the promise that an internal review had fixed the "technical
oversight" that had caused the delay. I'm a programmer, I understand
these things can happen — I would have preferred a more detailed reason
though.


[map]: http://flother.github.io/glasgow-cycle-hire/
[oct]: http://www.glasgow.gov.uk/councillorsandcommittees/submissiondocuments.asp?submissionid=65178
[mar]: http://www.glasgow.gov.uk/councillorsandcommittees/submissiondocuments.asp?submissionid=68243
[pdf]: http://github.com/flother/glasgow-cycle-hire/raw/master/foi_station_list.pdf
[geo]: http://geojson.org/
[pkg]: http://data.okfn.org/standards/data-package
[ghm]: https://github.com/flother/glasgow-cycle-hire/blob/master/stations.geojson
