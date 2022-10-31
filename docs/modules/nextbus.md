# NextBus

Displays information about the next bus for a particular stop. Useful for determining when to leave the house.

> Note that not all bus services around the world serves bus data through umoiq/NextBus. For those that don't, you will need to write the appropriate module to integrate with those APIs if they exist.

This module integrates the predictions command from the umoiq/NextBus API. [http://www.nextbus.com/xmlFeedDocs/NextBusXMLFeed.pdf](http://www.nextbus.com/xmlFeedDocs/NextBusXMLFeed.pdf).  

## Configuration

If the transit agency exists on this UI, we can configure this module. [https://retro.umoiq.com/](https://retro.umoiq.com/).  

To make JSON easier to read in the browser, try this chrome extension [JSONView](https://chrome.google.com/webstore/detail/jsonview/gmegofmjomhknnokphhckolhcffdaihd?hl=en).

1. To get the agency tag for your local transit agency, look through this list:  
`https://webservices.umoiq.com/service/publicJSONFeed?command=agencyList`

2. Once you locate your transit agency tag, you can view the list of available bus routes and route tag by replacing `<AGENCY TAG>` with your agency tag from step 1.  
`https://webservices.umoiq.com/service/publicJSONFeed?command=routeList&a=<AGENCY TAG>`

3. Once you locate your desired bus route, you can find the `stopID` you are interested in tracking by replacing `<AGENCY TAG>` with your transit agency tag from step 1 and by replacing `<ROUTE TAG>` with your desired route from step 2.
`https://webservices.umoiq.com/service/publicJSONFeed?command=routeConfig&a=<AGENCY TAG>&r=<ROUTE TAG>`

Once you have these 3 values, you can populate it in the `yaml` config.

#### Example:  
Step 1: `stl`  
Step 2: `24E`  
Step 3: `43428`  

#### Would result in: 
```yaml
nextbus:
    enabled: true
    border: false
    agency: stl
    route: 24E
    stopID: 43428
    position:
        top: 12
        left: 0
        width: 24 
        height: 2
    refreshInterval: 20s
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="agency", desc="Transit agency of your bus.", value="Ex. `stl` from https://webservices.umoiq.com/service/publicJSONFeed?command=agencyList" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="route", desc="Route Number of your bus.", value="Ex. `24E` from https://webservices.umoiq.com/service/publicJSONFeed?command=routeList&a=stl" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="stopID", desc="Your bus stop number.", value="Ex. `43428` from: https://webservices.umoiq.com/service/publicJSONFeed?command=routeConfig&a=stl&r=24E" %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Screenshots 

The output format is `<Bus route name> | ETA [<Minutes>:<Seconds>]`
<img class="screenshot" src="/assets/modules/nextbus.png" alt="nextbus screenshot" />

According to the above screenshot, the next #24 bus is in 16 minutes and 43 seconds.

{% set src="nextbus" %}
{% include "src_path.md" %}