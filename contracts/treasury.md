# Treasury

## SANCT / USDC LP

* V1

## Treasury

The treasury contract is a simple vault implementation holding all the funds
collected by the protocol. If for instance a user purchases a DAI bond, the
bonded DAI is fully taken in by the treasury in return of the market equivalent
of SANCT bonded for. New SANCT will be minted based on the RFV of the treasury
assets. Below are listed treasury contracts by version, where the latest version
represents the currently active contract.

* V1

The treasury contract is guarded by a 4 of 7 multisig. That means any
transaction for the treasury must be approved by at least 4 signers, of which we
have 7 signers in total. The operation security for our treasury assets is thus
protected from a single actor going rogue, because it takes a quorum of 4 to
authorize any transaction like moving funds in and out. The 7 signing addresses
for our treasury are listed below.

Note that the DAO and the Treasury signers are the same, since the DAO is the
manager of the Treasury contract.

1. 0xPoo
2. Asylum
3. TBA
4. TBA
5. TBA
6. TBA
7. TBA