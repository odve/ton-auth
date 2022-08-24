# ton-auth

## Build

### PasswordSB
`cd .\contracts\password-sb\toncli\`

`toncli run_tests`

## Deploy
`toncli deploy -n mainnet`

## Generate test message data
`fift -s .\data.fif`

## Send message
`toncli send -n testnet -a 0.03 --address "addr" --body ./fift/try.fif`