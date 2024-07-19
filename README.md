Purpose:
The purpose of this Java program is to accept latitude and longitude coordinates as input and return the corresponding country code in ISO 3166-1 alpha-2 format. This implementation does not rely on external API calls; instead, it uses a local in-memory dataset of boundry value to map coordinates to countries.

Explanation-

1: Country Class:

:- Represents a country with its ISO 3166-1 alpha-2 code and boundry value coordinates.
   Country(String code, double minLat, double maxLat, double minLon, double maxLon): This Constructor is used to initialize the property of Country class with the provided 
   data.

:- boolean contains (double lat, double lon): this method Checks if the given latitude and longitude falls within the country's boundry value.

2: GeoLocationToCountry Class:

Contains a arraylist of Country objects initialized with the range of longitute and latitude data.
Methods:
static { }: Static block to initialize the list of countries  with different  boundry value of different countries.
static String getCountryCode(double latitude, double longitude): Iterates through the list of countries and checks if the given coordinates fall within any country's boundry values. Returns the country code if found, otherwise returns "Unknown".
public static void main(String[] args): Main method to take user input for latitude and longitude, and print the corresponding country code.







