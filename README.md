Task 1: Backend Setup with Express, MongoDB, and Validation
Key Components and Packages
Express.js: Used as the server framework, handling API requests, routing, and middleware management.

MongoDB and Mongoose: MongoDB stores data for users, products, and orders. Mongoose ORM was utilized to define schemas, models, and manage data relationships.

Data Validation: Ensures data integrity using libraries such as express-validator for server-side form validation and validator to sanitize input data, safeguarding against malicious user inputs.

Authentication and Authorization:

bcrypt: Hashes passwords for secure storage.
JSON Web Token (JWT): Manages secure user authentication with token-based access. Tokens are generated at login and verified on each request to protect sensitive routes.
Backend Implementation Steps
Express Server Setup:

Created an Express server with RESTful API routes for authentication, product management, and order processing.
Defined middlewares for error handling and authentication.
User Model:

Defined in Mongoose, including fields for username, email, password (hashed using bcrypt), and roles for access control.
Form Validation with express-validator:

Implemented validation rules in routes to verify email format, password length, and other critical data points before saving to MongoDB.
JWT Authentication:

Integrated JWT to issue a token upon login.
Protected specific API routes using JWT verification middleware to confirm user identity before proceeding.

Task 2: Frontend with React, Hooks, and Redux for State Management
Key Components and Technologies
React: Used for building dynamic and responsive front-end components.

React Hooks: Simplified state and lifecycle management within functional components.

useState: Manages component-level state for form inputs, loading indicators, and dynamic UI elements.
useEffect: Handles side effects, like fetching data from the server when the component mounts.
useContext: Shares data across components without prop drilling.
Redux: Manages global state, including user authentication and product catalog.

Redux Toolkit: Simplified store setup, reducers, and actions for managing app state.
React-Redux Hooks:
useSelector: Accesses global state within any component.
useDispatch: Triggers actions to modify state, making components reactive to user interactions.
Frontend Implementation Steps
Setup React Application with Redux:

Created the React application with create-react-app.
Configured Redux with initial state and reducers for user, product, and cart management.
User Authentication Flow:

Implemented login and registration forms.
Stored the JWT token in local storage upon successful login.
Configured private routes to restrict access based on the user's authentication status.
Product Listing and Details:

Fetched products from the backend using Axios within useEffect.
Created components for displaying product information, adding to cart, and navigating between pages.
Cart Management:

Added items to the cart using Redux actions.
Displayed cart items, quantities, and total price.
Synchronized cart state across components, ensuring seamless UX when modifying cart contents.