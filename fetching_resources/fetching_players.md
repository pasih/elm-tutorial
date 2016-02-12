# Fetching players

The next step is to fetch the list of player from the fake api we set up before.

## Main Model

Remove the hardcoded list of players in __src/Model.elm__

```elm
initialModel : AppModel
initialModel =
  { players = []
  , routing = Routing.initialModel
  }
```

## Players Actions

Add a new import and action to __src/Players/Actions.elm__

```elm
...
import Http

type Action
    ...
    | FetchAllDone (Result Http.Error (List Player))
```

`FetchAllDone` will be called when we get the response from the server. This action will have a `Result` payload that will either contain an `Http.Error` or a list of players.

## Players Effects

## Players Update

## Main