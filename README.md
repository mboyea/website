www.mboyea.com
===
A portfolio website to host articles, apps, and games built by Matthew Boyea.
---
This website is built with [SvelteKit], [Typescript], & [Sass] to compile a html/css/js application delivered by a [Node.js] server. [PNPM] manages all dependency packages. [Docker] is used to compile the app into a minified [Ubuntu] environment. [Fly.io] hosts the Docker Image to serve the completed website.

### Fork & Clone This Repository
* [Fork this repository].
* [Clone that repository] to your computer.

### Install Dependencies
* Fork & Clone This Repository.
* [Install NPM].
* [Install PNPM].
* [Install flyctl] for deployments.
* [Install Git Bash] for deployment scripts & Github commits.
* [Install psql] for remote SQL deployment.
* Ensure each of the above command line tools are accessible by PATH.
* Open a terminal in the root folder.
* Run `pnpm i` in the terminal to install all app dependencies.

From here, you can use & edit the app locally. You can run the following scripts in the terminal to do things.

### Run Scripts
To run a script, type `pnpm run <script-name>` into a terminal within the root folder.

| script-name | description |
|:----------- |:----------- |
| `dev` | create a local hot-reloading server at [localhost:5173](http://localhost:5173) for development purposes |
| `preview` | build app using .env.development, create a local server at [localhost:4173](http://localhost:4173) |
| `deploy` | update app dependencies, build app, deploy database, deploy secrets, deploy server |
| `deploy:database` | update postgres users, databases, tables, procedures, etc. |
| `deploy:secrets` | set flyctl secrets from .env file |
| `deploy:server` | deploy build folder to flyctl |
| `check` | evaluate Svelte syntax |
| `check:watch` | re-evaluate Svelte syntax when files are updated |

### Create Secrets
Some features of this app require secret database credentials. These secrets cannot be shared in public.
* Obtain the secrets.
* Create a file named `.env` in the root directory.
* Copy the secrets into the `.env` file.
* Repeat for file named `.env.development`.

### Deploy
* Install Dependencies.
* Create Secrets.
* Open a terminal in the root folder.
* Run `pnpm run deploy`.
* If postgres access is denied: check .env password; check .env host; check port 5432 is free (use `netstat -ano | findstr :5432`)

### Contribute
Unfortunately, this project doesn't support community contributions right now.

[SvelteKit]: https://kit.svelte.dev/docs/introduction
[Typescript]: https://www.typescriptlang.org/why-create-typescript
[Sass]: https://sass-lang.com/guide
[Node.js]: https://nodejs.org/en/docs/guides/getting-started-guide
[Docker]: https://docs.docker.com/get-started/overview/
[Ubuntu]: https://ubuntu.com/about
[PNPM]: https://pnpm.io/motivation
[Install NPM]: https://nodejs.org/en/download
[Install PNPM]: https://pnpm.io/installation
[Install flyctl]: https://fly.io/docs/hands-on/install-flyctl/
[Install Git Bash]: https://git-scm.com/downloads
[Install psql]: https://www.timescale.com/blog/how-to-install-psql-on-mac-ubuntu-debian-windows/
[Fly.io]: https://fly.io/docs/
[Fork this repository]: https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository
[Clone that repository]: https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository#cloning-a-repository
