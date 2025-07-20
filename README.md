# tren.my
Repository for the tren.my website as progressive web app.

## Roadmap

### Legends*
- *F = field study required

### MNP requirements
- [ ] Basic station data structure
  - [ ] Name
  - [ ] Also include station code(s) here for the purpose of ID OR instead iterate through the ID of each platform's station code?
  - [ ] Vector-based station layouts for all KTM, LRT and MRT train stations *F
    - [ ] Platform door numbers in terms of total doors or in terms of per-carriage?
    - [ ] Custom-made directional platform-to-platform/platform-to-exit navigation inspired by SMRT train information displays' station layout screen
    - [ ] Estimated travel time needed within station through programmatically calculating the distance in relation to the layout vector?
  - [ ] Platform
    - [ ] Station code (also used to determine which service, regardless of transport type, is provided on certain station)
      - [ ] INCLUDING bus routes
        - RapidKL buses do not usually use specific/dedicated bus stop number? If so, may have to include a universal bus platform in structure instead for train stations with bus services *F
    - [ ] Longitude and latitude *in relation to station layout vectors*
  - [ ] Accessible? including specific exits *F
    - Station must have elevator from platform to concourse
    - No stairs for any route between concourse and exits
    - Conditional status for stations that require contacting station personnels to assist for e.g. wheelchair lifts installed on stairs (see KL Monorel)
    - For certain stations e.g. Abdullah Hukum, include accessibility of popular destinations that are directly connected to the station *not* on the ground level e.g. Abdullah Hukum-KL Eco City-Gardens Mall pedestrian bridge
    - Service/platform-specific accessibility options for stations with multiple services
    - Train-to-platform accessibility, specifically, is the height and/or width of the train gap enough to cause problems for wheelchair users without any assistance
  - [ ] Routes in relation to station layout?
    - Only specifically construct routes from the platform door(s) with the quickest rotue out of platform
    - Uses a list of positions in relation to station layout vectors
    - Mark which route can be done the quickest bidirectionally (if so, then reverse the position list's order)
    - ID scheme for each route TBD
  - [ ] Park & Ride?
    - [ ] If available, include carpark vector and if also available, include number for each bay for platform-to-carpark navigation
- [ ] Accessible mode *F
  - [ ] Excludes stations with no accessible options
    - [ ] Allow filter to include or exclude station indoor rotues with 
- [ ] Custom travel time between adjacent stations from the moment train starts to accelerate to the moment the train stops at the station platform *F

### Future features in consideration in terms of priority
- [ ] Implementation of map view with either OpenStreetMaps or GrabMaps tiles using public RapidKL bus realtime GTFS API
  - [ ] Bus routes
  - [ ] Live bus tracking
  - [ ] POI-based routing navigation using GrabMaps POI database
- [ ] Vector-based station layouts for:
  - [ ] KLIA Ekspres/Transit stations
  - [ ] Terminal Bersepadu Selatan bus terminal
    - [ ] To/from-Platform navigation
    - [ ] To/from-carpark nagivation complete with number for each bay
    
