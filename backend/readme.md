## Installation

To get started with Trustathon, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/itzpushan/Trustathon
   ```
2. Navigate to the project directory:
   ```sh
   cd Trustathon
   cd backend
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

## Protected Transaction Record PDF

Traditionally, PDFs are secured using predefined passwords, such as in Aadhar documents. However, these static passwords are more vulnerable to brute-force attacks, making them easier to crack. To enhance security, we implement an additional layer of protection using encryption. Instead of relying solely on a fixed password, we encrypt it using a public-private key mechanism, where both the bank and the user share certificates containing a public key.

The bank issues a digital certificate that includes its public key, which is securely shared with the user. Similarly, the user possesses a digital certificate containing their public key, which is shared with the bank. This mutual exchange of public keys ensures that sensitive data, including the PDF password, can be encrypted by one party and decrypted only by the intended recipient using their private key. This approach significantly reduces the risk of unauthorized access, ensuring that only authenticated users can access the transaction history while maintaining confidentiality and data integrity.
