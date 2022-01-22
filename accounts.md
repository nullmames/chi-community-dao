chihuahuad tx send <address-wallet-ms> <address-wallet-rc> 500000uhuahua --chain-id chihuahua-1 --generate-only >> tx.json

chihuahuad tx send <address-wallet-ms> <address-wallet-rc> 500000uhuahua --chain-id chihuahua-1 --generate-only >> tx.json

curl -s https://raw.githubusercontent.com/nullmames/chi-community-dao/main/tx/20220122/unsignedTx.json

chihuahuad tx sign unsignedTx.json --from coldchain --multisig chi-dao --chain-id chihuahua-1 --node https://rpc.chihuahua.wtf:443 5000uhuahua --signature-only 

chihuahuad tx multisign --from kingnodes tx.json chi-dao coldchain.json sig-karan.json > tx_signed.json


Karan

chihuahuad keys add karan --recover

chihuahuad keys add coldchain --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A1tmBTxbDQ5K2AZV9qm9Oy8d6QgGwzXt4TlajRZs7zFM"}'

chihuahuad keys add JA --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"Aw6o9s6kqbR+TgMh77qirhBwW0tR1tVmihnBiKa5nWJ2"}'

chihuahuad keys add chi-dao --multisig JA,coldchain,karan --multisig-threshold 2


Coldchain

chihuahuad keys add coldchain --recover

chihuahua keys add karan --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"AtQbuGTkRQriVcO77gEJlPEYMgvGYTqlY8abw1rT6Eje"}'

chihuahuad keys add JA --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"Aw6o9s6kqbR+TgMh77qirhBwW0tR1tVmihnBiKa5nWJ2"}'

chihuahuad keys add chi-dao --multisig JA,coldchain,karan --multisig-threshold 2


JA

chihuahuad keys add JA --recover

chihuahua keys add karan --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"AtQbuGTkRQriVcO77gEJlPEYMgvGYTqlY8abw1rT6Eje"}'

chihuahuad keys add coldchain --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A1tmBTxbDQ5K2AZV9qm9Oy8d6QgGwzXt4TlajRZs7zFM"}'

chihuahuad keys add chi-dao --multisig JA,coldchain,karan --multisig-threshold 2