#LOCAL
```
aliend init alien --chain-id=ovni
```
## Create WalletOne

```
aliend keys add walletOne
```
###Output

```
- name: walletOne
  type: local
  address: alien1ajay55sd4474vrs97fesqky9wt0rf9epyfw4ce
  pubkey: '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"AzFA6EwnPrmls0QDot+6d79/wOMzbIRZWwZSBEuasLzb"}'
  mnemonic: ""
awesome problem genre agree paddle field banana witness wink business ask term hair doctor tree pond churn burden series involve swift author stem today
```
#------------------------------ 

## Add Balance walletOne

```
aliend add-genesis-account alien1ajay55sd4474vrs97fesqky9wt0rf9epyfw4ce 1000000000ualien,80000000000000umicro

```


# Validator 1 143.110.153.115
 
```
aliend keys add validator1
```



#### Output
```
alien1txe65juz5mp0v2n4ycvemgk3592wpc40uhppdd
initial hollow electric rescue solar inmate echo innocent journey gold ranch end valley tornado carbon oppose surface curious badge love master degree draft reason
```

####Init Chain
```
aliend init alien --chain-id=ovni
```

### Add funds
```
aliend add-genesis-account alien1txe65juz5mp0v2n4ycvemgk3592wpc40uhppdd 100000000ualien
```

####sign gentx
```
aliend gentx validator1 100000000ualien --chain-id=ovni --moniker=validator1
```
##### Output

```
Genesis transaction written to "/home/alienuser/.alien/config/gentx/gentx-772724d7d7c6713ddbd4d1a07333a98a33ce4a21.json"
```

#### Make gentx folder & Download Gentx

```
mkdir ~/.alien/config/gentx
gentx="gentx-772724d7d7c6713ddbd4d1a07333a98a33ce4a21.json"
scp alienuser@143.110.153.115:/home/alienuser/.alien/config/gentx/$gentx ~/.alien/config/gentx/$gentx
```

### Delete genesis
```
rm ~/.alien/config/genesis.json
rm ~/.alien/config/config.toml
```


#------------------------------

# Validator 2 147.182.221.114

```
aliend keys add validator2
```
#### Output
```
alien1cs2unpaxvx3gz7q02qhxf5fma0zgzfldrgfuve
life junior climb picnic pitch upset educate casual victory alcohol dutch stand monkey bread report special history resource beauty boost slice desk bench please
```

####Init Chain
```
aliend init alien --chain-id=ovni
```

#### Add funds
```
aliend add-genesis-account alien1cs2unpaxvx3gz7q02qhxf5fma0zgzfldrgfuve 100000000ualien
```

####sign gentx
```
aliend gentx validator2 100000000ualien --chain-id=ovni --moniker=validator2
```
#####output
```
Genesis transaction written to "/home/alienuser/.alien/config/gentx/gentx-aaad05cd6d62d80bcc5bfeb96e3e74a3e52dbf52.json"
```

#### Make gentx folder & Download Gentx

```
gentx="gentx-aaad05cd6d62d80bcc5bfeb96e3e74a3e52dbf52.json"
scp alienuser@147.182.221.114:/home/alienuser/.alien/config/gentx/$gentx ~/.alien/config/gentx/$gentx
```

### Delete genesis
```
rm ~/.alien/config/genesis.json
rm ~/.alien/config/config.toml
```


#LOCAL

## Add Val1 and Val2
```
aliend add-genesis-account alien1txe65juz5mp0v2n4ycvemgk3592wpc40uhppdd 1000000000ualien
aliend add-genesis-account alien1cs2unpaxvx3gz7q02qhxf5fma0zgzfldrgfuve 1000000000ualien
```

```
aliend collect-gentxs
```

### Copy genesis back to val1 and val2

```
scp ~/.alien/config/genesis.json alienuser@143.110.153.115:/home/alienuser/.alien/config/genesis.json
scp ~/.alien/config/genesis.json alienuser@147.182.221.114:/home/alienuser/.alien/config/genesis.json

scp ~/.alien/config/config.toml alienuser@143.110.153.115:/home/alienuser/.alien/config/config.toml
scp ~/.alien/config/config.toml alienuser@143.110.153.115:/home/alienuser/.alien/config/config.toml




```
