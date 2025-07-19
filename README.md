# Formlabs API Mock Server with Swagger UI

This project provides a mock implementation of the Formlabs Web API with a Swagger UI interface for testing and exploration.

## Features

- Full Swagger UI interface for API documentation
- Working "Try it out" buttons for all endpoints
- Realistic mock responses for all API operations
- OAuth authentication simulation
- Paginated responses where applicable
- CORS enabled for cross-origin requests

## Getting Started

### Prerequisites

- Node.js installed on your system
- npm (comes with Node.js)

### Quick Start

1. Clone the repository:
```bash
git clone https://github.com/kradriany/mcp1.git
cd mcp1
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm start
```

4. Open your browser to http://localhost:4000/api-docs

That's it! The Swagger UI is ready to use.

### Running the Server

Start the mock API server:
```bash
npm start
```

The server will start on http://localhost:4000

## Using the API

### Swagger UI

Visit http://localhost:4000/api-docs to access the Swagger UI interface.

Alternative access: http://127.0.0.1:4000/api-docs

### Authentication

To test authenticated endpoints:

1. Click on the "Authentication" section in Swagger UI
2. Use the "Request an access token" endpoint with any client_id and client_secret
3. Copy the returned access_token
4. Click the "Authorize" button at the top of Swagger UI
5. Enter: `Bearer YOUR_ACCESS_TOKEN`
6. Click "Authorize"

Now you can test all authenticated endpoints!

### Available Endpoints

- **Authentication**: OAuth token management
- **Printers**: List and view printer details
- **Prints**: List print history with filtering
- **Groups**: Manage printer groups
- **Tanks**: List resin tanks
- **Cartridges**: List resin cartridges
- **Events**: List system events

### Mock Data

The server provides realistic mock data for all endpoints including:
- 2 mock printers (one idle, one printing)
- Print history with various statuses
- Printer groups with members
- Tank and cartridge information
- System events

## API Features

- Pagination support on list endpoints
- Query parameter filtering
- Realistic response data structures
- Proper HTTP status codes
- Error responses for invalid requests

## Development

To modify the mock responses, edit the `server.js` file. The mock data is defined in the `mockHandlers` object and individual route handlers.

## Notes

This is a mock server for development and testing purposes. It simulates the Formlabs API but does not connect to actual printers or the Formlabs cloud service.