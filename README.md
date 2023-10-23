# GAS OPTIMSATION

- Your task is to edit and optimise the Gas.sol contract.
- You cannot edit the tests &
- All the tests must pass.
- You can change the functionality of the contract as long as the tests pass.
- Try to get the gas usage as low as possible.

## To run tests & gas report with verbatim trace

Run: `forge test --gas-report -vvvv`

## To run tests & gas report

Run: `forge test --gas-report`

## To run a specific test

RUN:`forge test --match-test {TESTNAME} -vvvv`
EG: `forge test --match-test test_onlyOwner -vvvv`

- after changing the order : Deployment Cost: 2431979 | Deployment Size :11987

- erase getPaymentHistory() fuction because by default we already have the public array variable declared as a getter.
- erase senderOfTx to write msg.sender directly.
- erase the modifier onlyAdminOrOwner because we already ahve the contract already inherit of the ownable contract
- change the checkIfWhiteListed moidifier
- change the order of the struct element
