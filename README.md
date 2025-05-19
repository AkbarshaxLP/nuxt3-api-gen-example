Generating api methods and types
## ⚠️ cd to dir: api-gen/

## 🚀 API Client Generator

This tool generates TypeScript types and API methods based on a Swagger/OpenAPI schema.

### 📋 Steps to Generate

1. **Configure `swaggerUrl`**  
   - Open your Swagger UI in a browser.  
   - Press `F12` to open Developer Tools, go to the **Network** tab, and refresh the page.  
   - Look for a `.json` request (usually the Swagger schema), right-click it, and copy its URL.  
   - Paste the URL into the `swaggerUrl` field inside `config.json`.

2. **Run the generator**  
   In your terminal, run one of the following commands:

   ```bash
   npm run api-gen
   # or
   node generate.cjs


## 📦 Output

After running the command, a directory named `api` will be created in the same location as the script (if it doesn't already exist).

Inside the `api` folder, two files will be generated:

- `apiScheme.types.ts` — TypeScript types generated from the Swagger schema.
- `apiScheme.ts` — Grouped API methods based on tags defined in the Swagger spec.

These files are ready to use with the `useApiService` composable in your project.


## 🔧 Usage Example

```vue
<script lang="ts" setup>
const { data, error, status } = apiScheme.users.getUserList();
// ...
</script>




## Nuxt Minimal Starter

Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
