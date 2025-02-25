# Server Config for TailTag

Contains compose & config files, and more for TailTag!

## Very WIP, little to no support & docs.

./certificates is not included, you need to bring your own (private.pem, public.crt)

./frontend is not included, clone it from https://github.com/TailTag/frontend

./landing-page is not included, and has been sunset, but it can be found at https://github.com/TailTag/landing-page

## How to set up?

clone the tailtag/frontend repo into ./frontend, and follow its setup instructions

create the .env.local file in the ./frontend/ dir

```ìni
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
```

create and configure the .env file: ./traefik/.env

create and configure the env file for supabase: ./supabase/.env

supply your own certificates in a dir called ./certificates (private.pem, public.crt)

## How to run?

```shell

cd traefik
docker compose up -d

cd ../supabase
docker compose up -d

cd ../frontend
docker compose up -d  --build

```
