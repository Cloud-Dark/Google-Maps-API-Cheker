# Google Maps API Vulnerability Scanner

## Overview
The **Google Maps API Vulnerability Scanner** is a Python script designed to test the vulnerability of Google Maps API keys. It scans various endpoints and checks if the provided API key is accessible or vulnerable to unauthorized usage.

## Features
- Supports multiple Google Maps API endpoints.
- Tests vulnerability by attempting API requests.
- Outputs results in a tabular format, including:
  - API name.
  - Cost associated with the API.
  - Vulnerability status.
  - Details about the result.
- Provides references for up-to-date pricing.

## Installation
1. Clone or download this repository.
2. Ensure you have Python installed (version 3.6 or above).
3. Install required dependencies:
   ```bash
   pip install requests pandas
   ```

## Usage

### Run via Command Line
```bash
python maps_api_scanner.py --api-key YOUR_API_KEY
```
Replace `YOUR_API_KEY` with the Google Maps API key you want to test.

### Run Without Arguments
If you do not provide an API key as a command-line argument, the script will prompt you to enter it:
```bash
python maps_api_scanner.py
```
Enter your API key when prompted.

### Help
To view help information:
```bash
python maps_api_scanner.py --help
```

## Output
The script generates a tabular output displaying:
- API Name.
- Cost per 1000 requests.
- Vulnerability status (`Yes` or `No`).
- Details (e.g., API URL or reason for failure).

## Supported Google Maps APIs
The script tests the following APIs:
1. Staticmap API
2. Streetview API
3. Directions API
4. Geocode API
5. Distance Matrix API
6. Find Place From Text API
7. Autocomplete API
8. Elevation API
9. Timezone API
10. Nearest Roads API
11. Snap to Roads API
12. Speed Limits API
13. Geolocation API
14. Place Details API
15. Nearby Search API
16. Text Search API
17. Places Photo API

## Example Output
### Tabular Example
| API Name               | Cost                     | Vulnerable | Details       |
|------------------------|--------------------------|------------|---------------|
| Staticmap API          | $2 per 1000 requests     | Yes        | <API URL>     |
| Streetview API         | $7 per 1000 requests     | No         | <Reason>      |
| Directions API         | $5 per 1000 requests     | Yes        | <API URL>     |
| Geocode API            | $5 per 1000 requests     | No         | <Reason>      |
| Distance Matrix API    | $5 per 1000 elements     | Yes        | <API URL>     |

Reference for up-to-date pricing:
https://cloud.google.com/maps-platform/pricing
https://developers.google.com/maps/billing/gmp-billing

## Notes
- Ensure your API key has the necessary permissions enabled.
- Unauthorized usage of API keys may lead to unexpected charges.
- Use responsibly to test only your own API keys.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## References
- [Google Maps Platform Pricing](https://cloud.google.com/maps-platform/pricing)
- [Google Maps API Documentation](https://developers.google.com/maps/documentation)

