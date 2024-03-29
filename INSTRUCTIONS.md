

# Environment Setup
`npx create-next-app@latest antonio-notion-clone`

```
√ Would you like to use TypeScript? Yes
√ Would you like to use ESLint? Yes
√ Would you like to use Tailwind CSS? Yes
√ Would you like to use `src/` directory? No
√ Would you like to use App Router? (recommended) Yes
√ Would you like to customize the default import alias (@/\*)? No
```
`cd antonio-notion-clone`

`npx shadcn-ui@latest init`
```
√ Would you like to use TypeScript (recommended)? ... yes
√ Which style would you like to use? » Default
√ Which color would you like to use as base color? » Neutral
√ Where is your global CSS file? ... app/globals.css
√ Would you like to use CSS variables for colors? ... yes
√ Where is your tailwind.config.js located? ... tailwind.config.js
√ Configure the import alias for components: ... @/components
√ Configure the import alias for utils: ... @/lib/utils
√ Are you using React Server Components? ... yes
√ Write configuration to components.json. Proceed? ... yes
```
`npm run`

`npx shadcn-ui@latest add -y button`

# Folders setup
```
VSC Extension
Trunk Check
Id: trunk.io
Description: One linter to rule them all
Version: 3.9.0
Publisher: Trunk
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=Trunk.io
```
Powershell:
`powershell -ExecutionPolicy ByPass -Command 'c:\Users\(Username)\.cache\trunk\launcher\trunk.ps1' init --vscode`

# Landing page

Use command if cache issue in "(marketing)" - `rm -rf .next`

`npx shadcn-ui@latest add -y dropdown-menu`

`npm i next-themes`

# Authentication & Database

www.convex.dev - login
https://docs.convex.dev/quickstart/nextjs

`npm install convex`

`npx convex dev`

```
? Device name: DESKTOP-749U3IJ
Visit https://auth.convex.dev/activate?user_code=XXXX-YYYY to finish logging in.
You should see the following code which expires in 15 minutes: XXXX-YYYY  
? Open the browser? Yes
✔ Saved credentials to C:\Users\(Username)\.convex\config.json
? Project name: antonio-notion-clone
✔ Created project antonio-notion-clone-0aa9e, manage it at https://dashboard.convex.dev/t/stephyswe/antonio-notion-clone-0aa9e
```

- convex - clerk guide @ https://docs.convex.dev/auth/clerk

* https://dashboard.clerk.com/sign-up - login - create: "antonio-notion-clone" - disable "email, google" - enable "github" - copy two envs keys to .env.local
* jwt templates - new template - convex - copy issuer url - apply changes
* create convex/auth.config.js
  """
  export default {
  providers: [
  {
  domain: "https://your-issuer-url.clerk.accounts.dev/", // replace with issuer url
  applicationID: "convex",
  },
  ]
  };
  """

`npx convex dev`

`npm install @clerk/clerk-react`

components/provider/convex-provider.tsx - copy from https://github.com/AntonioErdeljac/notion-clone-tutorial/blob/master/components/providers/convex-provider.tsx

`npm run dev`

# Sidebar

`npm i usehooks-ts tailwindcss-animate`

# User Settings

```
npx shadcn-ui@latest add -y avatar
npx shadcn-ui@latest add -y dropdown-menu
```

# Schema & API - real-time data fetch

```
npm i sonner
npm run dev
npx convex dev
```

- add schema.ts before
https://www.convex.dev/ - login - new schema visible "documents" - show schema

- add documents.ts before
https://www.convex.dev/ - login - Functions - documents (get/create)

- add page.tsx - create one note
https://www.convex.dev/ - login - Data - one row

# Document List
```
npx convex dev
npm run dev
```
# Trash box
```
npx shadcn-ui@latest add popover
npx shadcn-ui@latest add input
npx shadcn-ui@latest add alert-dialog
```
# Search functionality
```
npm i zustand
npx shadcn-ui@latest add command
npx shadcn-ui@latest add dialog
```
# Settings
`npx shadcn-ui@latest add label`
# Toolbar component (Icon, Title)
```
npm i react-textarea-autosize
npm i emoji-picker-react
```
# Cover Image (File Upload)
`npm i zod react-dropzone @edgestore/react @edgestore/server`

edgestore.dev - login - new project - "name: antonio-notion" - copy two envs to .env.local

- env.local
```
EDGE_STORE_ACCESS_KEY=
EDGE_STORE_SECRET_KEY=
```
