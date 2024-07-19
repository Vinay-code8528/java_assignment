# java_project

Purpose
The purpose of this Java program is to accept latitude and longitude coordinates as input and return the corresponding country code in ISO 3166-1 alpha-2 format. This implementation does not rely on external API calls; instead, it uses a local in-memory dataset of bounding boxes to map coordinates to countries.

Components

1: Country Class:

Represents a country with its ISO 3166-1 alpha-2 code and bounding box coordinates.
Methods:
Country(String code, double minLat, double maxLat, double minLon, double maxLon): Constructor to initialize a country with its code and bounding box.
boolean contains(double lat, double lon): Checks if the given latitude and longitude fall within the country's bounding box.

2: GeoLocationToCountry Class:

Contains a static list of Country objects initialized with sample data.
Methods:
static { }: Static block to initialize the list of countries with example bounding boxes.
static String getCountryCode(double latitude, double longitude): Iterates through the list of countries and checks if the given coordinates fall within any country's bounding box. Returns the country code if found, otherwise returns "Unknown".
public static void main(String[] args): Main method to take user input for latitude and longitude, and print the corresponding country code.


Explanation

1- Country Class:

Represents a country with its ISO 3166-1 alpha-2 code and bounding box coordinates (minimum and maximum latitude and longitude).
The contains method checks if a given latitude and longitude fall within the bounding box of the country.

2- GeoLocationToCountry Class:

COUNTRIES List: A static list that holds Country objects. It's initialized with example data for the US, Canada, and India. This list should be expanded with a comprehensive dataset for practical use.
getCountryCode Method: Iterates through the COUNTRIES list and uses the contains method of each Country object to check if the input coordinates fall within any country's bounding box. Returns the country code if a match is found, otherwise returns "Unknown".
main Method: Prompts the user to enter latitude and longitude values, calls the getCountryCode method with these values, and prints the resulting country code.




