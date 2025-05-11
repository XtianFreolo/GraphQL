Retrieve all the titiles: 

query MyQuery {
  allFilms {
    films {
      id
    }
  }
}

Get a specific character using their specific ID

query MyQuery {
  allPeople {
    people {
      id
      name
    }
  }
}

this gets the name of everyone then...

query MyQuery {
  person(id: "cGVvcGxlOjIx") {
    name
  }
}

that gets Palpatine 

First five planets

query myQuery {
  allPlanets(first: 5) {
    planets {
      name
    }
  }
}

Fetch names and models of 3 starships:

query myQuery {
  allStarships(first: 3) {
    starships {
      name
      model
    }
  }
}

