# upSOL Solana NFT automation
## Simple API layer to send NFT as loyalty program for ecommerce



Introducing our revolutionary product, designed to provide a strong and secure API layer for affiliate NFT digital receipts. With the increasing demand for non-fungible tokens (NFTs), our product offers a comprehensive solution to help affiliates securely manage their digital receipts in a decentralized and transparent manner. Our API layer ensures that all transactions are executed seamlessly, while also providing robust security features to protect the integrity of the data. Trust and security are our top priorities, and our product is designed to deliver just that, making it the ideal choice for anyone looking to leverage the power of NFTs in their affiliate marketing strategy.


## Features

- Fully Automated NFT drop based on trigger
- Zapier Integration
- Rest API
- Managment webapp
- Shopify module, create special discount for holders and exclusive product

## Description

Our product offers seamless NFT automation that is connected with ecommerce platforms, making it easier than ever before to manage your NFT transactions. Our platform is also integrated with Zapier automation, enabling you to automate various tasks and workflows, thus saving you time and effort.

Our NFT automation feature is designed to provide end-to-end support for the creation, transfer, and management of NFTs. It offers a user-friendly interface that enables you to easily mint, list, and sell your NFTs. Additionally, you can use our platform to view your NFT analytics and track your sales performance.

With our Zapier integration, you can connect your NFT automation to over 2,000 applications, including ecommerce platforms, CRMs, and email marketing tools. This integration provides endless possibilities for automating your NFT transactions and workflows. You can set up triggers and actions to automatically create NFTs when a new product is added to your ecommerce store, transfer NFTs to buyers after a successful purchase, and much more.

In summary, our product offers a comprehensive solution for managing your NFTs, with seamless integration with ecommerce platforms and the power of Zapier automation. Try our product today and take your NFT marketing strategy to the next level.

## Possibile NFT integration

![alt text](https://github.com/3dvolt/upSOL/blob/main/img/API%20flow%202.jpg)

## API usage

Here is a full documentation about API

### Create new NFT collection
POST 
https://api.upsol.app/collection/create
```sh
Body
raw (json)
{
  "img_path": "path/logo.png",
  "name": "Demo 2",
  "description": "demo nft description 2",
  "supply": 100,
  "collectionName": "Collection Name 2"
}
```
response example
```
{
  "sol_addr": "7P7BKjKMTPEXDg7nkXm7daftnhMNyVYhoZ5oay8DnyRj", //SOLANA address
  "APIkey": "a112-ac79-4f42-b6c5-c9ba2f3", //api key, store in a secure place
  "sol_balance": 0.6 //balance that is needed to create collection
}
```

### Validate collection / verify balance
POST 
https://api.upsol.app/collection/validate
```sh
Body
raw (json)
{
  "API": "1408-949a-4fb7-8ab7-9c6bdab0cc"
}
```

response example
```
{
  "status": "update status",
  "value": 0, //current balance
  "needed": 0.6 //balance needed
}
```

### Send NFT to wallet
POST 
https://api.upsol.app/collection/send
```sh
Body
raw (json)
{
  "API": "949a--8ab7-9c6bdacc",
  "address": "CSjL1ZhKCAtpbfPC4jrH5eHF6KY"
}
```

response example
```
{
  "status": "send complete"
}
```

## Collection creation

##### once the balance is valid a scheduled job create the collection and update the status of the collection

## Flow

![alt text]()![alt text](https://github.com/3dvolt/upSOL/blob/main/img/API%20flow%202.jpg)

## Using WebAPP

to demonstrate the working flows a webapp as been created and let's the user be able to create their own collection and easily integrate with Zapier and +5400 available connectors

![alt text](https://miro.medium.com/v2/resize:fit:720/format:webp/1*7przvkgEivyU_rva54o_lg.png)

For more information about webapp please refer to this guide:

https://medium.com/@diego_46954/how-to-easily-use-upsol-solana-nft-integration-in-shopify-and-zapier-6241fc9b41



