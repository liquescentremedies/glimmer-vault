---
source_url: https://github.com/Crosstalk-Solutions/project-nomad
saved_date: 2026-03-23T07:55:56.809Z
fabric_id: 572a243a-6c32-4b78-8b43-78cd31c9678c
tags:
  - github
  - offline-first
  - AI
  - knowledge-base
  - self-hosted
---

Project N.O.M.A.D. is a self-contained, offline-first knowledge and education server packed with critical tools, knowledge, and AI to keep you informed and empowered—anytime, anywhere.

Project N.O.M.A.D. can be installed on any Debian-based operating system (we recommend Ubuntu). Installation is completely terminal-based, and all tools and resources are designed to be accessed through the browser, so there's no need for a desktop environment if you'd rather setup N.O.M.A.D. as a "server" and access it through other clients.

*Note: sudo/root privileges are required to run the install script*

`sudo apt-get update && sudo apt-get install -y curl && curl -fsSL https://raw.githubusercontent.com/Crosstalk-Solutions/project-nomad/refs/heads/main/install/install_nomad.sh -o install_nomad.sh && sudo bash install_nomad.sh`

Project N.O.M.A.D. is now installed on your device! Open a browser and navigate to `http://localhost:8080`

(or `http://DEVICE_IP:8080`

) to start exploring!

For more control over the installation process, copy and paste the Docker Compose template into a `docker-compose.yml`

file and customize it to your liking (be sure to replace any placeholders with your actual values). Then, run `docker compose up -d`

to start the Command Center and its dependencies. Note: this method is recommended for advanced users only, as it requires familiarity with Docker and manual configuration before starting.

N.O.M.A.D. is a management UI ("Command Center") and API that orchestrates a collection of containerized tools and resources via Docker. It handles installation, configuration, and updates for everything — so you don't have to.

**Built-in capabilities include:**

**AI Chat with Knowledge Base**— local AI chat powered by Ollama, with document upload and semantic search (RAG via Qdrant)**Information Library**— offline Wikipedia, medical references, ebooks, and more via Kiwix**Education Platform**— Khan Academy courses with progress tracking via Kolibri**Offline Maps**— downloadable regional maps via ProtoMaps**Data Tools**— encryption, encoding, and analysis via CyberChef**Notes**— local note-taking via FlatNotes**System Benchmark**— hardware scoring with a community leaderboard**Easy Setup Wizard**— guided first-time configuration with curated content collections

N.O.M.A.D. also includes built-in tools like a Wikipedia content selector, ZIM library manager, and content explorer.

While many similar offline survival computers are designed to be run on bare-minimum, lightweight hardware, Project N.O.M.A.D. is quite the opposite. To install and run the available AI tools, we highly encourage the use of a beefy, GPU-backed device to make the most of your install.

At it's core, however, N.O.M.A.D. is still very lightweight. For a barebones installation of the management application itself, the following minimal specs are required:

*Note: Project N.O.M.A.D. is not sponsored by any hardware manufacturer and is designed to be as hardware-agnostic as possible. The harware listed below is for example/comparison use only*

- Processor: 2 GHz dual-core processor or better
- RAM: 4GB system memory
- Storage: At least 5 GB free disk space
- OS: Debian-based (Ubuntu recommended)
- Stable internet connection (required during install only)

To run LLM's and other included AI tools:

- Processor: AMD Ryzen 7 or Intel Core i7 or better
- RAM: 32 GB system memory
- Graphics: NVIDIA RTX 3060 or AMD equivalent or better (more VRAM = run larger models)
- Storage: At least 250 GB free disk space (preferably on SSD)
- OS: Debian-based (Ubuntu recommended)
- Stable internet connection (required during install only)

**For detailed build recommendations at three price points ($150–$1,000+), see the Hardware Guide.**

Again, Project N.O.M.A.D. itself is quite lightweight - it's the tools and resources you choose to install with N.O.M.A.D. that will determine the specs required for your unique deployment

Project N.O.M.A.D. is designed for offline usage. An internet connection is only required during the initial installation (to download dependencies) and if you (the user) decide to download additional tools and resources at a later time. Otherwise, N.O.M.A.D. does not require an internet connection and has ZERO built-in telemetry.

To test internet connectivity, N.O.M.A.D. attempts to make a request to Cloudflare's utility endpoint, `https://1.1.1.1/cdn-cgi/trace`

and checks for a successful response.

