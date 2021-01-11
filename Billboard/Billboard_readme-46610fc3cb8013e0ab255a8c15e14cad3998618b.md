## Description
Welcome to the billboard, you can post an advertisement on the billboard chain, and the more coin you deposit the higher your advertisement ranking will be.

[Attachment](https://rwctf2021.s3-us-west-1.amazonaws.com/Billboard-c6ef484de3903a4f87a406327610a6888a5e4fae.zip)  
[Playground](http://54.177.154.38:8080)  

RPC: http://54.177.154.38:26657  

## Goal
Send a successful `CaptureTheFlag`  type transaction.

## Instruction
1. Gen&add player private key

```
$ billboardcli keys mnemonic --unsafe-entropy
> your team token md5 + 32 * "0"

$ echo "your mnemonic here" | billboardcli keys add $KEY --recover
```

2. Check balance, should be none-zero

```
$ billboardcli query account $ADDRESS --node $RPC
```

3. Post an advertisement

```
$ billboardcli tx billboard create-advertisement $ID $CONTENT --from $KEY --chain-id mainnet --fees 10ctc --node $RPC
```

## Hint
* The playground website is only used for AD display and TX hash submission (Not a web challenge !!!)
* For fairness, we have banned some query RPC https://github.com/iczc/tendermint/commit/42111f2a780d7910fcc7adac61d65628d0fa4ea7