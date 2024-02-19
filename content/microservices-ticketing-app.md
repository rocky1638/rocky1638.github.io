# Microservices Ticketing App

## Features.
- Users can list ticket for an event.
- Other users can purchase this ticket.
- Ticket is locked for some time when a user begins purchasing a ticket.
- While locked, no one else should be able to edit or purchase the ticket.
- Ticket prices can be edited if they are not locked.

## Services.
- Authentication service.
	- For user accounts.
- Tickets service.
	- For ticket creation/editing.
- Orders service.
	- For creating/editing orders.
- Expiration service.
	- For watching for orders and cancelling them after some time.
- Payments service.
	- For handling credit card payments, watch the related order.

## Error handling.
- Because we have microservices that might be running different backends, we should have a common error library so the formats are the same!

Categories:: [[microservices]]