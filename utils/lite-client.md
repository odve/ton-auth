#Lite Client

## Help

list of available commands:
time    Get server time
remote-version  Shows server time, version and capabilities
last    Get last block and state info from server
sendfile <filename>     Load a serialized message from <filename> and send it to server
status  Show connection and local database status
getaccount <addr> [<block-id-ext>]      Loads the most recent state of specified account; <addr> is in [<workchain>:]<hex-or-base64-addr> format
saveaccount[code|data] <filename> <addr> [<block-id-ext>]       Saves into specified file the most recent state (StateInit) or just the code or data of specified account; <addr> is in [<workchain>:]<hex-or-base64-addr> format
runmethod[full] <addr> [<block-id-ext>] <method-id> <params>... Runs GET method <method-id> of account <addr> with specified parameters
dnsresolve [<block-id-ext>] <domain> [<category>]       Resolves a domain starting from root dns smart contract
dnsresolvestep <addr> [<block-id-ext>] <domain> [<category>]    Resolves a subdomain using dns smart contract <addr>
allshards [<block-id-ext>]      Shows shard configuration from the most recent masterchain state or from masterchain state corresponding to <block-id-ext>
getconfig [<param>...]  Shows specified or all configuration parameters from the latest masterchain state
getconfigfrom <block-id-ext> [<param>...]       Shows specified or all configuration parameters from the masterchain state of <block-id-ext>
getkeyconfig <block-id-ext> [<param>...]        Shows specified or all configuration parameters from the previous key block with respect to <block-id-ext>
saveconfig <filename> [<block-id-ext>]  Saves all configuration parameters into specified file
gethead <block-id-ext>  Shows block header for <block-id-ext>
getblock <block-id-ext> Downloads block
dumpblock <block-id-ext>        Downloads and dumps specified block
getstate <block-id-ext> Downloads state corresponding to specified block
dumpstate <block-id-ext>        Downloads and dumps state corresponding to specified block
dumptrans <block-id-ext> <account-id> <trans-lt>        Dumps one transaction of specified account
lasttrans[dump] <account-id> <trans-lt> <trans-hash> [<count>]  Shows or dumps specified transaction and several preceding ones
listblocktrans[rev] <block-id-ext> <count> [<start-account-id> <start-trans-lt>]        Lists block transactions, starting immediately after or before the specified one
blkproofchain[step] <from-block-id-ext> [<to-block-id-ext>]     Downloads and checks proof of validity of the second indicated block (or the last known masterchain block) starting from given block
byseqno <workchain> <shard-prefix> <seqno>      Looks up a block by workchain, shard and seqno, and shows its header
bylt <workchain> <shard-prefix> <lt>    Looks up a block by workchain, shard and logical time, and shows its header
byutime <workchain> <shard-prefix> <utime>      Looks up a block by workchain, shard and creation time, and shows its header
creatorstats <block-id-ext> [<count> [<start-pubkey>]]  Lists block creator statistics by validator public key
recentcreatorstats <block-id-ext> <start-utime> [<count> [<start-pubkey>]]      Lists block creator statistics updated after <start-utime> by validator public key
checkload[all|severe] <start-utime> <end-utime> [<savefile-prefix>]     Checks whether all validators worked properly during specified time interval, and optionally saves proofs into <savefile-prefix>-<n>.boc
loadproofcheck <filename>       Checks a validator misbehavior proof previously created by checkload
pastvalsets     Lists known past validator set ids and their hashes
savecomplaints <election-id> <filename-pfx>     Saves all complaints registered for specified validator set id into files <filename-pfx><complaint-hash>.boc
complaintprice <expires-in> <complaint-boc>     Computes the price (in nanograms) for creating a complaint
known   Shows the list of all known block ids
knowncells      Shows the list of hashes of all known (cached) cells
dumpcell <hex-hash-pfx>
Dumps a cached cell by a prefix of its hash
dumpcellas <tlb-type> <hex-hash-pfx>
Finds a cached cell by a prefix of its hash and prints it as a value of <tlb-type>
privkey <filename>      Loads a private key from file
help [<command>]        This help
quit    Exit
