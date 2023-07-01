
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


=====

# [OAuth2 using Google, PocketBase, and SvelteKit](https://www.youtube.com/watch?v=Ig_RMc0GFw4&list=PLHT1TNReACRcHR8rMnB8T0JSMIpz-Z7Mp&index=3)

> [Github](https://github.com/consultingninja/pbOAuth2)

> [Google Cloud Console](https://console.cloud.google.com/apis/dashboard)

## create project
- name: `MoonPocketBase`
- id: `moonpocketbase`


## OAuth consent screen
- User Type: `External` > `CREATE`
- App information
  - App name: `svelte-pocketbase`
  - User support email: `mooninlearn@gmail.com`

- App logo

- App domain
  - 

- Authorized domains
  - 

- Developer contact information
  - 

`SAVE AND CONTINUE`


### Scopes

> `ADD OR REMOVE SCOPES`

- ./auth/userinfo.email
- ./auth/userinfo.profile
- openid

`SAVE AND CONTINUE`

### Test users

> `+ ADD USERS`

- `mooninlearn@gmail.com`

`SAVE AND CONTINUE`


## Credentials

> [Google Cloud](https://console.cloud.google.com/apis/dashboard) > `Credential`(좌측 메뉴) 클릭 > `+ CREATE CREDENTIALS` `OAuth client ID`(상단 select 메뉴)

  - Application type: `Web application`
  - Name: `Svelte-Pocketbase`
  - Authorized JavaScript origins
    - `+ ADD URI`
      - `http://localhost:5173`
  - Authorized redirect URIs
    - `+ ADD URI`
      - `http://localhost:5173/oauth`

  - `CREATE` 클릭

> `Your Client ID`(popup) Copy => `pocketbase settings`, `.env`
> `Your Client Secret`(popup) Copy => `pocketbase settings`, `.env`

### Settings / Application

```
http://127.0.0.1:8090/_/
```
> Settings 버튼(좌측 최하단 Settings 아이콘) 클릭 > `Authentication` > `Auth providers`

> Google > `Google provider` `Enable`

> `Your Client ID`(popup) Copy => Paste to `Google provider > Client ID`
> `Your Client Secret`(popup) Copy => Paste to `Google provider > Client Secret`

> `Save changes` 버튼 클릭

### `.env`
```ini
SECRET_GOOGLE_CLIENT_ID=
SECRET_GOOGLE_CLIENT_SECRET=
```

## Edit

> `pocketbase.bat`

> `src/hooks.server.ts`

> `src/routes/signup/+page.svelte`, `src/routes/signup/+page.server.ts`

> `src/routes/oauth/+server.ts`

> `src/routes/+page.svelte`, `src/routes/+layout.svelte`

## Run

### pocketbase server
```bash
cd C:\MoonDev\withTool\inPocketBase\learning\Youtube\ConsultingNinja\learn-pocketbase-youtube-consulting_ninja-ts
pocketbase.bat
```

### svelte client

```bash
cd C:\MoonDev\withTool\inPocketBase\learning\Youtube\ConsultingNinja\learn-pocketbase-youtube-consulting_ninja-ts
yarn dev --open
```

```
http://localhost:5173/signup
```