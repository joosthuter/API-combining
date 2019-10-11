# Creating an alarm for your morning commute

We are gonna be creating an Arduino that will tell you when you need to leave in time to catch your train. We are going to be using the [NS API](https://www.ns.nl/en/travel-information/ns-api) to tell the arduino when our train is leaving and we're going to be using  [Zapier Account](https://zapier.com/) to connect our Google Calendar to the device.

### How will this work?

#### Zapier

With [Zapier](https://zapier.com/) we'll make sure that our Arduino gets a notification when you have an appointment set in your calendar. With Zapier you can determine when you get your notification, for instance: you can tell zapier:
> Tell me that I have my appointment an hour before the appointment is.

#### NS API

After we got the notification we'll call the [NS API](https://www.ns.nl/en/travel-information/ns-api). NS is the Dutch railservice, so this API will only tell you the data of dutch trains. You can use this API as an example or you could look up what API's are available for train departures in your counrty/region.

UK: [National Rail](https://www.nationalrail.co.uk/46391.aspx)
India: [rapidapi](https://rapidapi.com/singhkgp/api/indian-rail-api?utm_source=google&utm_medium=cpc&utm_campaign=1672506610_63847892534&utm_term=_b&utm_content=1t2&gclid=Cj0KCQjw0IDtBRC6ARIsAIA5gWt4dImn4OkoyRpxsEmp2Vumv3qduifvLK75nGBvI0fJAwB-Vmhz5EMaAh2BEALw_wcB)

With the [NS API](https://www.ns.nl/en/travel-information/ns-api) we'll request the train departure times at the train station near you. We'll search for a train that arrives at the location of your appointment in time. From that train we'll get the departure time from the station nearest you. 15 Minutes before this train leaves we'll let your Arduino blink it's LED, telling you you need to leave!

### What do we need for this to work?

#### Hardware
- NodeMCU

#### Software
- [NS API](https://www.ns.nl/en/travel-information/ns-api)
- [Zapier Account](https://zapier.com/)

## Step 1

