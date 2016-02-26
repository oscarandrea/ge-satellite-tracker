The getrack.py script performs four main functions:
  1. generates a satellites.kml file that can be imported into Google Earth
  1. performs ephemeride calculations using pyephem
  1. generates kml containing each satellites orbital data
  1. manages a simple http server that Google Earth will query for the kml

The satellites.kml file consists of one network link per satellite of interest.  Each network
link points to a url resource that contains orbital data for the satellite of interest.  The urls
look like this:
  * http://localhost:8080/satellite1
  * http://localhost:8080/satellite2
  * ...

Where satellite1 may refer to HAMSAT and satellite2 may refer to the ISS.  This is all transparent to
the end-user for the most part, since they will only see "HAMSAT" in the Google Earth temporary places
listing.  The urls themselves are not nearly as interesting as the contents of the kml (which is actually
really basic).  For each satellite, orbits are plotted based upon the configured look ahead minutes and
tick interval seconds.  The look ahead minutes defines how leading/trailing the orbit will be in
terms of time.  The tick interval seconds defines how often points will be calculated along the orbit.
The tracking refresh interval seconds dictates how often Google Earth will request new orbital data.

Keplerian elements can be downloaded either from AMSAT or Space-Track.org.  Changing the source is simply a matter of modifying the keps source in the configuration file:

```
[keps]
source = amsat
```

See the appropriate configuration sections for details.

note: This script can be easily modified to work with other keplerian element sources.