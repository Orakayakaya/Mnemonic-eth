# $ echo "legal winner thank year wave sausage worth useful legal winner thank yellow" > myfile
$ ./mnemonic_utils.py myfile

Mnemonic key > private key #2
from mnemonic_utils import mnemonic_to_private_key
private_key = mnemonic_to_private_key("legal winner thank year wave sausage worth useful legal winner thank yellow")

Private key > Mist keystore using eth-keyfile module
import binascii
import eth_keyfile
json_keyfile = eth_keyfile.create_keyfile_json(binascii.unhexlify(private_key), b"any password")

Private key > Mist keystore using web3.py module
import binascii
from web3.auto import w3
json_keyfile = w3.eth.account
