BudgetBuddy
===
## Project Description:

In this project, I have made a transaction categorisation on the transaction data taken from Plaid API. 

## Prerequisites:

- Current version of [Node.js](https://nodejs.org/). >=v14.0.0
- Private key of the sender's account
  - If the account was created using [near-cli](https://docs.near.org/tools/near-cli) or you ran [near login](https://docs.near.org/tools/near-cli#for-accounts) in your terminal, the private key can be found in a `.json` file located in `/HOME/.near-credentials`.
  - If the account was created using [NEAR Wallet](https://wallet.testnet.near.org/), the key can be found in the browser's Local Storage (in your browser's Developer tools... `Application >> Storage >> Local Storage`). Watch [this short video](https://youtu.be/rw2Tdc-7ccM) to learn how to get it.

## Setup:

1) Setup an environment variable `SENDER_PRIVATE_KEY` with the private key of the sender's account.

Either create a `.env` file in the root of this project, or export a bash variable by running the following in your terminal (replacing the example key).

```bash
export SENDER_PRIVATE_KEY=3wb4fVQvafPebkcCmyQPgMa2VsnX3JAQXZ4gjpc3kSu9AbVtLpLZqEog4xTbJrJxG1Y88SkHpuJV58GmPRnPXMD
```

2) Install dependencies by running:
```bash
npm i
```

## Built Using:
<table>
  <tr>
    <th><b>Purpose</b></th>
    <th><b>Technology</b></th>
  </tr>

  <tr>
    <td align="center">Notebook Environment</td>
    <td>
      <img src="https://github-readme-tech-stack.vercel.app/api/cards?theme=github_dark&title=Jupyter Noteboook&lineCount=1&line1=Jupyter,Jupyter,auto;python,python,61DAFB">
    </td>
  </tr>

  <tr>
    <td align="center">Programming Language</td>
    <td>
      <img src="https://github-readme-tech-stack.vercel.app/api/cards?theme=github_dark&title=Python&lineCount=1&line1=Python,Python,auto;python,61DAFB">
    </td>
  </tr>

  <tr>
    <td align="center">Data Manipulation and Visualisation</td>
    <td>
      <img src="https://github-readme-tech-stack.vercel.app/api/cards?theme=github_dark&title=Pandas&lineCount=1&line1=Pandas,Pandas,auto,61DAFB">
    </td>
  </tr>
</table>

### Send Tokens (High Level)
>[`send-tokens-easy.js`](./send-tokens-easy.js) will show you the easiest (JavaScript) way to send NEAR tokens (Ⓝ) using a [`near-api-js`](https://github.com/near/near-api-js) method; `account.sendMoney()`

1) In `send-tokens-easy.js`, update:
  - account IDs for `sender` and `receiver`.
  - network ID (`default` is `testnet`)

2) Run the file and send those tokens!

```bash
node send-tokens-easy.js
```

### Send Tokens (Low Level)
>[`send-tokens-deconstructed.js`](./send-tokens-deconstructed.js) completely dissects the transaction construction process and shows the lowest level way to send NEAR tokens (Ⓝ).

1) In `send-tokens-deconstructed.js`, update:
  - account IDs for `sender` and `receiver`.
  - network ID (`testnet` is default)
2) Enter the amount of Ⓝ you would like to send.
3) Run the file and send those tokens!
  
```bash
node send-tokens-deconstructed.js
```

For a detailed walk-through, see the [create-transactions](https://docs.near.org/integrator/create-transactions) doc.

Happy coding! 🚀 