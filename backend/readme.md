## Installation

To get started with Trustathon, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/itzpushan/Trustathon
   ```
2. Navigate to the project directory:
   ```sh
   cd Trustathon
   cd Backend
   ```
3. Install dependencies:
   ```sh
   npm install  # For Node.js projects
   ```
4. Run the backend server:
   ```sh
   nodemon index.js
   ```

## API Routes

### Authentication

- `POST /api/v1/user/signup` - Register a new user.
- `POST /api/v1/user/signin` - Authenticate and log in a user.

### Users

- `PUT /api/v1/user/` - Updating user info.
- `GET /api/v1/user/bulk` - Get all other user details.
- `PUT /api/v1/user/bulk/:filter` - filters the user based on firstName or lastName.

### Transactions

- `GET /api/v1/account/balance` - Get user balance.
- `POST /api/v1/account/transfer` - Transfer amount.
- `GET /api/v1/account/transactions/pdf` - Retrieve transaction records in pdf.
