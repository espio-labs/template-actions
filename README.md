# GitHub Actions Templates Repository

Welcome to our GitHub Actions Templates repository! This is a centralized hub for GitHub Actions workflows and actions, designed to streamline and automate your CI/CD processes across multiple projects. Our goal is to ensure consistency, efficiency, and adherence to best practices throughout your development lifecycle by providing reusable workflow templates.

## 📁 Repository Contents

This repository contains a variety of GitHub Actions templates, including but not limited to:

- **Docker Build and Push**: Automates the process of building Docker images and pushing them to a Docker registry.
- **Build Template**: A generic template for building your projects.
- **Push Template**: Simplifies the process of pushing built artifacts to various destinations.
- _More templates will be added as we expand our collection._

## 🚀 How to Use the Templates

### Workflow Templates

1. **Copy the desired template**: Find the workflow template you want to use (e.g., `.github/workflows/build.yaml`) and copy its contents.
2. **Create a new workflow in your repository**: In your project's repository, navigate to the `.github/workflows/` directory. Create a new `.yaml` file and paste the copied template content.
3. **Customize the workflow**: Modify the workflow's parameters, such as `runs-on`, triggers (`on`), and steps according to the needs of your project.

### Action Templates

1. **Reference the action in your workflow**: In the workflow file of your project, use the `uses` directive to reference the action template stored in this repository. For example:
   ```yaml
   steps:
     - uses: actions/checkout@v2
     
     - uses: your-org/github-actions-templates/.github/actions/docker-build-action@main
       with:
         image-name: 'your-image-name'
         image-version: 'latest'
         registry-url: 'your.harbor.domain'
         dockerfile-path: './path/to/Dockerfile'
