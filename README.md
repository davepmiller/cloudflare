# ☁️🚀 cliflare 🚀☁️
[![Coverage Status](https://coveralls.io/repos/github/davepmiller/cliflare/badge.svg?branch=main)](https://coveralls.io/github/davepmiller/cliflare?branch=main)
* 🛠 CLI️ to interact with Cloudflare APIs.
* 🥳 An excuse to write some Rust
* 👷 Under heavy development!!! Happy for help!

#### Setup:
* [Install Rust 📝](https://www.rust-lang.org/tools/install)
    ```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```
* Install
    ```bash
    cargo install cliflare
    ```
* [Generate a Cloudflare API token 📝](https://developers.cloudflare.com/cloudflare-one/api-terraform/scoped-api-tokens/)
* [Grab Account And Zone IDs 📝](https://developers.cloudflare.com/fundamentals/setup/find-account-and-zone-ids/)
* Environment
  ```bash
  # add your token value to a startup script
  echo CLOUDFLARE_TOKEN=abcd1234**API_TOKEN**4321dcba >> ~/.zshrc
  echo CLOUDFLARE_ACCOUNT_ID=abcd1234**ACCOUNT_ID**4321dcba >> ~/.zshrc
  ```
#### Execute:
* [Token Verify 📝](https://developers.cloudflare.com/api/operations/user-api-tokens-verify-token)
    ```bash
    cliflare token verify
    ```
* [Zone List 📝](https://developers.cloudflare.com/api/operations/zones-get)
    ```bash
    # print out all zone info
    cliflare zone list
    # print domain name for each zone
    cliflare zone list --domains
    ```
* [Create Zone 📝](https://developers.cloudflare.com/api/operations/zones-post)
  ```bash
  cliflare zone create newzone.com
  ```
* [List DNS Records For A Zone](https://developers.cloudflare.com/api/operations/dns-records-for-a-zone-list-dns-records)
  ```bash
  cliflare zone dns list --id <ZONE_ID>
  ```

#### Coming Soon:
* [Zone Details](https://developers.cloudflare.com/api/operations/zones-0-get)
* [Create DNS Record For A Zone](https://developers.cloudflare.com/api/operations/dns-records-for-a-zone-create-dns-record)

#### Coming Soonish:
* Homebrew setup
* Create WAF rules
* Create redirect rules
* Create some other rules
