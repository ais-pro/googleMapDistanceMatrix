# googleMapDistanceMatrix
use http connection to retrieve the google distance in json 


Url
https://maps.googleapis.com/maps/api/distancematrix/json?origins=23.75223408437255,90.37963235475122&destinations=23.758761375530757,90.37364904989002&mode=walking


Url parssing:
https://maps.googleapis.com/maps/api/distancematrix/json<br>
?origins=23.75223408437255,90.37963235475122<br>
&destinations=23.758761375530757,90.37364904989002<br>
&mode=walking


<h3>Travel Modes</h3>

For the calculation of distances, you may specify the transportation mode to use. By default, distances are calculated for driving mode. The following travel modes are supported:

<h4>driving (default)</h4> indicates distance calculation using the road network.
<h4>walking</h4> requests distance calculation for walking via pedestrian paths & sidewalks (where available).
<h4>bicycling</h4> requests distance calculation for bicycling via bicycle paths & preferred streets (where available).
transit requests distance calculation via public transit routes (where available). This value may only be specified if the request includes an API key or a Google Maps APIs Premium Plan client ID. If you set the mode to transit you can optionally specify either a departure_time or an arrival_time. If neither time is specified, the departure_time defaults to now (that is, the departure time defaults to the current time). You can also optionally include a transit_mode and/or a transit_routing_preference.
Note: Both walking and bicycling routes may sometimes not include clear pedestrian or bicycling paths, so these responses will return warnings in the returned result which you must display to the user.


<h3>Retrive Data</h3>
{
   "destination_addresses" : [ "Mirpur Rd, Dhaka, Bangladesh" ],
   "origin_addresses" : [ "17 Panthapath, Dhaka 1205, Bangladesh" ],
   "rows" : [
      {
         "elements" : [
            {
               "distance" : {
                  "text" : "1.1 km",
                  "value" : 1114
               },
               "duration" : {
                  "text" : "14 mins",
                  "value" : 859
               },
               "status" : "OK"
            }
         ]
      }
   ],
   "status" : "OK"
}
