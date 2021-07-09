# The CFR Aircraft Engines Database
This repository contains a manually-collected database giving engine and body type information for 3,741 aircraft models. The aircraft model and type information was collected from [What is flying?](https://github.com/jbroutier/whatisflying-db) and the CFR team worked to source the other fields in this database from documents such as the FAA Type Certificates or websites such as Wikipedia.

# Database Structure

The `aircraft_engines.csv` file contains the following data:

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| manufacturer | string | The aircraft manufacturer | Airbus |
| model        | string | The aircraft model | A330-301 |
| aircraft_type | string | The aircraft ICAO code | A333 |
| description  | string | The aircraft ICAO Document 8643 description | L2J
| engine_count | integer| The number of engines the aircraft has | 2
| engine_type  | string | The type of engine the aircraft has | Jet
| aircraft_category | string | The type of the aircraft | LandPlane
| engine_manufacter | string | Name of the aircraft's engine manufacturer | General Electric
| engine_model | string | The models of the aircraft's engine | CF6-80E1A2
| body_type | string | The aircraft's body type | Wide
| max_seats | string | The maximum number of seats in the aircraft | 440

The database contains an additional 3 fields: `engine_source`, `max_seats_source`, and `contributor`. The first 2 contains URLs to where the data was sourced from while the contributor column credits who added in the vaues. Some aircraft contain multiple engines and engine manufacturers and the values for those aircraft were separated using semicolons. For example:

    O-320-B2A;O-320-B2B

The database contains 3,741 distinct aircraft models and fields for most records are complete. 

`engine_type` can take on the following values:

    1. Jet
    2. Turboprop/Turboshaft
    3. Piston
    4. Electric

`aircraft_category` can take on the following values:

    1. LandPlane
    2. SeaPlane
    3. Helicopter
    4. Gyrocopter
    5. Tiltrotor
    6. Amphibian

`body_type` can take on the following values:

| body_type | description |
| --------- | ----------- |
| Helicopter| ALL helicopters |
| UAV | Unmanned Arial Vehicle |
| Private   | Small, private aircraft |
| Regional | Short distance, commercial aircraft |
| Narrow | Longer distance, 1-aisled aircaft |
| Wide | 2-aisled aircraft |
| Freighter | Cargo aircraft |
| Utility | Service aircraft |
| Military | Combat aircraft |

The distinction between the aircraft body types was made according to what we felt would best fit it. Narrow aircraft differed from Regional ones by having 4-or-more abreast seating. The Utility type was introduced after a lot of the database was already complete, so if you feel like any of the aircraft are incorrectly categorized, please let us know. 

# License

This database is published under the [Creative Commons Attribution Non-Commercial ShareAlike](https://creativecommons.org/licenses/by-nc-sa/3.0/legalcode). You can share and modify the work as you wish (we'd be excited to know what you do with it!), but the CFR Aircraft Engines Database must be attributed and the new works must be used non-commercially and under a similar license.

# Contributing

Please feel free to contribute to this database in whichever way you can. If you notice an error with the values (there likely quite a few!) post an issue on the [Issues Tab](https://github.com/The-CFR-Project/AircraftEnginesDatabase/issues) and we'll get back to you as soon as we can. If you have any other suggestions, use the same tab to post them!
