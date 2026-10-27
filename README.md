# New Mesa Bot

This is a fork of https://github.com/ReallyFullStack/MesanImperialBot, a bot of mines made initially for Mesa
but I made it too entrenched in an alternate scenario that won't happen. The main logic will be primarily
updated there, this repo is mainly a reskin of it.

## Get Started

First, you'll need to clone the repository and install the dependencies:

```sh
git clone https://github.com/ReallyFullStack/NewMesaBot
cd NewMesaBot
npm install
```

It has for major dependencies `discord.js`, `better-sqlite3`, `@googleapis/docs` and `@googleapis/drive`.

Then, you will have to create an SQLite3 database at `data/database.db` based on the `data/database.sql` schema:

```sh
sqlite3 data/database.db < data/database.sql
```

You will have to register both an application on the Discord Dev Portal, and an application in the Google Cloud Console, add it
the Google Docs API and Google Drive API, create a Service Account and download the key file for the Service Account. For the bot to access Google Docs
documents, you have to or make the document available to everyone with the link, or share it with the bot's Service Account e-mail.

Finally, you will have to rename [`src/config.ts.template`](./src/config.ts.template) to `config.ts` and populate it with the required information.

### Run

- To run the dev environment, use:

    ```sh
    npm run dev
    ```

- To run the production environment:

    ```sh
    npm run prod
    ```

## License

This project is licensed under the GNU Affero General Public License, version 3 or later, see [`LICENSE`](./LICENSE) for more information.
