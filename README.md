
# learn-pocketbase-youtube-consulting_ninja-ts

> [PocketBase](https://www.youtube.com/playlist?list=PLHT1TNReACRcHR8rMnB8T0JSMIpz-Z7Mp)

> References
- [Picocss Documentation](https://picocss.com/docs/)
- [Picocss Github](https://github.com/picocss/pico)
- [Picocss Theme Default](https://github.com/picocss/pico/blob/master/css/themes/default.css)
- [Picocss > Docs > Customization](https://picocss.com/docs/customization.html)
- [SCSS](https://github.com/picocss/pico/blob/master/scss/pico.slim.scss)


# Install

```bash
# init app
bootapp -l node -u moondevnode -n learn-pocketbase-youtube-consulting_ninja-ts -d "Svelte Kit with Picocss(Web Start)" -t svelte-kit-pocketbase-ts
```

# Run

```bash
yarn dev --open
```

# setting:pocketbase

## start pocketbase
```bash
cd C:/JnJ-soft/Developments/Database/sqlite
pocketbase serve --dir="./pb-consullting_ninja" --http="127.0.0.1:8090"

# result
Server started at http://127.0.0.1:8090
 ➜ REST API: http://127.0.0.1:8090/api/
 ➜ Admin UI: http://127.0.0.1:8090/_/
```

## Admin login

```
http://127.0.0.1:8090/_/
```

> Admin sign in
```
mooninlearn@gmail.com
```


=====

# [Create a CRUD App with PocketBase and SvelteKit!](https://www.youtube.com/watch?v=Zm_DIu0MaBs&list=PLHT1TNReACRcHR8rMnB8T0JSMIpz-Z7Mp&index=2)

> [Github](https://github.com/consultingninja/pbCrud)

## Create collection

```
http://127.0.0.1:8090/_/
```

> collection: `jobs`

> fields
  - jobname  Text
  - salary  number

> sample record
- developer  50000

## Edit

> `.env`

> `src/lib/Navbar.svelte`

> `src/+layout.svelte`, `scr/+page.svelte`

> `src/routes/create/+page.svelte`, `src/routes/create/+page.server.ts`
> `src/routes/read/+page.svelte`, `src/routes/read/+page.server.ts`
> `src/routes/update/+page.svelte`, `src/routes/update/+page.server.ts`
> `src/routes/destroy/+page.svelte`, `src/routes/destroy/+page.server.ts`