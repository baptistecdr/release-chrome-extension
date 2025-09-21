# Release Chrome Extension

This is a GitHub Action to publish a Chrome extension to the Chrome Web Store.

## Quick start

The minimal usage is as follows:

```yaml
- uses: baptistecdr/release-chrome-extension
  with:
    extension-id: "********************************"
    extension-path: "path/to/your/extension.zip"
    oauth-client-id: ${{ secrets.OAUTH_CLIENT_ID }}
    oauth-client-secret: ${{ secrets.OAUTH_CLIENT_SECRET }}
    oauth-refresh-token: ${{ secrets.OAUTH_REFRESH_TOKEN }}
```

The `oauth-client-id`, `oauth-client-secret`, and `refresh-token` are all required to authenticate with the Chrome Web Store API. You can find more information on how to get these values [here](https://developer.chrome.com/webstore/using_webstore_api#beforeyoubegin).

There is also a mock OAuth2 application that can be used to get a refresh token.  You can get the token by running the following command:

```bash
node oauth-mock-app/server.mjs
```

### Inputs

All supported inputs are the following:

| Name                  | Description                         | Required |
|-----------------------|-------------------------------------|----------|
| `extension-id`        | The ID of the extension to publish. | Yes      |
| `extension-path`      | The path to the extension zip file. | Yes      |
| `oauth-client-id`     | The OAuth2 client ID.               | Yes      |
| `oauth-client-secret` | The OAuth2 client secret.           | Yes      |
| `oauth-refresh-token` | The OAuth2 refresh token.           | Yes      |

## How to build

- Install [Node.JS LTS](https://nodejs.org/)
- Clone the project
- Run `npm install`
- Run `npm run package`

## Bugs and feature requests

Have a bug or a feature request? Please first search for existing and closed issues. If your problem or idea is not
addressed yet, [please open a new issue](https://github.com/baptistecdr/release-chrome-extension/issues/new).

## Contributing

Contributions are welcome!
