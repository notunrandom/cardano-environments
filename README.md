# cardano-environments

Versioned copy of [environments][env] (i.e. configuration
files) for Cardano networks.

This is for use with the [homebrew-cardano][tap] tap.

Unfortunately although these files are available from at
least three places ([official][env], [source][io],
[CF][cf]), none of those reliably tag them in an
appropriate way for versioning.

The following commands are used to download them.

Preview:
```bash
curl --output-dir preview --remote-name-all --variable prefix=https://book.play.dev.cardano.org/environments/preview --expand-url "{{prefix}}/{config,config-legacy,tracer-config,db-sync-config,submit-api-config,topology,checkpoints,byron-genesis,shelley-genesis,alonzo-genesis,conway-genesis,peer-snapshot}.json" --expand-url "{{prefix}}/guardrails-script.plutus"
```

Preprod:
```bash
curl --output-dir preprod --remote-name-all --variable prefix=https://book.play.dev.cardano.org/environments/preprod --expand-url "{{prefix}}/{config,config-legacy,tracer-config,db-sync-config,submit-api-config,topology,byron-genesis,shelley-genesis,alonzo-genesis,conway-genesis,peer-snapshot}.json" --expand-url "{{prefix}}/guardrails-script.plutus"
```

Mainnet:
```bash
curl --output-dir mainnet --remote-name-all --variable prefix=https://book.play.dev.cardano.org/environments/mainnet --expand-url "{{prefix}}/{config,config-legacy,tracer-config,db-sync-config,submit-api-config,topology,topology-non-bootstrap-peers,checkpoints,byron-genesis,shelley-genesis,alonzo-genesis,conway-genesis,peer-snapshot}.json" --expand-url "{{prefix}}/guardrails-script.plutus"
```

[env]: https://book.play.dev.cardano.org/environments.html
[tap]: https://github.com/notunrandom/homebrew-cardano
[io]: https://github.com/input-output-hk/cardano-playground
[cf]: https://github.com/cardano-foundation/cardano-configurations
