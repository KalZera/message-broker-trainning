# Message Broker Portfolio Project

## Overview

This is a portfolio project designed to demonstrate and practice message broker concepts using modern technologies. The project serves as a practical learning exercise focusing on asynchronous communication patterns, message queuing, and distributed system architecture.

## Project Purpose

The main objective of this project is to:
- **Practice Message Broker Concepts**: Implement real-world messaging patterns using RabbitMQ
- **Learn Asynchronous Communication**: Understand publisher-subscriber patterns, message queues, and event-driven architecture
- **Apply SOLID Principles**: Demonstrate clean code practices and software design principles
- **Modern Technology Stack**: Gain hands-on experience with cutting-edge development tools

## Technology Stack

### Backend Framework
- **NestJS**: A progressive Node.js framework for building efficient and scalable server-side applications
- **TypeScript**: Strongly typed programming language that builds on JavaScript

### Database & ORM
- **PostgreSQL**: Advanced open-source relational database
- **Prisma**: Next-generation ORM for type-safe database access

### Message Broker
- **RabbitMQ**: Robust message broker that supports multiple messaging protocols

### Architecture Principles
- **SOLID Principles**: Following clean code practices for maintainable and scalable software design
  - **S**ingle Responsibility Principle
  - **O**pen/Closed Principle
  - **L**iskov Substitution Principle
  - **I**nterface Segregation Principle
  - **D**ependency Inversion Principle

## Project Structure

```
message-broker-portfolio/
├── docker-compose.yml          # Container orchestration
├── package.json               # Project dependencies
├── README.md                  # Project documentation
├── src/                       # Source code
├── prisma/                    # Database schema and migrations
└── docs/                      # Additional documentation
```

## Infrastructure Services

### PostgreSQL Database
- **Container Name**: `db`
- **Port**: `5432`
- **Database**: `messagebroker`
- **Credentials**: `postgres/postgres`

### RabbitMQ Message Broker
- **Container Name**: `rmq`
- **AMQP Port**: `5672`
- **Management UI**: `http://localhost:15672`
- **Credentials**: `admin/admin`

## Getting Started

### Prerequisites

- **Docker & Docker Compose**: For running PostgreSQL and RabbitMQ containers
- **Node.js** (v18 or higher): For running the NestJS application
- **npm or yarn**: Package manager

### Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd message-broker-portfolio
   ```

2. **Start the infrastructure services**
   ```bash
   docker-compose up -d
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Set up the database**
   ```bash
   npx prisma migrate dev
   npx prisma generate
   ```

5. **Start the development server**
   ```bash
   npm run start:dev
   ```

## Learning Objectives

### Message Broker Concepts
- **Queues**: Understanding FIFO message processing
- **Exchanges**: Learning different routing mechanisms (direct, topic, fanout)
- **Publishers & Consumers**: Implementing producer-consumer patterns
- **Dead Letter Queues**: Handling failed message processing
- **Message Acknowledgments**: Ensuring reliable message delivery

### Software Architecture
- **Event-Driven Architecture**: Building loosely coupled systems
- **Microservices Communication**: Inter-service messaging patterns
- **Error Handling**: Implementing robust error recovery mechanisms
- **Performance Optimization**: Message batching and connection pooling

### SOLID Principles Application
- **Dependency Injection**: Using NestJS's IoC container
- **Interface Segregation**: Creating focused, single-purpose interfaces
- **Open/Closed Principle**: Extending functionality without modifying existing code
- **Single Responsibility**: Each class/module has one reason to change

## Features to Implement

- [ ] **Basic Message Publishing**: Send messages to queues
- [ ] **Message Consumption**: Process messages from queues
- [ ] **Event-Driven Communication**: Implement publisher-subscriber patterns
- [ ] **Database Integration**: Persist message metadata using Prisma
- [ ] **Error Handling**: Implement retry mechanisms and dead letter queues
- [ ] **Message Routing**: Different exchange types and routing patterns
- [ ] **Monitoring**: Health checks and message tracking
- [ ] **Testing**: Unit and integration tests for messaging flows

## Development Guidelines

### Code Style
- Follow TypeScript best practices
- Use ESLint and Prettier for code formatting
- Implement comprehensive error handling
- Write meaningful tests

### Architecture
- Apply SOLID principles consistently
- Use dependency injection for loose coupling
- Implement proper abstraction layers
- Follow NestJS conventions and best practices

## Project Setup

```bash
# Install dependencies
$ npm install

# Start infrastructure services
$ docker-compose up -d

# Set up database
$ npx prisma migrate dev
$ npx prisma generate
```

## Compile and Run the Project

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Run Tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Documentation

- **API Documentation**: Auto-generated with Swagger/OpenAPI
- **Database Schema**: Documented with Prisma schema comments
- **Message Flows**: Documented messaging patterns and use cases

## Contributing

This is a learning project, but contributions and suggestions are welcome:
1. Fork the repository
2. Create a feature branch
3. Follow the coding standards
4. Add tests for new features
5. Submit a pull request

## Resources

- [NestJS Documentation](https://docs.nestjs.com/)
- [RabbitMQ Tutorials](https://www.rabbitmq.com/tutorials.html)
- [Prisma Documentation](https://www.prisma.io/docs/)
- [SOLID Principles](https://en.wikipedia.org/wiki/SOLID)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
