Canadian Biodiversity and Global Forest Decline
-------
In this ETL and interactive visualization project, I examine Canadian biodiversity decline and forested area loss. I used a variety of tools for the ETL process and the construction of a web app including Flask, sqlalchemy, SQL, Geoapify, ajax, D3, Plotly, and DataTables. 

Highlights
-------

'''
# Define a function to geocode country names and get coordinates using Geoapify
def geocode_country(country):
    try:
        params = {
            'text': country,
            'apiKey': api_key,
        }
        response = requests.get(api_endpoint, params=params)
        data = response.json()

        if 'features' in data and data['features']:
            latitude = data['features'][0]['properties']['lat']
            longitude = data['features'][0]['properties']['lon']
            return latitude, longitude
        else:
            return None, None
    except requests.exceptions.RequestException:
        return None, None
'''




Resources: 
-------
Regional breakdown of the status of wild species, Canada, 2020
https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/general-status-wild-species.html

National conservation status of wild species, Canada, 2020
https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/general-status-wild-species.html

General status of species in selected groups, Canada, 2020
https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/general-status-wild-species.html


Trends in bird populations by species group, Canada, 1970 to 2016
https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/trends-bird-populations.html
									

Canadian species index, percentage change, 1970 to 2016
https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/canadian-species-index.html


https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/general-status-wild-species.html#status-assessment
							

World Forest Cover Trends:
https://www.kaggle.com/datasets/parasharmanas/world-forest-cover-trends


Additional information available: 
https://www.canada.ca/en/environment-climate-change/services/species-risk-public-registry/general-status/wild-species-2020.html

Images sources included in HTML. 
