# Metabase on a sub-path in local dev

## What is this

This is a simple tunnel to have metabase on a subpath tunnel to your local environment

## How to use

- In metabase admin settings, set the metabase url to `https://localhost:9090/metabase/`
- Build the metabase frontend statically (this does not currently work with hot-reload, so you'll need to stop your local frontend hot reload environment): `MB_EDITION=ee yarn build`
- Run the metabase backend alone: `ENTERPRISE_TOKEN='xxx' clojure -M:run:dev:ee"` in your metabase development directory
- run `docker compose up` in this directory
- Navigate to `https://localhost:9090/metabase/` and you should see the your local metabase dev environment running properly in a subpath
