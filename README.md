# BowieCountyParcelMap
This mapbox project visualizes Bowie County parcel data in a color coded format.


# Texarkana Parcel Viewer & Selector

An interactive web application that allows users to explore, inspect, and export land parcel data using a custom Mapbox tileset and style. This tool is designed for urban planners, real estate professionals, investors, and local officials to analyze parcel-level data with ease.

## Features

- Custom Mapbox style and vector tileset integration
- Click on any parcel to view detailed property attributes
- "Add to Queue" functionality for selected parcels
- Display of queued parcels in a persistent top bar
- Shift + Drag selection for bulk parcel highlighting
- Visual highlighting of selected parcels
- Export selected parcels as GeoJSON or CSV
- Scrollable popup windows displaying over 30 parcel metadata fields

## Technologies Used

- Mapbox GL JS
- JavaScript, HTML5, CSS3
- Vector Tiles hosted on Mapbox
- GeoJSON export

## Data Sources

This viewer is designed to work with a custom vector tileset derived from county-level parcel data. The following Mapbox assets are used:

- **Tileset ID**: `bymarkallan.1ghta18f`
- **Style URL**: `mapbox://styles/bymarkallan/cmd5li67d00br01s88rpmf4lv`
- **Layer Name (source-layer)**: `stratmap24-landparcels_48037_lp`

## Parcel Metadata Fields Displayed

When available, the popup displays the following attributes:

- COUNTY, DATE_ACQ, FIPS, GEO_ID, GIS_AREA, GIS_AREA_U
- IMP_VALUE, LAND_VALUE, LEGAL_AREA, LEGAL_DESC, LGL_AREA_U
- LOC_LAND_U, MAIL_ADDR, MAIL_CITY, MAIL_LINE1, MAIL_LINE2
- MAIL_STAT, MAIL_ZIP, MKT_VALUE, NAME_CARE, OBJECTID
- OWNER_NAME, Prop_ID, SITUS_ADDR, SITUS_CITY, SITUS_NUM
- SITUS_STAT, SITUS_STRE, SITUS_ST_1, SITUS_ST_2, SITUS_ZIP
- SOURCE, STAT_LAND_, TAX_YEAR, YEAR_BUILT

All fields are conditionally shown only if data is available for that parcel.

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/parcel-viewer.git
   cd parcel-viewer

	2.	Set your Mapbox access token
Open index.html and replace:

mapboxgl.accessToken = 'YOUR_MAPBOX_ACCESS_TOKEN';


	3.	Serve the application
You can use any static file server. Here are a few options:
	•	Python 3

python3 -m http.server


	•	Node (serve)

npx serve .


	•	VS Code Live Server
	•	Install the extension
	•	Open index.html and click “Go Live”

	4.	Open your browser
Navigate to http://localhost:8000 (or whatever port your server uses)

Usage
	•	Click a parcel to view its information
	•	Click “Add to Queue” in the popup to track it
	•	Use Shift + Drag to select multiple parcels at once
	•	Export your selected parcels using the top-left dropdown and “Export” button

Customization

To use your own tileset:
	•	Update the map.addSource() configuration in index.html with your Mapbox tileset URL
	•	Update the style field with your own Mapbox style URL
	•	Ensure the source-layer name matches the name of your layer in Mapbox Studio

License

This project is open-source and available under the MIT License.

Contact

For feedback, questions, or support, please contact [yourname] at [your.email@example.com].

---

Let me know if you’d like:

- A live deployment version (e.g., GitHub Pages)
- Instructions for customizing filters (e.g., by acreage or owner)
- A `.env` setup for the Mapbox token

Happy to help make it production-ready.
