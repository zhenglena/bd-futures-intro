### Reading a Future

Expected time required: 15 min

We are working on a utility for Amazon Music that will allow users to access stats about their listening habits
while using their account. Fun facts like how many times they have listened to a playlist, or what are their top
music genres. 

Continuing the work from last time, we are adding a new method in in `MusicAccountRetriever` called
`retrieveAccounts(List<String> accountIDs)`. This method takes in a list of account IDs, and returns an imported
list of `AmazonMusicAccount` associated with those IDs from the `MusicAccountService` database. 

To complete this assignment, you must pass all the unit tests. To do so:

- Complete the method `retrieveAccounts(List<String> accountIDs)`. The method will take the list of account IDs
  and use an `ExecutorService` to generate a list of `Future<AmazonMusicAccount>` objects. You just have to
  iterate through that list to obtain the `AmazonMusicAccount` objects from it.
- Have a Try/Catch block for the exceptions you throw for obtaining the results.
  - For `InterruptedException`, print the message "`MusicAccountStatsManager` was interrupted."
  - For `ExecutionException`, print the message "`ImportAccountTask` threw an exception."

Verify that the tests in `tst` pass.

HINT:
* [Do I need to worry about blocking time?](hints/hint-01.md)
* [IntelliJ isn't generating all the imports I need.](hints/hint_02.md)
