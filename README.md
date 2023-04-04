# Global-Flight-Schedules-API
Global airport timetable data with real-time status updates

<div id="header" align="center">
  <img src="https://media.giphy.com/media/LRZc4dV2kf787nbOB3/giphy.gif" width="100"/>
</div>

[Aviyair’s Global Flight Schedules API](https://aviyair.com/global-flight-schedules-api/) has useful airport timetable data with real-time updates for airports around the world. The REST structure allows fetching the in JSON easily with GET requests and other formats may be added in the future. 
The API provides real-time airport schedule data with static data such as the flight number, airline, departure and arrival airports etc. as well as updated, real-time data such as flight status, delay, scheduled/estimated/actual departure and arrival airport, gate, baggage belt and more. 

Get complete airport schedule data in a single call or narrow down the data to flights of a certain airline, flight number, status and others.

--------

## Main Endpoint and Filters with Description

**GET** https://data.aviyair.com/data/v1/liveschedule?key=[APIKEY]&airport_aita=IAD&type=departure

Airport IATA code and schedule type (can be either departure or arrival) are obligatory fields. You can add the below filters to narrow down the flights within the schedule

| Request Parameter  | Description |
| ------------- | ------------- |
| airport_iata  | Filter the flights based on the three-letter IATA code for arrival airport  |
| type  | Filter the flights based on the aircraft status as either depature or arrival   |
| status  | Filter the flights based on the flight status designated as (started, en-route, landed, unknown) For outputs limit the value  |
| departure_iata  | Filter the flights based on the three-letter IATA code of the departure airport  |
| departure_icao | The ICAO code for departure airport |
| departure_terminal | Departure flight's terminal |
| departure_delay  | Departure delay measured in minutes  |
| departure_sch_time  | Scheduled departure of flight  |
| departure_est_time | Estimated time of departure of the fligth  |
| departure_act_time  | The actual time of departure of the flight |
| departure_est_runway  | Estimated time of departure at runway  |
| departure_act_runway | The actual time of departure at runway |
| arrival_iata | The IATA code of arrival airport  |
| arrival_icao | The ICAO code for arrival airport  |
| arrival_terminal| Arrival flight's terminal |
| arrival_delay| Arrival delay measured in minutes |
| arrival_sch_time| Scheduled arrival time of the flight |
| arrival_est_time| Estimated arrival time of the flight|
| arrival_act_time| Actual arrival time of the flight upon landing |
| arrival_est_runway| Estimated time of arrival at runway |
| arrival_act_runway| Actual time of arrival at runway |
| airline_name| Airline name |
| airline_iata| Airline IATA code |
| airline_icao| Airline ICAO code |
| flight_number| Flight number |
| flight_iata| IATA format of the flight number |
| flight_icao| ICAO format of the flight number |

------

## 200 OK Response Example

```
{
  "status": {
    "message": "Success"
  },
  "results": {
    "airline": {
      "iataCode": "ID",
      "icaoCode": "BTK",
      "name": "Batik Air"
    },
    "arrival": {
      "actualRunway": "2023-03-15T14:23:00.000",
      "actualTime": "2023-03-15T14:23:00.000",
      "baggage": null,
      "delay": null,
      "estimatedRunway": "2023-03-15T14:23:00.000",
      "estimatedTime": "2023-03-15T14:21:00.000",
      "gate": null,
      "iataCode": "MKZ",
      "icaoCode": "WMKM",
      "scheduledTime": "2023-03-15T14:50:00.000",
      "terminal": null
    },
    "codeshared": null,
    "departure": {
      "actualRunway": "2023-03-15T12:49:00.000",
      "actualTime": "2023-03-15T12:49:00.000",
      "baggage": null,
      "delay": "4",
      "estimatedRunway": "2023-03-15T12:49:00.000",
      "estimatedTime": null,
      "gate": null,
      "iataCode": "PKU",
      "icaoCode": "WIBB",
      "scheduledTime": "2023-03-15T12:45:00.000",
      "terminal": null
    },
    "flight": {
      "iataNumber": "ID311",
      "icaoNumber": "BTK311",
      "number": "311"
    },
    "status": "landed",
    "type": "arrival"
  }
}

```

-------


## Full Documentation

Please visit our [website]( https://aviyair.com/documentation/).

-------

## Most Popular Use Cases

These are the most common use cases for the Global Flight Schedules API but there are no limitations regarding how the API can be useful for you. If you have any concerns about the Terms and Conditions for the global flight schedule data, you may visit the hyperlink below or contact us to ask about it.

-	Real-time interactive timetables where people can track the current status and delay information of their flights
- Flight schedule tracking for booking or travel websites and apps
-	Flight status tracking for travel agencies and airport greeting services
-	Air traffic analysis in real-time with scheduled, estimated and actual flight times
- Airline performance analysis
- Airport operation and saff planning and improvements based on air traffic data per terminal or the whole airport
- Route efficiency comparison
-	Gate assessment in airports

---------

## License

[Terms and Conditions of Use](https://aviyair.com/terms-and-conditions/) apply. If you have any questions or concerns about your use case of the Flight Tracker and Status API, please [contact us](https://aviyair.com/contact-aviyair/). 

--------

## How to Access

The API key to access global flight schedule data is possible by creating an API subscription. The subscriptions do not require any commitments. It is possible to cancel anytime or make changes to your subscription level.

[View the prices and get an API key here.](https://aviyair.com/pricing-subscription-plans/)
