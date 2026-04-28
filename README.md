# ZIP to KML

A small, static web tool for generating KML boundary files from U.S. ZIP codes using U.S. Census TIGER/Line data.

## What This Project Includes

- `generate-kml.html`: Main app that:
  - accepts up to 200 unique 5-digit ZIP codes,
  - fetches ZIP boundary geometry from the U.S. Census TIGERweb API,
  - builds a downloadable `.kml` file for use in Google My Maps and GIS tools.
- `index.html`: A step-by-step guide for creating, embedding, and maintaining a service area map in Google My Maps.

## Features

- Paste ZIPs separated by commas, spaces, or new lines
- De-duplicates ZIP codes automatically
- Batch requests to Census API (with progress + logs)
- Handles partial matches and reports missing ZIP boundaries
- Custom area name and fill color
- One-click KML download

## How to Use the Generator

1. Open `generate-kml.html`.
2. Paste ZIP codes.
3. Choose a fill color and area name (optional).
4. Click **Generate KML**.
5. Click **Download KML File**.
6. Import the file into Google My Maps (or another GIS tool).

## Data Source

Boundary data is retrieved from:

- U.S. Census Bureau TIGERweb / TIGER-Line (public API)

## Privacy Notes

- No backend server is included in this project.
- ZIP lists are processed in-browser and sent directly to the Census API.

## Limitations

- Supports U.S. 5-digit ZIP code inputs only.
- Some ZIP codes may not return boundary data from the source dataset.
- API availability/performance depends on the Census service.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
