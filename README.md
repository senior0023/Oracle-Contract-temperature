https://ropsten.etherscan.io/address/0x068Ff850D30d0cf7F827947acc1e5100A35b091E#readContract

Contract
- Provide a setter for the temperature
setter method for every user
- Provide a getter for the temperature
getter view for every user

- How to ensure we are decentralized and without a single point of failure?
because of using solidity in ropsten network, this project certainly will be sure decentralized one
- How do we determine who can submit the temperature?
to set temperature, user should insert geo info of longitude and latitude, user's browser will support this feature and can detect if setter is valid user(not bot), also will confirm if the temperature is valid
- How can we make sure no one is submitting wrong values?
Will build a bot which is listening the event of Added, then if bot receive Added event, will confirm the value is valid based on online service and geolocation info
So can confirm if the value is right or wrong and also will calculate the outlier
- How do we detect outliers?
Oracle bot(event listener) will observe the status of contract and will calculate the outlier based on online service
For example, if the outlier is out of 10~15%, bot will decide tx is wrong tx and will remove that value of contract
To implement this feature, oracle bot has balance of this address
