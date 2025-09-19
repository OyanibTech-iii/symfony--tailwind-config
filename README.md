# Symfony App with Tailwind CSS

A modern Symfony 7.3 application with Tailwind CSS 4.x for styling, featuring Webpack Encore for asset management and Stimulus for interactive components.

## 🚀 Features

- **Symfony 7.3** - Latest stable version of the Symfony framework
- **Tailwind CSS 4.x** - Modern utility-first CSS framework
- **Webpack Encore** - Asset management and build tooling
- **Stimulus** - Modest JavaScript framework for HTML data attributes
- **Turbo** - Fast navigation and form submissions
- **Doctrine ORM** - Database abstraction layer
- **Twig** - Flexible templating engine

## 📋 Requirements

- PHP 8.2 or higher
- Node.js 16+ and npm
- Composer
- Symfony CLI (optional but recommended)

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd appTailwind
   ```

2. **Install PHP dependencies**
   ```bash
   composer install
   ```

3. **Install Node.js dependencies**
   ```bash
   npm install
   ```

4. **Environment setup**
   ```bash
   cp .env .env.local
   # Edit .env.local with your database configuration
   ```

5. **Database setup** (if using database)
   ```bash
   php bin/console doctrine:database:create
   php bin/console doctrine:migrations:migrate
   ```

6. **Build assets**
   ```bash
   npm run build
   # or for development with watch mode
   npm run watch
   ```

## 🏃‍♂️ Running the Application

### Development Server

Start the Symfony development server:
```bash
symfony server:start
# or
php -S localhost:8000 -t public/
```

### Asset Development

For development with automatic rebuilding:
```bash
npm run watch
```

For production build:
```bash
npm run build
```

The application will be available at `http://localhost:8000`

## 📁 Project Structure

```
├── assets/                 # Frontend assets
│   ├── app.js             # Main JavaScript entry point
│   ├── styles/
│   │   └── app.css        # Main CSS file with Tailwind
│   └── controllers/       # Stimulus controllers
├── config/                # Symfony configuration
├── public/                # Web-accessible files
│   ├── build/            # Compiled assets
│   └── index.php         # Application entry point
├── src/                   # PHP source code
│   ├── Controller/        # Controllers
│   ├── Entity/           # Doctrine entities
│   └── Repository/       # Data repositories
├── templates/             # Twig templates
│   ├── base.html.twig    # Base template
│   └── homepage/         # Page-specific templates
├── tests/                 # Test files
├── webpack.config.js     # Webpack Encore configuration
├── postcss.config.mjs    # PostCSS configuration
├── composer.json         # PHP dependencies
└── package.json          # Node.js dependencies
```

## 🎨 Styling with Tailwind CSS

This project uses Tailwind CSS 4.x with PostCSS. The main CSS file is located at `assets/styles/app.css`.

### Example Usage

```html
<div class="flex flex-row">
  <ul>
    <li class="text-red-500">Item 1</li>
    <li class="text-green-500">Item 2</li>
    <li class="text-blue-500">Item 3</li>
  </ul>
</div>
<h1 class="text-3xl font-bold text-cyan-400">
  Hello world!
</h1>
```

## 🧪 Testing

Run the test suite:
```bash
php bin/phpunit
```

## 📦 Available Scripts

### PHP Scripts
- `composer install` - Install PHP dependencies
- `php bin/console cache:clear` - Clear Symfony cache
- `php bin/console doctrine:migrations:migrate` - Run database migrations

### Node.js Scripts
- `npm run dev` - Build assets for development
- `npm run watch` - Build assets and watch for changes
- `npm run build` - Build assets for production
- `npm run dev-server` - Start development server with hot reload

## 🔧 Configuration

### Webpack Encore
The build process is configured in `webpack.config.js`. It includes:
- PostCSS loader for Tailwind CSS
- Stimulus bridge for JavaScript components
- Source maps for development
- Asset versioning for production

### PostCSS
Tailwind CSS is configured via PostCSS in `postcss.config.mjs`.

## 🚀 Deployment

1. **Build production assets**
   ```bash
   npm run build
   ```

2. **Install production dependencies**
   ```bash
   composer install --no-dev --optimize-autoloader
   ```

3. **Clear and warm up cache**
   ```bash
   php bin/console cache:clear --env=prod
   ```

4. **Deploy to your web server**

## 📚 Documentation

- [Symfony Documentation](https://symfony.com/doc/current/index.html)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Webpack Encore Documentation](https://symfony.com/doc/current/frontend.html)
- [Stimulus Documentation](https://stimulus.hotwired.dev/)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is proprietary. All rights reserved.

## 🆘 Support

If you encounter any issues or have questions, please:
1. Check the [Symfony documentation](https://symfony.com/doc/current/index.html)
2. Search existing issues
3. Create a new issue with detailed information

---

**Happy coding! 🎉**
