# Arweave TestWeave Docker

This repository contains the docker that setups a full arweave-node, including a gateway, on a local device. After having built and run this docker, you'll be able to use the [TestWeave SDK](https://github.com/ArweaveTeam/testweave-sdk) for testing your arweave application locally. 

# Prerequisite 
1. [Docker](https://docs.docker.com/engine/install/): version 16 or higher 
2. [Docker-Compose](https://docs.docker.com/compose/install/): verison ~1.27 or higher 

# Usage

1. Be sure to have docker and docker-compose on your system. 
2. Clone this repo;
3. Run `docker-compose up` (add a `-d` flag if you want to run it in detached mode). 

Now you'll have: 

- a full arweave node running on [http://localhost:1984](http://localhost:1984). Here you can access all the endpoints listed in this page: [https://docs.arweave.org/developers/server/http-api](https://docs.arweave.org/developers/server/http-api)
- a full arweave gateway running on [http://localhost:3000](http://localhost:3000) and an GraphQL playground running on [http://localhost:3000/graphql](http://localhost:3000/graphql). Here you can do all the amazing things graphql and arweave supplies together. You can find examples and tutorials here [https://gql-guide.vercel.app/](https://gql-guide.vercel.app/) 


So, now, [import the TestWeave SDK](https://github.com/ArweaveTeam/testweave-sdk) in your projects and HAPPY TESTDLING ! 🖖🌋🚀 

# Images used

https://hub.docker.com/r/lucaarweave/arweave-node - run an arweave node on your local machine

https://github.com/users/demo-hub/packages/container/package/testweave-gateway - run a gateway connected to the node

<!-- ## Build and publish the Docker

1. Clone this repo
2. Merge everything but the .env file from here: [https://github.com/ArweaveTeam/gateway](https://github.com/ArweaveTeam/gateway)
3. Run a `docker-compose build`
4. Run a `docker-compose up`
5. Verify that everything works on your local environment. So, after having done 3. and 4. you should verify the followings: 
   1. Clone the TestWeave SDK repository [https://github.com/ArweaveTeam/testweave-sdk](https://github.com/ArweaveTeam/testweave-sdk);
   2. Go inside the TestWeave SDK dir, and run a `npm install` and then a `npm run test`;
   3. Now you should have some TXs inside your arweave-node;
   4. Go to https://localhost:3000/TXID that should display something like: "Arweave is the best web3-related thing out there!!!"
   5. Check out that the arweave-node works too. Navigate to http://localhost:1984/tx/TXID that should display the JSON info about the transaction
   6. If 4. and 5. above work, then the docker built and run properly
6. Stop the docker container by running `docker-compose down` or by presing ctrl+c
7. Run `docker images` and sign down the ID of the image having the name: "testweave-docker_gateway"
8. If you are not logged in docker, do it by running `docker login −−username=<USERNAME> −−email=<EMAIL ID>`
9. Assign to that image a tag that is relevant to your docker user and that increments the latest version you have published of the image. For instance, since my username is "lucaarweave", since the last version I have published was the "0.0.1", and since my image ID is "e61546b17694" I have to run: `docker tag e61546b17694 lucaarweave/testweave-docker:0.0.2`
10. Publish the docker on docker-hub by running `docker push <user−name>/image−name`. For instance, for the example in 9. yous should run `docker push lucaarweave/testweave-docker:0.0.2`
11. To verify that everything worked properly: 
    1.  firstly clean your docker local system by running: `docker system prune` and `docker volume prune`
    2.  pull the image that you have published in 10. by running `docker pull <user−name>/image−name`. For instance, for the example in 9. you should run `docker pull lucaarweave/testweave-docker:0.0.2`
    3.  After the image is downloaded run `docker run <user−name>/image−name`, for instance -->

# RootJwk
Root JWK, it has an initial balance of 10000000 and the address MlV6DeOtRmakDOf6vgOBlif795tcWimgyPsYYNQ8q1Y

```
{
  "kty": "RSA",
  "e": "AQAB",
  "n": "zhTx5Kr9VNQrXGarf0EXySfbSePBbIQuSOpb07s3pM3q8HKCx-bbd_py8t-JxgwnKAmpGKt6UhOP0FeobGITCwr_O7ATFPrFgTbM-xLYG0JOzxUlPScyqdJ8rFRcSSpevfUyJ6UVTpA3LDQHEzf7kebjfMPeYwpsWuT3c9LP3j0kyPDOBini-LRUpKX3n4ljhJIHzl-Jdv6Z31U65kZRBR1LPwnjcBUg4hoc50i8JZsSLsrUYFfpYVuxM0L4ch0l2-FvPtmZs831mOQgT8e1s7GPB7kJBhrQBagGF3eVnAiImJjslXNQhy4eQr6Nffb5Wa61Tec52LX5-gmoNSuA0PW5yuYGuDO2faULW74u8ZfmMUxd2x3E3M6E0deP_rj27FUQCECdbO6ATVanA16wnW7MrySu2m-Kt83XyATdVoNDls-coxA4UxuX7Rmlr2eGM7ZRKtypt12GziKnZgNglK5c_4mmMP2xeeLU1fneBLkvuHSEnoFjqZnAaI0ei6pW8Jy3k8txI5MucaRkXdPOhCm3Nwj8B9rBAh0hU64NVVb7C28Gz8LCwZkRhtGRY_v2vzcS0DaomK2G63vyQMKx3VUc9_RnkxcI6bwy6xG2GBEjpV8tHxXgw8zGc53_8EMo-9EM1PpjOHHYyaYoubDbxHaSJPwCPqi_OlGbl2h8gIM",
  "d": "VTCEVB45Dd2NNSu9_iNW5VEkDdXoKec0SPEUV6DfXjG_SnlTxbYRiHXQGcU9a1CvyRXBQJD2RkKO4zWxSmh6bci0fKSLJtOJXKJeNvXxvsb41BLuK2ruPxRjdEuFQLuSoZzgCFJuTeVA4XV6bT_pr0UOSg-f-TogU6yt_EOrqTeGYshkqlibWmsVSGDRTbJaIL3LG00UAsw5qIBPkkyEBoS3C86XJcieKMlZpGRFXphNemlfRJpiv9vLEyE-mdGhylTVC1qhdpoPyg2Xq9MnMiqWsT8U02C3GHd-WSoWfwNqEAa7WgZqxg7S9I1X6Tf0mNWnXhZVK9gCB5IBZkVfAIR727N9eFu8QQfBUld3QNtT-JwIjXWvEsk6mc7vx3puiZiT75Adc40gV0-ynAjy2Pb1O51g9mqD19mqvwxUWeW0YBKO03dYUfw9P7lxNUaYZGoc7rUec94xznOZKxgyKXwGGPe1tROMVBZf3Ewv0yrsB6YmDXQVv1p9MHiJ6pd4iXfeyvZjzCAqwUUukMKC6C38KlVLhS_PvX1V4ebDmmfbhlQTwLyJIcL1fxrHDyOVA8ued-TI4ioXO1OXaPwjM6rwhvRYcah6UKRxnF23iJjDZ7sBedrowSYPAjDyeoU4go3MaJIcuuKl3wIrvBe-K8TczkrG4AFx7BktkRA80Lk",
  "p": "6lC25S1c8MQWSbw1a932A2MqjPMkB79H8VQ1eYxTCI7ihMGkubOwr-ZZTcGE_-S0O5GmHPklsAmdWqnNSEotuiCCLX-cvZwbiTi0EfD4P6A9BU8n2ElIuBwWxLZKoqM977Q-2qIUFnvpfPit8Shqu3x-OykEYHDnbSLbOphcbAI1-kGsBui-wmezbvXv-ULwLi3FKey_FJfP7nYf2RazNXk1b7lqe8l3UbotsC86FudHmJe6c7O0epcuUbADeu5cpKPTzf0CMJVsW152KWOc--tXTfA03gANl30qUGYnNm40qYntGxhpUtfUZYGTg9nHKKS-gteCobMVIxHNZk8q6Q",
  "q": "4SdWJW-MMFlrUhVLYmOTgzFNpZ9-xQ3GQ0-uJpjfqfFcwVaEyeLMQE2lDknCd58RwRpYHJBjKWIO8yhNkeIVcmSl1Fyg91g61gOBtXQoz6JQm5K9y2snGlj4BC4nQdP39dCdg7xjiRMa9nwEFnxL8hNN27xDq2n81F3VsFqG3VmXY5YMnALUjkNCVOZM_0h8L2RrOCLroKu_NI6WV1LIaAKe7y99ZiOsQl5MMjwp12n4ea_U7l_Oyp2NlEsp5idbYa1TrC8LOWOn80jgM_iE3DrxAB5JKuI8vx_A7Jrral-aLT4oTtJDKV9B5Y7PPuhDYZrqHOkI0fwUrDIRRzYUiw",
  "dp": "CnUxxIbCyCgoSoAw7jCI41vQsVvEtufNoTK99D_UEOS3rW8rF_KyJxej0rmZYwZlGOeGP3LLQNEdCcfcVqag5da_mKJCb6ABBp3WQ5q6qbRQJOWEhL24licCySLNr_aTNBiaWY20UdCT-jTrJoFESjvjMmbBQECpw5AzsqjMLzHmENZPhDttECYqtwAZBsn7CESYsSdU2-luqVjyUPEXbIKNZQAkhYPXZHlnwp5I_G60HlZfRvy1SGdo9NJjRWBQGDULpfzt1RdGL8nGglBk2EWHrv3Sjjn4YVN_yPjWNTKz_QEf6P6s7LqfSyx-VfspTWIU8qgFt4vTnK4VucQ8yQ",
  "dq": "BhZ2MdTuSXBhgnqo6yQeHPH8U3oYh2Nz9OX2o3yGr6WjCGc6d-r18tcmm1hLNcjLRhlcQIl25OuN0-1HC6a9RbaK9U772zQ7gwXdP_bAE70jyNES6KkhCYlWS2akEReWIMNfPuydFFu74uY_hgweUZFMDaDtg3j-KQ_Qc1A_TUTa3wpzlNROwvn2lS0U7-IZ2X4xl_b5wAJkzRr93aaTXJyVh4oVLenRAopiLQmLaBOpcEDc1QUqJjhUV6ogm-R8iAuTs5giCY80P1O9HCqgDQRa99HZ0JsFYXWOVddqfhnPpWGE3Xy57ChzM63E1MKa78ysf9OdNXBHbtB7vx0rOQ",
  "qi": "QTbN_oNqyg9Zi9k2zlR4qtBZwDlDwCU6E_QrCKDY1z3pIvLFmc9eVO8aLek_GEKvvjri8voEctK-lrPRipwpdXj7cxw93cfS86vK6FSkb9plkInBfoKnC7DEOTP2Gx7WpHNQPbR8C8yFAidiRKc7lqgvRSh0LvWBzZ-spUANKAfNBaR6RAy2EAavAojeRMGxANqjqqnYP3Vwl35ZwNtmzkK_qIvsjKe3xFWMiCfzeFatunV2xUhJNrenoBoNp4z_66Xu-jUPLwRcWDdI7fz3MD3kZBH3gH4t52Amod79WxRriRW0SYcUeuvKbAi9FJv0RiCnvt0vzkjpF0XtukyHIg"
}
```

From https://github.com/ArweaveTeam/testweave-sdk/blob/main/src/assets/arweave-keyfile-MlV6DeOtRmakDOf6vgOBlif795tcWimgyPsYYNQ8q1Y.json
