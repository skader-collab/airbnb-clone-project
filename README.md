# airbnb-clone-project
The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security. This project enables learners to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application.
# Team Roles
1. Sekou S kamaera Backend-developer
2. Meek Dukuly- Database admin
3. Kader Kamara- Frontend-developer
# Technology Stack

- **Django**: A robust Python web framework for building the backend, managing database models, user authentication, and providing APIs.
- **PostgreSQL**: A powerful, open-source relational database system used to persist and manage structured data.
- **GraphQL**: An API query language that allows the frontend to request exactly the data it needs, improving efficiency and flexibility.
## Database Design

### Entities and Fields

1. **Users**
   - `id`: Unique identifier for each user.
   - `name`: Full name of the user.
   - `email`: User’s email address.
   - `password`: Hashed password for authentication.
   - `role`: Defines if the user is an admin, property owner, or guest.

2. **Properties**
   - `id`: Unique identifier for each property.
   - `title`: Name or title of the property listing.
   - `description`: Detailed information about the property.
   - `address`: Location of the property.
   - `owner_id`: References the `id` of the user who owns the property.

3. **Bookings**
   - `id`: Unique identifier for each booking.
   - `user_id`: References the `id` of the user who made the booking.
   - `property_id`: References the `id` of the booked property.
   - `start_date`: Booking start date.
   - `end_date`: Booking end date.

4. **Reviews**
   - `id`: Unique identifier for each review.
   - `user_id`: References the `id` of the user who wrote the review.
   - `property_id`: References the `id` of the reviewed property.
   - `rating`: Numeric rating score.
   - `comment`: Text of the review.

5. **Payments**
   - `id`: Unique identifier for each payment.
   - `booking_id`: References the `id` of the related booking.
   - `amount`: Total payment amount.
   - `status`: Payment status (e.g., pending, completed, failed).
   - `payment_date`: Date the payment was made.

### Relationships

- A **User** can own multiple **Properties**.
- A **User** can make multiple **Bookings**.
- A **Booking** is linked to one **Property** and one **User**.
- A **Property** can have multiple **Bookings** and **Reviews**.
- A **Booking** can have one **Payment**.
- A **User** can write multiple **Reviews** for different **Properties**.

## Feature Breakdown

### User Management
Users can sign up, log in, and manage their profiles securely. This feature ensures that only registered users can book properties or list their own properties for rent.

### Property Management
Property owners can create, update, and delete property listings. Each listing includes detailed information, photos, pricing, and availability to help guests find suitable accommodations.

### Booking System
Guests can search for available properties, view details, and make reservations for specific dates. This system handles availability checks, prevents double bookings, and tracks all reservations.

### Review System
After a stay, guests can leave reviews and ratings for properties. This helps maintain quality and trust within the platform, allowing future guests to make informed choices.

### Payment Integration
Secure payment processing is integrated to handle booking payments. This feature ensures transactions are tracked, payment statuses are updated, and owners receive payouts for successful bookings.

### Search and Filtering
Guests can search for properties based on location, price, amenities, and availability. Advanced filtering improves the user experience by helping guests find the perfect property quickly.

### Admin Dashboard
Admins can manage users, properties, bookings, and payments from a centralized dashboard. This feature supports moderation and ensures the platform runs smoothly and securely.

