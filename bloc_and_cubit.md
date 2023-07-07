# Bloc
## Usage
Manage states that need to be updated asynchronously, such as data from backend, data from other API, future processes, etc
## States
- has bool isLoading
- has bool isRebuild
- has bool isError
- has String errorMessage
- has String action
- and other states
## onEvent
- validate parameters (if any)
- emit isLoading true
- get and process asynchronouse data
- emit states and isLoading false
- emit states with errorMessage
## States
- use model (mixin entities) that have error, msg, and data

# Cubit
## Usage
Manage states that did not need to be asynchronous such as settings, options, errors, etc
- has bool isRebuild
- has bool isError
- has String errorMessage
- has String action
- and other states
## void Function
- validate parameters (if any)
- emit isRebuild true
- process synchronouse states
- emit states with isRebuild false
- emit states with errorMessage
# States
- use entities
