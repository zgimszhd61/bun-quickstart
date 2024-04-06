Here is a quickstart guide for getting started with Bun:

## Installation

First, you need to install Bun. You can install the latest version from the official website:

```bash
curl -fsSL https://bun.sh/install | bash
```

This will install the `bun` executable in your system.

## Creating a New Project

To create a new Bun project, run:

```bash
bun init
```

This will initialize a new project with some default files like `index.ts`, `package.json`, `tsconfig.json` etc. Just press enter to accept the defaults.

## Running a Server

Open `index.ts` and paste the following code to create a simple HTTP server:

```typescript
const server = Bun.serve({
  port: 3000,
  fetch(req) {
    return new Response("Hello, Bun!");
  }
});

console.log(`Listening on http://localhost:${server.port}`);
```

Now run the server with:

```bash
bun run index.ts
```

This will start the server at `http://localhost:3000`. Visit that URL to see "Hello, Bun!" rendered in the browser. [1]

## Installing Dependencies

You can install npm packages just like you would with Node.js:

```bash
bun add figlet
```

This installs the `figlet` package which renders ASCII art text.

Update `index.ts` to use `figlet`:

```typescript
import figlet from "figlet";

const server = Bun.serve({
  port: 3000, 
  fetch(req) {
    const body = figlet.textSync("Bun!");
    return new Response(body);
  }
});

console.log(`Listening on http://localhost:${server.port}`);
```

Now when you run `bun run index.ts` and visit `localhost:3000`, you'll see the "Bun!" text rendered as ASCII art. [1]

This is just a basic introduction to get you started with Bun. Refer to the official docs at https://bun.sh/docs for more details on using Bun for your JavaScript/TypeScript projects.

Citations:
[1] https://bun.sh/docs/quickstart
[2] https://bun.sh
[3] https://codedamn.com/news/backend/bun-js-tutorial-2022
[4] https://github.com/oven-sh/bun
[5] https://www.youtube.com/watch?v=eTB0UCDnMQo
[6] https://github.com/oven-sh/awesome-bun
[7] https://blog.logrocket.com/getting-started-bun-react/
[8] https://bun.sh/guides
[9] https://www.freecodecamp.org/news/a-quick-look-at-bun-js/
[10] https://dev.to/fritzblue/creating-a-modern-web-application-with-bun-astro-typescript-and-htmx-2023-quickstart-tutorial-4k0d
[11] https://www.youtube.com/watch?v=4oZiNLiOUuM
[12] https://www.youtube.com/watch?v=JjXqsviSGvY
