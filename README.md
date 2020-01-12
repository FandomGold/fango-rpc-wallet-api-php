# fango-rpc-wallet-api-php
This is the API library for the Fandom Gold rpc-wallets in PHP.
For the wiki, refer to this url: https://github.com/FandomGold/fandomgold/wiki/RPC-wallet-API-methods

How to use it?  
Look into the `index.php` file to see an example.  
  
What to do with empty value's?  
We're going to use `getTransactionHashes` for an example. Click [here](https://github.com/FandomGold/fandomgold/wiki/RPC-wallet-API-methods#getBlockHashes) to see the arguments.
~~~php
<?php
include('service.php');

/* For every value that needs to be empty u just fill in '' */
$RpcTest = new FandomGold_RpcClient("spookypool.nl", "12345", "hi");
print_r($RpcTest->getTransactionHashes(
  'fango2nGK6YRwYThLiqEer2UinJUqvQdTC8LYK82aVyQ9uyDVKTdC8M7ugDwpdbpSweYpgLcu318zZAN3FVzzLkRLQxDkQWtRmg',
  '',
  1,
  10,
  ''
));
?>
~~~
