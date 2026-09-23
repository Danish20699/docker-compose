# Contributing to Docker Compose Labs

Thank you for your interest in contributing to the **Docker Compose Labs** repository!

## 🛠️ Development & Submission Workflow

1. **Fork the Repository**:
   Click the **Fork** button at the top right of this repository.

2. **Clone your Fork**:
   ```bash
   git clone https://github.com/<your-username>/docker-compose.git
   cd docker-compose
   ```

3. **Create a Feature Branch**:
   ```bash
   git checkout -b feature/lab-enhancement
   ```

4. **Follow Standards**:
   - Validate YAML syntax: all `docker-compose.yml` files must pass `docker compose config`.
   - Document any new labs with step-by-step markdown, architectural ASCII diagrams, and verification commands.
   - Maintain clear commit messages following Conventional Commits (`feat: ...`, `fix: ...`, `docs: ...`).

5. **Commit & Push**:
   ```bash
   git add .
   git commit -m "docs: improve lab documentation"
   git push origin feature/lab-enhancement
   ```

6. **Submit a Pull Request**:
   Open a Pull Request against the `main` branch with a clear description of your changes.
