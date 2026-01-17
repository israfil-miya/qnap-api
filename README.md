# QNAP API

A NestJS-based API service for integrating with QNAP QTS File Station API (v5.x).

## Features

- Full QNAP QTS File Station API v5+ integration
- Session management with MongoDB persistence
- Auto re-authentication on session expiry
- File operations: list, create folder, rename, move, copy, delete

## Installation

```bash
pnpm install
```

## Configuration

Copy `.env.example` to `.env` and update the values:

```bash
cp .env.example .env
```

### Environment Variables

| Variable        | Description               | Default |
| --------------- | ------------------------- | ------- |
| `QNAP_HOST`     | QNAP NAS hostname or IP   | -       |
| `QNAP_PORT`     | QNAP NAS port             | 8080    |
| `QNAP_USERNAME` | QNAP user account         | -       |
| `QNAP_PASSWORD` | QNAP user password        | -       |
| `QNAP_HTTPS`    | Use HTTPS connection      | false   |
| `MONGODB_URI`   | MongoDB connection string | -       |
| `PORT`          | Server port               | 3000    |

## Running the app

```bash
# production mode
pnpm run start

# development
pnpm run dev

# debug mode
pnpm run debug
```

## API Endpoints

| Method | Endpoint       | Description             |
| ------ | -------------- | ----------------------- |
| GET    | `/qnap/list`   | List folder contents    |
| POST   | `/qnap/folder` | Create a new folder     |
| POST   | `/qnap/rename` | Rename a file or folder |
| POST   | `/qnap/move`   | Move files/folders      |
| POST   | `/qnap/copy`   | Copy files/folders      |
| DELETE | `/qnap/delete` | Delete files/folders    |

## Documentation

See [src/qnap/README.md](src/qnap/README.md) for detailed API integration documentation.
