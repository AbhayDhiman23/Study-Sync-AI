# Study Sync AI 🚀

An intelligent study companion application built with modern web technologies to help students organize, track, and optimize their learning experience using AI.

## 🌟 Features

- **AI-Powered Study Assistant**: Intelligent recommendations and study planning
- **User Authentication**: Secure login system with NextAuth.js
- **Real-time Data Management**: Efficient data handling with tRPC and Prisma
- **Responsive Design**: Beautiful UI with Tailwind CSS
- **Type Safety**: Full TypeScript support throughout the application
- **Modern Architecture**: Built with Next.js 15 and React 19

## 🛠️ Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript
- **Styling**: Tailwind CSS 4.0
- **Backend**: tRPC, Prisma ORM
- **Authentication**: NextAuth.js v5
- **Database**: PostgreSQL (configurable)
- **State Management**: TanStack Query (React Query)
- **Development**: ESLint, Prettier, TypeScript ESLint

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** (v10 or higher)
- **Docker** (for database)
- **Git**

For Windows users:
- **WSL** (Windows Subsystem for Linux) - [Installation Guide](https://learn.microsoft.com/en-us/windows/wsl/install)
- **Docker Desktop** or **Podman Desktop**

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/AbhayDhiman23/Study-Sync-AI.git
cd Study-Sync-AI/study-sync-ai
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Setup

Create a `.env` file in the root directory and configure your environment variables:

```env
# Database
DATABASE_URL="your-database-connection-string"

# NextAuth.js
NEXTAUTH_SECRET="your-nextauth-secret"
NEXTAUTH_URL="http://localhost:3000"

# OAuth Providers (configure as needed)
# GOOGLE_CLIENT_ID="your-google-client-id"
# GOOGLE_CLIENT_SECRET="your-google-client-secret"
```

### 4. Database Setup

#### Option A: Using Docker (Recommended)

For Windows users, open WSL first:
```bash
wsl
```

Then run the database setup script:
```bash
./start-database.sh
```

#### Option B: Using Your Own Database

If you have your own PostgreSQL database, update the `DATABASE_URL` in your `.env` file.

### 5. Database Migration

Generate and run the database migrations:

```bash
npm run db:generate
```

### 6. Start Development Server

```bash
npm run dev
```

The application will be available at [http://localhost:3000](http://localhost:3000)

## 📝 Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server with Turbo |
| `npm run build` | Build the application for production |
| `npm run start` | Start the production server |
| `npm run preview` | Build and start production server |
| `npm run lint` | Run ESLint |
| `npm run lint:fix` | Fix ESLint issues automatically |
| `npm run typecheck` | Run TypeScript type checking |
| `npm run format:check` | Check code formatting with Prettier |
| `npm run format:write` | Format code with Prettier |
| `npm run db:generate` | Generate Prisma client and run migrations |
| `npm run db:migrate` | Deploy migrations to production |
| `npm run db:push` | Push schema changes to database |
| `npm run db:studio` | Open Prisma Studio |

## 🏗️ Project Structure

```
study-sync-ai/
├── src/                    # Source code
├── public/                 # Static assets
├── prisma/                 # Database schema and migrations
├── .env                    # Environment variables
├── package.json           # Dependencies and scripts
├── tsconfig.json          # TypeScript configuration
├── tailwind.config.js     # Tailwind CSS configuration
├── next.config.js         # Next.js configuration
├── eslint.config.js       # ESLint configuration
├── prettier.config.js     # Prettier configuration
└── start-database.sh      # Database startup script
```

## 🔧 Development Workflow

### Code Quality

This project uses several tools to maintain code quality:

- **ESLint**: For identifying and fixing code issues
- **Prettier**: For consistent code formatting
- **TypeScript**: For type safety
- **Husky**: For pre-commit hooks (if configured)

### Database Development

- Use `npm run db:studio` to open Prisma Studio for database management
- Run `npm run db:generate` after making schema changes
- Use `npm run db:push` for development database updates

### Type Safety

- Run `npm run typecheck` to verify TypeScript compilation
- The project is configured with strict TypeScript settings
- All API routes are type-safe with tRPC

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

### Environment Variables for Production

Ensure all environment variables are properly set in your production environment:

- `DATABASE_URL`: Production database connection string
- `NEXTAUTH_SECRET`: Secure random string for NextAuth.js
- `NEXTAUTH_URL`: Your production domain

### Deployment Platforms

This application can be deployed on:

- **Vercel** (recommended for Next.js)
- **Netlify**
- **Railway**
- **Heroku**
- **AWS**
- **Google Cloud Platform**

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow the existing code style
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Run `npm run check` before submitting PRs

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Troubleshooting

### Common Issues

**Database Connection Issues**
- Ensure Docker is running
- Check if the database container is started
- Verify DATABASE_URL in .env file

**Build Errors**
- Run `npm run typecheck` to identify TypeScript issues
- Check for missing environment variables
- Clear `.next` folder and rebuild

**Development Server Issues**
- Clear npm cache: `npm cache clean --force`
- Delete `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Check if port 3000 is available

### Getting Help

- Check the [Issues](https://github.com/AbhayDhiman23/Study-Sync-AI/issues) page
- Review the documentation for each technology in the stack
- Join our community discussions

## 📞 Support

For support and questions:

- **GitHub Issues**: [Create an issue](https://github.com/AbhayDhiman23/Study-Sync-AI/issues)
- **Email**: Contact the maintainer
- **Documentation**: Check the inline code documentation

---

**Built with ❤️ using the T3 Stack**

*This project was bootstrapped with `create-t3-app`.*
