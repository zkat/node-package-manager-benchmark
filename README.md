# Node package manager benchmark

This benchmark compares the performance of [npm](https://github.com/npm/npm), [npm ci](https://github.com/npm/npm/blob/latest/doc/cli/npm-ci.md) [pnpm](https://github.com/pnpm/pnpm) and [yarn](https://github.com/yarnpkg/yarn).

## React app

The app's `package.json` [here](./fixtures/react-app/package.json)

| action  | cache | lockfile | node_modules| npm i | Yarn | pnpm | npm ci
| ---     | ---   | ---      | ---         | --- | --- | --- | --- |
| install |       |          |             | 22.8s | 21.4s | 45.6s | N/A |
| install | ✔    | ✔        | ✔           | 6.7s | 1s | 1.3s | 11.3s |
| install | ✔    | ✔        |             | 12.2s | 8.2s | 9.5s | 6.9s |
| install | ✔    |          |             | 21.1s | 10.8s | 16.3s | N/A |
| install |      | ✔        |             | 14.4s | 17.6s | 33.9s | 8.6s |
| install | ✔    |          | ✔           | 6.7s | 7.6s | 11s | N/A |
| install |      | ✔        | ✔           | 6.8s | 1.1s | 1.2s | 13.5s |
| install |      |          | ✔           | 6.4s | 16.6s | 37.2s | N/A

![Graph of the react-app results](./results/imgs/react-app.svg)

## Ember app

The app's `package.json` [here](./fixtures/ember-quickstart/package.json)

| action  | cache | lockfile | node_modules| npm i | Yarn | pnpm | npm ci
| ---     | ---   | ---      | ---         | --- | --- | --- | --- |
| install |       |          |             | 27.3s | 42.5s | 1m 37.3s | N/A |
| install | ✔    | ✔        | ✔           | 6.1s | 1.6s | 1.7s | 20.8s |
| install | ✔    | ✔        |             | 17.3s | 17.4s | 16.3s | 12.3s |
| install | ✔    |          |             | 26.6s | 21s | 22.1s | N/A |
| install |      | ✔        |             | 21.5s | 43.3s | 58.2s | 15.5s |
| install | ✔    |          | ✔           | 5.5s | 9.8s | 14.1s | N/A |
| install |      | ✔        | ✔           | 6s | 1s | 1.7s | 25.1s |
| install |      |          | ✔           | 5.3s | 34.8s | 57.4s | N/A

![Graph of the ember-quickstart results](./results/imgs/ember-quickstart.svg)

## Angular app

The app's `package.json` [here](./fixtures/angular-quickstart/package.json)

| action  | cache | lockfile | node_modules| npm i | Yarn | pnpm | npm ci
| ---     | ---   | ---      | ---         | --- | --- | --- | --- |
| install |       |          |             | 23.6s | 30.3s | 1m 7.7s | N/A |
| install | ✔    | ✔        | ✔           | 6.9s | 1.1s | 1.6s | 14.3s |
| install | ✔    | ✔        |             | 14.1s | 11.6s | 13.9s | 8.6s |
| install | ✔    |          |             | 22.3s | 22.4s | 20.1s | N/A |
| install |      | ✔        |             | 16.1s | 25.1s | 49.8s | 10.5s |
| install | ✔    |          | ✔           | 7.1s | 10.6s | 13.9s | N/A |
| install |      | ✔        | ✔           | 7s | 1.1s | 1.4s | 16.9s |
| install |      |          | ✔           | 6.3s | 24.2s | 46.8s | N/A

![Graph of the angular-quickstart results](./results/imgs/angular-quickstart.svg)

## Medium Size App

The app's `package.json` [here](./fixtures/medium-size-app/package.json)

| action  | cache | lockfile | node_modules| npm i | Yarn | pnpm | npm ci
| ---     | ---   | ---      | ---         | --- | --- | --- | --- |
| install |       |          |             | 23s | 22.1s | 43.8s | N/A |
| install | ✔    | ✔        | ✔           | 6.4s | 1s | 1.4s | 11.6s |
| install | ✔    | ✔        |             | 12.3s | 8.6s | 9.9s | 6.5s |
| install | ✔    |          |             | 20.9s | 11.7s | 16s | N/A |
| install |      | ✔        |             | 13.9s | 19.4s | 34.3s | 8.2s |
| install | ✔    |          | ✔           | 6.1s | 7.1s | 10.6s | N/A |
| install |      | ✔        | ✔           | 6.4s | 1s | 1.4s | 14.5s |
| install |      |          | ✔           | 5.9s | 17.3s | 39.5s | N/A

![Graph of the medium-size-app results](./results/imgs/medium-size-app.svg)

## Lots of Files

The app's `package.json` [here](./fixtures/alotta-files/package.json)

| action  | cache | lockfile | node_modules| npm i | Yarn | pnpm | npm ci
| ---     | ---   | ---      | ---         | --- | --- | --- | --- |
| install |       |          |             | 5.8s | 32.9s | 50s | N/A |
| install | ✔    | ✔        | ✔           | 6.1s | 987ms | 2.5s | 19.8s |
| install | ✔    | ✔        |             | 16.9s | 12.9s | 10.1s | 10.2s |
| install | ✔    |          |             | 25.1s | 17.7s | 20.5s | N/A |
| install |      | ✔        |             | 17.1s | 23.4s | 39s | 11.2s |
| install | ✔    |          | ✔           | 7.1s | 11s | 14.3s | N/A |
| install |      | ✔        | ✔           | 6.7s | 980ms | 1.9s | 22.6s |
| install |      |          | ✔           | 6.2s | 18.3s | 46.1s | N/A

![Graph of the alotta-files results](./results/imgs/alotta-files.svg)