- `pnpm add better-auth`

<!-- SHADCN -->

- `pnpm dlx shadcn@latest init`
- `pnpm add next-themes`
- `pnpm dlx shadcn@latest add button dropdown-menu`

<!-- PRISMA -->

- Dont Forget `pnpm add better-auth`
- Create a theme provider https://ui.shadcn.com/docs/dark-mode/next
- Create a file named auth.ts in one of these locations:
- - Project root
- - lib/ folder
- - utils/ folder
- `pnpm i @prisma/client`
- `pnpm i -D prisma`
- `pnpm dlx prisma init`
- Create auth.ts & copy paste its content (see prismaORM scroll: https://www.better-auth.com/docs/installation) except prisma import (NOTE: PLZ PASS ADAPTER IN AUTH.TS FILE THATS WHY IT IS WORKING!)
- Connect DB in env
- https://www.prisma.io/docs/orm/more/help-and-troubleshooting/nextjs-help & create that file
- ignore file error for now & delete import statement bcz we import it other way
- import the prisma in auth.ts file from the above created file
- run thi `npx @better-auth/cli generate` say 'y', this will give error to solve it
- to fix this create a dummy/test model in prisma/schema.prisma
- model Test {
  id String @id @default(uuid())
  test String
  }
- run `pnpm dlx prisma db push`
- run `pnpm dlx prisma generate`
- After it success go to prisma.ts hover over prismaClient and import from './generated/prisma'
- again run `npx @better-auth/cli generate`
