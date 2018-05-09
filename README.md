![Polytech Paris-sud](https://www.usinenouvelle.com/mediatheque/3/4/0/000268043_image_260x175.jpg)
# compare-itinerary
_version 1.0.1_

A module to compare an itinerary with an array of itineraries.

## Utility
This module allow you to give an itinerary, a stock of itinerary and a radius and see if there is already one existing itinerary that match your itinerary. You can modify the value of the radius in meter.

Since the version 1.0.2, you can also compare 2 place to see if the distance between them is smaller than a given distance.

## Install
```
npm install compare-itinerary
```

## Example to compare itinerary
```javascript
// Import package
var compareItinerary = require("compare-itinerary")

const trajects = compareItinerary.getSameTrajects(itinerary, existingItinerary, radius);

console.log(trajects)
```

## Input value example
```javascript
var existingItinerary = [{id: 1, from: {lat: 48.6895, lon: 2.1855}, to: {lat: 48.7090, lon: 2.171}},
			{id: 2, from: {lat: 48.69546, lon: 2.1631}, to: {lat: 48.7090, lon: 2.171}},
			{id: 3, from: {lat: 48.7075, lon: 2.23745}, to: {lat: 48.7090, lon: 2.171}},
			{id: 3, from: {lat: 48.68775, lon: 2.18799}, to: {lat: 48.7090, lon: 2.171}},
			{id: 4, from: {lat: 48.7090, lon: 2.171}, to: {lat: 29.026, lon: 34.399}}];
                        
var itinerary = {from: {lat: 48.68775, lon: 2.18799}, to: {lat: 48.7090, lon: 2.171}};

var radius = 250; //the value in meters of the max distance betwin the base traject and the existing one.
```

## Returned value
```javascript
[
   {
      id: 1,
      from : {
         lat : 48.6895,
         lon : 2.1855
      },
      to : {
         lat : 48.7090,
         lon : 2.171
      }
   },{
      id: 3,
      from : {
         lat : 48.68775,
         lon : 2.18799
      },
      to : {
         lat : 48.7090,
         lon : 2.171
      }
   },
]
```

## Example to compare place
```javascript
// Import package
var compareItinerary = require("compare-itinerary")

const near = compareItinerary.isNear(placeOne, placeTwo, radius);

console.log(near)
```

## Input value example
```javascript
                        
var placeOne = {lat: 10.434, lon: 20.214}; 
var placeTwo = {lat: 10.459, lon: 20.194}; 

var radius = 500; //the value in meters of the max distance between the two place
```



## Returned value
```javascript
true
```
