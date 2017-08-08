#  Donation Matcher Solidity Contract


This script is a "smart" donation contract developed on solidity. Main features of this donation contract are the following:
* Customizable beneficiary (you choose any beneficiary who has an Ethereum wallet)
* Customizable multiplier (you choose percentages to add on the top of the contributed donation)
* Customizable deadline (you choose the date when contract stops to send donations to the beneficiary. After this date you may use destroy option)
* Destroy option (you may take your deposited Ethers back)

## Usage

You can run this script with solidity 0.4.2.
Usage example: you want to collect donations for Moscow Zoo bears and add extra sum for every donated Ether. Your steps:
1. Paste this contract into Ethereum Wallet Contracts source code field.
2. Indicate account you will use for this contract.
2. Indicate Moscow Zoo's Ethereum Wallet address as beneficiary address.
3. Indicate deadline (note: use Unix time).
4. Indicate percentages you want to add on the top of the donated Ethers (_for example, Alice donated 20 Ethers and you want to add your 10% on the top of 20 Ethers, i.e. transfer 22 Ethers to the beneficiary_). Indicate 0 if you do not want to add extra percentages
5. Deploy contract.
5. After the contract is deployed you need to transfer Ethers to this contract (the amount of Ethers you sent to the contract serves as a deposit for the contract. Note: if you chose to add extra percentages on the top of the donated Ethers, contract will use these deposited Ethers to send added amount of Ethers to the beneficiary).
6. After the deadline you may use "Destroy" option to send your deposited Ethers back to you. Note: if you added percentages on the top of the donated sums, the contract will send you the rest of the deposited sum.
