# quest-submissions

## Chapter 1 Day 1 Quests


1-Explain what the Blockchain is in your own words:
  -An immutable and traceable chronological chain database that is linked together through cryptography

2-Explain what a Smart Contract is. You can read this to help you

-They are programming in the block chain. Error free because they are intelligent, automated, digital and without intermediaries.

3-Explain the difference between a script and a transaction.

-the script is the common language used between the parties of a transfer to be able to execute the exchange of the token.

-The script is an instruction "embedded in the transaction" is an algorithm used to communicate orders.  It is the language in which transactions are communicated

-It would be like serotonin transfers


### Chapter 1 Day 2 Quests

1.Safe - because of the structure of the language
Clarity - easy to read language
Approachability - easy to write language
Developer Experience - easy to track errors in the code
Resource Oriented Programming - resources are what we will need to work with.

2.This is a language specially created for smart contracts. The laconically constructed structure makes it easy to audit the code. Which increases the security and clarity of the code. The language is designed in such a way, that you can easily to learn to write the code not only with experience but also without programming skills. Cadence is resource-oriented, which makes it unique and helps a lot in working with blockchain.
----------


***Chapter 2 Day 1


Contract Deployment:


pub contract JacobTucker {

    pub let is: String

    init() {
        self.is = "the best"
    }
}



<img width="941" alt="Captura de pantalla 2022-06-23 090513 QUEST 2 DAY 1" src="https://user-images.githubusercontent.com/90107106/175334221-84086222-4dc5-4972-bb3d-626eb0dfa8d6.png">




Script Result:


  import JacobTucker from 0x03

  pub fun main(): String {
      return JacobTucker.is
  }



<img width="946" alt="Captura de pantalla 2022-06-23 091424 quest2 day1 script" src="https://user-images.githubusercontent.com/90107106/175335039-c734852f-db15-4c9a-a275-780f74928b78.png">


***Chapter 2 day 2

 ·Explain why we wouldn't call changeGreeting in a script?

 Because we would need to send the transaction, since we cannot modify the script, we could only visualize the information in the block chain.

 •What does AuthAccount mean in the transaction preparation phase?

 It has the functionality of being able to read the account data, after signing or approving the transaction by the user

 •what is the difference between the preparation phase and the execution phase in a transaction?

 In the preparation phase is where all the user data and information are, while we could not access that information in the execution phase.  We could execute everything in the preparation phase but we use the execution phase to give clarity in the execution of changes in the blockchain

contract

  pub contract JacobTucker {

      pub let is: String
      pub var myNumber: Int

      init() {
          self.is = "the best"
          self.myNumber = 0
      }

      pub fun updateMyNumber(newNumber: Int) {
          self.myNumber = newNumber
      }
  }
  
  
  <img width="958" alt="Captura de pantalla 2022-06-24 093257 1,1" src="https://user-images.githubusercontent.com/90107106/175497380-fce84c48-a1f0-4248-b14c-efbda401a021.png">


script

import HelloWorld from 0x01

pub fun main(): Int {
        return HelloWorld.myNumber
}


<img width="958" alt="Captura de pantalla 2022-06-24 092624" src="https://user-images.githubusercontent.com/90107106/175497871-4d7c4550-451f-4d6c-851a-e6bafe292f65.png">


transaction

import HelloWorld from 0x01

transaction(myNewNumber: Int) {

  prepare(signer: AuthAccount) {}

  execute {
    HelloWorld.updateMyNumber(newNumber: myNewNumber)
  }
}


<img width="958" alt="Captura de pantalla 2022-06-24 093117" src="https://user-images.githubusercontent.com/90107106/175498111-66c63213-912e-43ec-814b-d2e6813185b0.png">


output screen


<img width="958" alt="Captura de pantalla 2022-06-24 093212" src="https://user-images.githubusercontent.com/90107106/175498243-e8fd6b37-b634-4e71-a232-c697de20a393.png">

```Cadence
Your Cadence codes in here
```

and github will turn it to code for you


