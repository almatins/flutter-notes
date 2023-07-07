# Clean Archicteture Flutter

## Config
- themes
- translations
- routers

## Core
- constants
- errors
- networks
- utils
- use_cases_abstract
- resources
  - data_states.dart (for entire network call response)
    - abstract DataState<T>
    - DataSuccess<T> extends DataState
    - DataFailed<T> extends DataState
## Features (each)
### Data
- data_sources
  - local
  - remote
- models
  mixin of entities.
- repository_impl
### Domain (totally independent from other layers)
- entities
  business object
- repository_abstract
- use_cases_impl
### Presentation
- bloc
- cubit
- pages
- widgets

# Sequence
- Domain > Entities
- Domain > Repository (bridge between the Domain - Repository - Data)
  only interfaces, the implementation will be on the Data layer.
  abstract class
- Data > Models
  Mixin entities. to keep the entitites independent from other layers
- Data > Repository Implmentation
  use models, and not entities
- 
