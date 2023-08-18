# Intermittent-counter
## Description:
This collector is designed for the fsp430fr4133 board. The collected data will be protected by ECC and checkpoint mechanisms.
## mechanisms:
### ECC
We use hamming code to protect the data
### rollback and checkpint
1. I use two pointer to record the start of data and end of data.
2. If we fould that the latest data has a problem by ECC, we can move the end of pointer to previous place to rollback our system.