# Airline Case Study
This case study aims to analyse the flight operations using characteristics for Airline A and subsequently suggesting the best aircrafts to a start-up airline B by using the previously available data.

### Data Description
Part A - Airline A is currently flying a large international network. Their flight operations are shown in the tab "Operations". Various aircraft characteristics are listed in tab "AC characteristics". They would like to know the following:
1. What is the total cost by aircraft type for the year? </br> Note:	Total cost = Hours flown * Costs/hour									
2. Which aircraft type  has the lowest cost per seat per km flown?

Part B - Airline B is a startup airline and is considering flying on the city pairs as shown in tab "City Pairs". They would like to know: </br>
Which aircraft types are best suited for their operation? </br>

Note:	This is an optimization between 3 factors: Range, Passenger demand, and Costs. Hence the aircraft which is capable of flying between 2 cities (range), has enough seats to meet the demand, and has the lowest cost will win. Also note that the passenger demand is per day, hence an aircraft can make several trips between 2 cities to meet that demand. One aircraft type will always be most suitable for a given city pair. Hence resultant fleet would be a mix of different aircraft types.

### Data manipulation
The data for this problem is provided in an excel file with several sheets, thus warranting the need for data cleaning, which is done by readjusting the header and dropping unnecessary columns for all sheets.

### Analysis
**PART A** </br>
1. Total cost by aircraft type for the year: This parameter deals with the cost incurred by running the different types of aircraft throughout the year. It has a relatively simple calculation as follows: </br>

_Total cost = Total hours flown * Costs / hour_ </br>

It would be prudent to give priority to **ATR72** for travel on the conditions that the passenger demand doesn’t exceed the seat limit (75) and the distance is less than 1000 km.

2. Lowest cost per seat per km flown: This parameter deals with the cost associated with each seat in an aircraft over a kilometre long journey. It can be formulated as: </br>

_Cost per seat per kilometre = (Total cost) / (No.of seats * Total hours * Avg.speed)_ </br>

The most economically efficient aircraft type in terms of per-seat cost by kilometre is **A330**. It is this reason why Airline A chose **A330** for the maximum air travel hours. </br>

**PART B** </br>

The start-up Airline B, wants to find out which aircraft type is the best option for their fleet, keeping in mind the range, passenger demand, and cost incurred.
Priorities in this case study are given to the following parameters:
* Range: Ensuring that the aircraft is able to cover the distance between two given cities.
*	Number of seats: The number of trips required for an aircraft to fully meet the passenger demand.
*	Total trip cost: The amount it takes for an aircraft type to make one or more trips to the destination.

Using direct cost-based analysis as well as manual study, the following conclusions can be made for Airline B: </br>
1. In the first instance, the same aircraft is considered for travel between a city pair. A parameter 'Total cost of the trip' was calculated as follows: </br>

Findings show that aircraft types **A320** and **A330** prove to be more efficient than others.

2. In the second instance, upon manual inspection, the results corroborated with those in the first instance, confirming yet again that **A330** and **A320** are most suitable for travel between city pairs AA-BB, BB-CC and CC-AA, AA-DD respectively. </br>

### Conclusion
Thus, the start-up Airline B can use **4 aircrafts of type A320 and 4 aircrafts of type A330** for an optimal travel scheme. </br>
