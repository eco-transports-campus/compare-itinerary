![Polytech Paris-sud](https://www.usinenouvelle.com/mediatheque/3/4/0/000268043_image_260x175.jpg)
# compare-itinerary
A module to compare an itinerary with an array of itineraries.

## Prerequisite
...

## Install
```
npm install compare-itinerary
```

## Example
```javascript
// Import package
var compareItinerary = require("compare-itinerary")

const trajects = compareItinerary.getSameTrajects()

console.log(trajects)
```

## Returned value
```json
{
   "destination_addresses" : [ "91400 Orsay, France" ],
   "origin_addresses" : [ "Paris, France" ],
   "rows" : [
      {
         "elements" : [
            {
               "distance" : {
                  "text" : "32,0 km",
                  "value" : 31962
               },
               "duration" : {
                  "text" : "38 minutes",
                  "value" : 2295
               },
               "status" : "OK"
            }
         ]
      }
   ],
   "status" : "OK"
}
```
