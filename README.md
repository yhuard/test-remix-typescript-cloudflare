# Welcome to Remix!

- [Remix Docs](https://remix.run/docs)

## Development

You will be running two processes during development:

- The Miniflare server (miniflare is a local environment for Cloudflare Workers)
- The Remix development server

```sh
# in one tab, start the remix dev server
$ npm run dev

# in another, start the miniflare server
$ npm start
```

Open up [http://127.0.0.1:8787](http://127.0.0.1:8787) and you should be ready to go!

If you'd rather run everything in a single tab, you can look at [concurrently](https://npm.im/concurrently) or similar tools to run both processes in one tab.

## Deployment

Use [wrangler](https://developers.cloudflare.com/workers/cli-wrangler) to build and deploy your application to Cloudflare Workers. If you don't have it yet, follow [the installation guide](https://developers.cloudflare.com/workers/cli-wrangler/install-update) to get it setup. Be sure to [authenticate the CLI](https://developers.cloudflare.com/workers/cli-wrangler/authentication) as well.

If you don't already have an account, then [create a cloudflare account here](https://dash.cloudflare.com/sign-up) and after verifying your email address with Cloudflare, go to your dashboard and set up your free custom Cloudflare Workers subdomain.

Once that's done, you should be able to deploy your app:

```sh
npm run deploy
```

## I learned...

- how to set up Remix with Cloudflare Workers
- how to create a GitHub action to automatically deploy to CF Workers on every push
- Cloudflare Workers don't run in a Node.js environment, meaning we don't have access to Node.js native modules (like `fs`). For data persistence, something like Cloudflare Workers KV could be used https://www.cloudflare.com/en-gb/products/workers-kv/

## Personal notes

- I had to configure SourceTree to have "workflow" scope -> created a new GH personal access token (https://community.atlassian.com/t5/Bitbucket-questions/I-can-t-connect-to-Github-from-Sourcetree/qaq-p/30851#U1350882)
