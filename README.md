# Handshake Explorer Redirector

A simple, client-side redirector to your favorite Handshake blockchain explorer.

## What is this?

This tool allows you to set a preferred Handshake explorer once and then use a single, consistent URL format to look up transactions, addresses, blocks, and names. It saves your preference in your browser's local storage and automatically redirects you.

For example, after setting your explorer, you can go to `explorer.hns.dev/name/proofofwork` and be redirected to the correct page on your chosen explorer (e.g., `https://e.hnsfans.com/name/proofofwork`).

## How to Use

1.  **Visit explorer.hns.dev**.
2.  **Choose your explorer:**
    - Select one of the pre-configured explorers from the dropdown menu.
    - Or, select "Custom..." to configure your own.
3.  **Save your preference.**
4.  You're all set! Now you can use the following URL formats:
    - `explorer.hns.dev/tx/<transaction_hash>`
    - `explorer.hns.dev/address/<handshake_address>`
    - `explorer.hns.dev/block/<block_height>`
    - `explorer.hns.dev/name/<handshake_name>`

The site will redirect you to the correct page on your chosen explorer.

### Changing Your Explorer

To change your setting, visit `https://explorer.hns.dev/?redirect=false`.

## Custom Explorers

If your favorite explorer isn't on the list, you can add it yourself. Select "Custom..." from the dropdown and fill in the following fields:

- **Provider Name:** A friendly name for your explorer (e.g., "My HNS Explorer").
- **Transaction URL Template:** The URL structure for transactions. Use `{tx}` as a placeholder for the transaction hash.
  - _Example:_ `https://my-explorer.com/transactions/{tx}`
- **Address URL Template:** The URL structure for addresses. Use `{address}` as a placeholder for the address.
  - _Example:_ `https://my-explorer.com/addresses/{address}`
- **Block URL Template:** The URL structure for blocks. Use `{block}` as a placeholder for the block height or hash.
  - _Example:_ `https://my-explorer.com/blocks/{block}`
- **Name URL Template:** The URL structure for Handshake names. Use `{name}` as a placeholder for the name.
  - _Example:_ `https://my-explorer.com/names/{name}`

## Self-Hosting

This is a single `index.html` file with no server-side dependencies. You can download it and host it on any static web hosting service.

## Technology

- HTML
- Vanilla JavaScript
- Tailwind CSS (via CDN)
