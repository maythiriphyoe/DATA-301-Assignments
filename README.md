### Project Overview 

This project provides a simple Python-based simulation of a restaurant's customer flow and table management. It models customers arriving (both walk-ins and reservations), waiting in a priority queue, being seated at available tables, and tables progressing through various dining stages before being freed and cleaned.

### Functions 

- Customer Management: Customers are defined by their name, party size, and whether they have a reservation.
- Priority Queue: Customers are added to a priority queue that prioritizes reservations over walk-ins, and earlier reservation times (or arrival times for walk-ins) over later ones.
- Table Management: Tables have capacities and statuses (available, occupied, dirty, cleaned).
- Table Assignment Logic: The restaurant attempts to seat customers from the priority queue based on table availability and size matching.
- Dining Stages: Tables can progress through various stages like "seated", "ordered", "food_served", "bill_requested", and "paid", ultimately becoming "dirty" and needing to be "cleaned".
- Waiting List: Customers who cannot be immediately seated are placed on a waiting list and are prioritized when tables become available.

### Code Structure
The project is built using four main classes: Customer, PriorityQueue, Table and Restaurant.

- Customer: Defines customer attributes (name, size, reservation status) and their priority logic for seating.
- PriorityQueue: Manages the queue of waiting customers, automatically sorting them by priority (reservations first, then arrival/reservation time).
- Table: Represent dining tables with its capacity, current status (available, occupied, dirty), and the dining stage of its current customer.
- Restaurant: sets up tables, manages customer flow from the PriorityQueue to Tables, handles table status updates, and oversees table assignment logic.
