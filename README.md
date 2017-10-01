# runningbeta/xmrig-proxy

Monero (XMR) and AEON Stratum protocol proxy

This is an Ubuntu Linux Docker image running [XMRig proxy](https://github.com/xmrig/xmrig-proxy).

# Basic example

`docker run --restart unless-stopped runningbeta/xmrig-proxy -o POOL -u YOUR_WALLET -p PASSWORD --bind 0.0.0.0:3333 --bind 0.0.0.0:5555`

# Failover

`docker run --restart unless-stopped runningbeta/xmrig-proxy -o POOL01 -u YOUR_WALLET01 -o POOL02 -u YOUR_WALLET02 -p PASSWORD --bind 0.0.0.0:5555`

For failover you can add multiple pools, maximum count not limited.

# Full example

`docker run --restart unless-stopped runningbeta/xmrig-proxy -o r8.network:5222 -u 4AjqdPQxRA1aot1nwAFn8M6wHcUhZupiJMjAkbxeitGV4YBZsn4rKBYdUEHQC5GxTwP8tg8yhuHoYL2qCEcTxeRN4vr47ae -o pool.supportxmr.com:5555 -u 4AjqdPQxRA1aot1nwAFn8M6wHcUhZupiJMjAkbxeitGV4YBZsn4rKBYdUEHQC5GxTwP8tg8yhuHoYL2qCEcTxeRN4vr47ae -p x --bind 0.0.0.0:3333 --bind 0.0.0.0:5555`

# Options

```
  -b, --bind=ADDR       bind to specified address, example "0.0.0.0:3333"
  -o, --url=URL         URL of mining server
  -O, --userpass=U:P    username:password pair for mining server
  -u, --user=USERNAME   username for mining server
  -p, --pass=PASSWORD   password for mining server
  -k, --keepalive       send keepalived for prevent timeout (need pool support)
  -r, --retries=N       number of times to retry before switch to backup server (default: 5)
  -R, --retry-pause=N   time to pause between retries (default: 5)
      --no-color        disable colored output
      --verbose         verbose output
  -B, --background      run the miner in the background
  -l, --log-file=FILE   log all output to a file
  -h, --help            display this help and exit
  -V, --version         output version information and exit
```

# Donations

Development of Monero and tools can be supported directly through donations.

Proxy at this moment does not contain any developer fee. Future updates may change this. Until then you can make an one time donation to this organizations:

monero-project XMR: `44AFFq5kSiGBoZ4NMDwYtN18obc8AemS33DBLWs3H7otXft3XjrpDtQGv7SqSsaBYBb98uNbr2VBBEt7f2wfn3RVGQBEP3A`
xmrig XMR: `48edfHu7V9Z84YzzMa6fUueoELZ9ZRXq9VetWzYGzKt52XU5xvqgzYnDK9URnRoJMk1j8nLwEVsaSWJ4fhdUyZijBGUicoD`
r8-network XMR: `4AjqdPQxRA1aot1nwAFn8M6wHcUhZupiJMjAkbxeitGV4YBZsn4rKBYdUEHQC5GxTwP8tg8yhuHoYL2qCEcTxeRN4vr47ae`
