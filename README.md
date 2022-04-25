# Okta Elasticsearch Node Example

In this tutorial, you'll learn to build a node application using Elasticsearch and secure it using Okta.

Please read [The Ultimate Guide to Using Elasticsearch in Node.js]() to walk through the tutorial.

**Prerequisites**

- Basic knowledge of JavaScript
- [Node.js](https://nodejs.org/en/)
- [Okta CLI](https://cli.okta.com/)

> [Okta](https://developer.okta.com/) has Authentication and User Management APIs that reduce development time with instant-on, scalable user infrastructure. Okta's intuitive API and expert support make it easy for developers to authenticate, manage and secure users and roles in any application.


## Getting Started

To install this example application, run the following commands:
```
git clone https://github.com/oktadev/okta-elasticsearch-node-example.git
cd okta-elasticsearch-node-example
```


### Create an OIDC Application in Okta

Create a free developer account with the following command using the [Okta CLI](https://cli.okta.com):

```shell
okta register
```

If you already have a developer account, use `okta login` to integrate it with the Okta CLI.

Provide the required information. Once you register, in the `backend` folder, create a client application in Okta with the following command:

```shell
okta apps create
```

You will be prompted to select the following options:
- Type of Application: **1: Web**
- Redirect URI: `https://localhost:8080/callback`
- Logout Redirect URI: `https://localhost:8080/`

Run `cat .okta.env` (or `.okta.env` on Windows) to see the issuer and credentials for your app.


### Create an Elasticsearch Cloud account

Create a trial account on Elasticsearch Cloud and update the `.elastic.env` file.


### Install dependencies and run the backend

To install the dependencies and start the app, run the following commands:

```bash
cd backend
npm install
node create-index.js
node index.js
```

### Install dependencies and run the frontend

To install the dependencies and start the app, run the following commands:

```bash
cd frontend
npm install
npm run dev # Start Vite development server
```

## Help

Please post any questions as comments on the [blog post](), or visit our [Okta Developer Forums](https://devforum.okta.com/).

## License

Apache 2.0, see [LICENSE](LICENSE).
