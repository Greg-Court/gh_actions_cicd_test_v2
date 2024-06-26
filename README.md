# Node.js React Application CI/CD

This repository houses a React application created with Vite, focusing on demonstrating a complete Continuous Integration (CI) and Continuous Deployment (CD) pipeline using GitHub Actions. The application is automatically built and deployed to an Azure Web App whenever changes are pushed to the main branch.

## Project Structure

The project's directory is organized as follows:

- `.github/workflows`: Contains the workflow files for GitHub Actions.
  - `ci.yml`: Defines the CI workflow that builds the application and runs tests.
  - `cd.yml`: Handles the CD workflow, deploying the application to Azure.
- `public`: Public assets like the HTML template.
- `src`: Source files of the React application.
- `vite.config.js`: Configuration file for Vite.

Other key files include:

- `.eslintrc.js`: ESLint configuration for linting the project.
- `package.json` and `package-lock.json`: Manage project dependencies and lock their versions.
- `README.md`: Documentation about the project.

## Key Features

- **Continuous Integration**: Automatically builds and tests the project on every push to `main` or pull request, ensuring that changes do not break the build or functionality.
- **Continuous Deployment**: Deploys the latest version of the application to Azure Web App automatically, using the latest capabilities of GitHub Actions to manage artifacts across workflows.
- **GitHub Actions v4**: This project uses the enhanced features of GitHub Actions v4 to pass build artifacts between different workflows. Can't believe this wasn't possible before v4!

## Deployment

The project was deployed to an Azure Web App (now no longer running due to cost). This setup demonstrates an end-to-end automated pipeline from code push to production deployment.

## Getting Started

To get a local copy up and running, follow these simple steps:

1. Clone the repository.
2. Install dependencies:

```
npm install
```

3. Run the application locally

```
npm run dev
```

You can then try to deploy this via the available CI/CD pipelines to your own Azure App Service. Hands on practice is the best way to learn. Detailed instructions on continuous deployment for Azure App Services can be found here: https://learn.microsoft.com/en-us/azure/app-service/deploy-continuous-deployment?tabs=github%2Cgithubactions

In your web app configuration settings, make sure you specify the following startup command:

```
npx serve -s /home/site/wwwroot -l 8080
```

## Contributing

Contributions are what make the open source community such a powerful platform for learning, inspiring, and creation. Any contributions you make are **greatly appreciated**.

To contribute:

1. Fork the project.
2. Create your Feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.
