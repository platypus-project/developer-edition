# Setup TheGraph and Uniswap webclient

1.  Change postgres user and password in postgres and graph-node service

    ```yaml
    environment:
      POSTGRES_USER: <postgres_user>
      POSTGRES_PASSWORD: <postgres_password>
    ```
2. (Optional) Change ethereum url in graph-node service

   ```yaml
   ethereum: 'mainnet:https://rpc1.piccadilly.autonity.org/'
   ```
3. Change webclient image in webclient-uniswap and pluto-landing service
    ```yaml
    webclient-uniswap:
        image: <webclient_image_url>
    ...
    pluto-landing:
        image: <pluto_landing_image_url>
    ```

4. Run in terminal
    ```bash
        docker compose up -d
    ```

### This docker-compose.yml will deploy TheGraph node with ipfs and postgres, and uniswap webclient.