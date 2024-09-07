1. Introduction
  The Airport Management System is a simple console-based Python project designed to simulate the basic operations of an airport management system. The system allows users to manage flight information, book and cancel tickets, and maintain a passenger list for flights. The system is intended to provide a functional demonstration of how an airport could manage flights and passengers using Python object-oriented programming (OOP).
  This project uses Python classes to model real-world entities such as flights and passengers and provides a menu-driven interface for users to interact with the system.

2. Objective
  The main objective of this project is to create a simple, efficient, and interactive Airport Management System. It allows users to:

  Add flights to the system.
  View available flights.
  Book and cancel passenger tickets.
  View passenger lists for specific flights.
  Remove flights from the system.
3. Project Overview
  The project consists of the following key components:

  Flight Class: Represents individual flights, containing details like flight number, origin, destination, available seats, and a list of passengers.
  Passenger Class: Represents individual passengers, containing their name and passport number.
  Airport Management System Class: Manages the list of flights and handles operations like adding/removing flights and managing ticket bookings.
  Main Function: Provides a user interface where the user can interact with the system via a menu-based interface.
**4. System Design**
4.1 Flight Class
  The Flight class is responsible for managing individual flights. It contains attributes like the flight number, origin, destination, available seats, and a list of passengers. The class also contains methods for booking and canceling tickets, as well as displaying the passenger list.

Attributes:

  flight_number: Unique identifier for the flight.
  origin: The starting point of the flight.
  destination: The flight's destination.
  seats_available: The number of available seats for booking.
  passengers: A list of Passenger objects booked on this flight.
Methods:

  book_ticket(): Books a ticket for a passenger if seats are available.
  cancel_ticket(): Cancels a passenger's ticket.
  show_passenger_list(): Displays the list of passengers on the flight.
4.2 Passenger Class
  The Passenger class models the passengers in the system, storing their names and passport numbers. The passenger is added to the flight they are booking.

Attributes:
  name: Passenger's name.
  passport_number: Unique passport number for identification.
4.3 Airport Management System Class
  This class manages the overall system. It keeps a record of all flights and provides methods for adding, removing, and retrieving flights. It acts as the core controller for handling all system operations.

Attributes:
  flights: A list of available Flight objects.
Methods:
  add_flight(): Adds a new flight to the system.
  remove_flight(): Removes a flight from the system.
  get_flight(): Fetches a specific flight by flight number.
  list_flights(): Displays a list of available flights with seat availability.
4.4 User Interface
  The main() function acts as the interface between the user and the system. It provides a menu-based interaction, allowing the user to:

  Add or remove flights.
  Book or cancel tickets.
  View the list of available flights.
  Show the passenger list for a flight.
  The program runs in a loop until the user selects the option to exit.

5. Code Breakdown
  Here is a breakdown of the project's key components:

5.1 Flight Class Implementation
  The Flight class contains methods for ticket booking and cancellation:

  book_ticket(): Books a ticket for the passenger and reduces the available seats.
  cancel_ticket(): Removes a passenger and increases available seats.
  show_passenger_list(): Lists all passengers booked on the flight.
5.2 Passenger Class Implementation
  The Passenger class simply stores the name and passport number of a passenger. It is used to create passenger objects when booking tickets.

5.3 Airport Management System Implementation
  This class is the system's controller, which manages all flights and flight-related operations. It:

Stores flights in a list.
  Allows adding and removing flights.
  Facilitates ticket booking and cancellation by managing Flight objects.
5.4 User Interface
  The menu-based interface lets users perform operations like adding flights, booking tickets, and viewing passenger lists.

6. Key Features
  Add Flights: Users can add new flights to the system, specifying the flight number, origin, destination, and available seats.

  Remove Flights: Flights can be removed from the system by specifying the flight number.

  View Available Flights: Displays all available flights and the remaining seats for each flight.

  Book Ticket: Passengers can book a flight ticket if seats are available. The system will store the passenger details on the flight.

  Cancel Ticket: Passengers can cancel their ticket, freeing up a seat on the flight.

  View Passenger List: Displays the list of passengers who have booked tickets on a particular flight.

7. Example Output

   Airport Management System
1. Add Flight
2. Remove Flight
3. List Flights
4. Book Ticket
5. Cancel Ticket
6. Show Passenger List
7. Exit

Choose an option: 1
Enter flight number: AI101
Enter flight origin: New York
Enter flight destination: London
Enter the number of available seats: 200
Flight AI101 added.

Choose an option: 3
Available flights:
AI101: New York to London - Seats Available: 200

Choose an option: 4
Enter the flight number to book: AI101
Enter passenger name: John Doe
Enter passport number: 123456789
Ticket booked for John Doe on flight AI101

Choose an option: 6
Enter flight number to show passengers: AI101
Passengers on flight AI101:
- John Doe

8. Limitations and Future Enhancements
  Passenger Search: The current implementation finds passengers by name only. In the future, the system could use passport numbers for more precise passenger identification.

  Flight Management: Future versions could include more advanced flight management, such as updating flight details or integrating with real-world APIs to fetch flight statuses.

  Graphical User Interface (GUI): The current version uses a command-line interface. In future versions, a graphical user interface could be added for better user interaction.

  Database Integration: The current version stores flight and passenger information in memory (during runtime). Future versions could integrate a database system for persistent data storage.

9. Conclusion
  The Airport Management System built using Python demonstrates a simplified approach to managing flights and passengers in an airport. This project uses object-oriented programming principles to model real-world entities and offers an easy-to-use menu interface for operations. While basic in its current form,
  the system can be enhanced further for more sophisticated management features, such as seat selection, integration with real-time flight data, and persistent data storage.