By design, Project N.O.M.A.D. is intended to be open and available without hurdles - it includes no authentication. If you decide to connect your device to a local network after install (e.g. for allowing other devices to access it's resources), you can block/open ports to control which services are exposed.

**Will authentication be added in the future?** Maybe. It's not currently a priority, but if there's enough demand for it, we may consider building in an optional authentication layer in a future release to support uses cases where multiple users need access to the same instance but with different permission levels (e.g. family use with parental controls, classroom use with teacher/admin accounts, etc.). For now, we recommend using network-level controls to manage access if you're planning to expose your N.O.M.A.D. instance to other devices on a local network. N.O.M.A.D. is not designed to be exposed directly to the internet, and we strongly advise against doing so unless you really know what you're doing, have taken appropriate security measures, and understand the risks involved.

Contributions are welcome and appreciated! Please read this section fully to understand how to contribute to the project.

**Open an issue first**: Before starting work on a new feature or bug fix, please open an issue to discuss your proposed changes. This helps ensure that your contribution aligns with the project's goals and avoids duplicate work. Title the issue clearly and provide a detailed description of the problem or feature you want to work on.**Fork the repository**: Click the "Fork" button at the top right of the repository page to create a copy of the project under your GitHub account.**Create a new branch**: In your forked repository, create a new branch for your work. Use a descriptive name for the branch that reflects the purpose of your changes (e.g.,`fix/issue-123`

or`feature/add-new-tool`

).**Make your changes**: Implement your changes in the new branch. Follow the existing code style and conventions used in the project. Be sure to test your changes locally to ensure they work as expected.**Add Release Notes**: If your changes include new features, bug fixes, or improvements, please see the "Release Notes" section below to properly document your contribution for the next release.**Conventional Commits**: When committing your changes, please use conventional commit messages to provide clear and consistent commit history. The format is`<type>(<scope>): <description>`

, where:`type`

is the type of change (e.g.,`feat`

for new features,`fix`

for bug fixes,`docs`

for documentation changes, etc.)`scope`

is an optional area of the codebase that your change affects (e.g.,`api`

,`ui`

,`docs`

, etc.)`description`

is a brief summary of the change

**Submit a pull request**: Once your changes are ready, submit a pull request to the main repository. Provide a clear description of your changes and reference any related issues. The project maintainers will review your pull request and may provide feedback or request changes before it can be merged.**Be responsive to feedback**: If the maintainers request changes or provide feedback on your pull request, please respond in a timely manner. Stale pull requests may be closed if there is no activity for an extended period.**Follow the project's code of conduct**: Please adhere to the project's code of conduct when interacting with maintainers and other contributors. Be respectful and considerate in your communications.**No guarantee of acceptance**: The project is community-driven, and all contributions are appreciated, but acceptance is not guaranteed. The maintainers will evaluate each contribution based on its quality, relevance, and alignment with the project's goals.**Thank you for contributing to Project N.O.M.A.D.!**Your efforts help make this project better for everyone.

This project uses semantic versioning. The version is managed in the root `package.json`

and automatically updated by semantic-release. For simplicity's sake, the "project-nomad" image
uses the same version defined there instead of the version in `admin/package.json`

(stays at 0.0.0), as it's the only published image derived from the code.

Human-readable release notes live in `admin/docs/release-notes.md`

and are displayed in the Command Center's built-in documentation.

When working on changes, add a summary to the `## Unreleased`

section at the top of that file under the appropriate heading:

**Features**— new user-facing capabilities**Bug Fixes**— corrections to existing behavior**Improvements**— enhancements, refactors, docs, or dependency updates

Use the format `- **Area**: Description`

to stay consistent with existing entries. When a release is triggered, CI automatically stamps the version and date, commits the update, and pushes the content to the GitHub release.

**Website:**www.projectnomad.us - Learn more about the project**Discord:**Join the Community - Get help, share your builds, and connect with other NOMAD users**Benchmark Leaderboard:**benchmark.projectnomad.us - See how your hardware stacks up against other NOMAD builds

Project N.O.M.A.D. is licensed under the Apache License 2.0.

Once installed, Project N.O.M.A.D. has a few helper scripts should you ever need to troubleshoot issues or perform maintenance that can't be done through the Command Center. All of these scripts are found in Project N.O.M.A.D.'s install directory, `/opt/project-nomad`


`sudo bash /opt/project-nomad/start_nomad.sh`

`sudo bash /opt/project-nomad/stop_nomad.sh`

###### Update Script - Attempts to pull the latest images for the Command Center and its dependencies (i.e. mysql) and recreate the containers. Note: this *only* updates the Command Center containers. It does not update the installable application containers - that should be done through the Command Center UI

`sudo bash /opt/project-nomad/update_nomad.sh`

###### Uninstall Script - Need to start fresh? Use the uninstall script to make your life easy. Note: this cannot be undone!

`curl -fsSL https://raw.githubusercontent.com/Crosstalk-Solutions/project-nomad/refs/heads/main/install/uninstall_nomad.sh -o uninstall_nomad.sh && sudo bash uninstall_nomad.sh`
