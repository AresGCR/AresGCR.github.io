---
title:"Breakable Toy II"
date: 2024-09-05 00:00:00 +0800
categories:[Breakable Toy]
---

# Breakable Toy II
## Problem Overview
The flight search app is designed to provide users with the ability to search for flights and view flight details. The app is built with a React, Typescript  frontend and a Java Spring Boot backend. It integrates the Amadeus API to fetch flight data and displays it in a user-friendly format.
1. **FlightSearch Component**:
   - This component is the entry point where users input their departure, arrival airports, and travel dates.
   - After submission, it triggers a search request, making an API call to retrieve available flights.
   - Once flights are retrieved, the component redirects the user to the flights display page.

2. **Flights Component**:
   - Displays the list of flights fetched from the backend API.
   - Each flight shows key information like departure/arrival times, airline, duration, and price.
   - Users can click on a flight to view more detailed information, which navigates to the `FlightDetail` page.

3. **FlightDetail Component**:
   - Shows in-depth details about a single flight, including segments , aircraft type, and more.
   - It presents both summary-level information and per-segment details.

4. **Backend (Java Spring Boot)**:
   - The backend exposes APIs to fetch flight data. 
   - The flight data is structured and returned as a JSON response that the frontend can consume.
   - The backend uses a `AmadeusApiService` class to fetch flight offers from the API.

## API Integration
**getFlight**: The primary API call that retrieves flight data. It sends a request to the backend's `/fetch-flight-summary` endpoint.
- The API response contains flight summary information, including segments, pricing, and airlines, which is displayed on the frontend.


## Alternative Solutions – What Else Was Considered?
One and most important inconvenience was the Amadeus API because most of the develop time was shut down and I could not fetch data to develop the application 
#### Solution : **Using a Mock Service Class in Backend**
We used a mock service class in the backend (`MockAmadeusApiService`) to simulate API responses in conjuction with a static JSON file.

**Pros**:
- More realistic simulation of API behavior.
- Ability to control mock responses dynamically.

**Cons**:
- Additional complexity to develop mock service logic.
- Refactoring some lines of the code to develop with this solution.
- This is not what is requiered to be developed.



