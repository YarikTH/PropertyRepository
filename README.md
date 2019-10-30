# PropertyRepository

Special framework that allows to have property tree ready for replication, persistent storage and change notification etc.
It should be thread unsafe by design.
At first I want a prototipe with PropertyRepository intended to be used mostly with runtime data.
Need start with just int values to make life easier.

## Things to see and try

* library to have values that calculated from another values https://github.com/schlangster/cpp.react
* slot-signal system to notify about changes (maybe doesn't need if we have reactive values and replication system)
  * https://en.wikipedia.org/wiki/Observer_pattern
  * note that value modification notifications should be sent only after change transaction is done, not immidiatly after value assign.
* property class to make values reading and modification easyer
* replication system (need automatic easy way to have read only copy of tree on remote mahine with minimum diffs)
  * note that some data shouldn't be replicatable (passwords etc)
  * note that reactive values should go in transaction automatically
* some way to make data change transactions (atomic change of several values)
* some variant like class to reduce amount of different complex classes


