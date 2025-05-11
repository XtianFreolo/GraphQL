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


INTERMEDIET TASK

list the first 5 characters and the starshipsnthey piloted:

query myQuery {
  allPeople(first: 5) {
    people {
      name 
      starshipConnection{
        starships{
          name
          model
        }
      }
    }
  }
}


5 species and their language:

query MyQuery {
  allSpecies(first: 5) {
    species {
      name
      language
    }
  }
}

planets and their climates:

query myQuery {
  allPlanets(first: 5) {
    planets {
      name
      climates
    }
  }
}

vehicles and their cost: 

query myQuery {
  allVehicles(last: 3) {
    vehicles {
      name
      costInCredits
    }
  }
}

ADVANCED TASK

All characters in specific film:

query myQuery {
  allFilms(first: 1) {
    films {
      characterConnection {
        totalCount
        characters {
          name
        }
      }
    }
  }
}


Character that has more than one film: 
lets use palpatine

query myQuery {
  person(id: "cGVvcGxlOjIx") {
    name
    filmConnection {
      totalCount
      films {
        episodeID
      }
    }
  }
}


Aggregated film Stats:

query MyQuery {
  allFilms {
    totalCount
    films {
      title
      characterConnection {
        totalCount
        characters {
          name
        }
      }
    }
  }
}



COMPLEX TASK

Full Char profile
lets use palpatine 


{
  person(id: "cGVvcGxlOjIx") {
    name
    homeworld {
      name
    }
    filmConnection {
      films {
        title
      }
    }
    starshipConnection {
      starships {
        name
        model
      }
    }
  }
}

NABOOOO!!

Link first 5 char with their planets:

query myQuery {
  allPeople(first: 5) {
    people {
      name
      homeworld {
        name 
        population
      }
    }
  }
}

Vehicles, Their Pilots, and Pilots' Species:

query MyQuery {
  allVehicles(last: 3) {
    vehicles {
      name
      model
      pilotConnection {
        pilots {
          name
          id
          species {
            id
          }
        }
      }
    }
  }
}

First 3 movies, list related char, planet and starships. 

query MyQuery {
  allFilms(first: 3) {
    films {
      title
      characterConnection {
        characters {
          name
        }
      }
      planetConnection {
        planets {
          name
        }
      }
      starshipConnection{
        starships {
          name
        }
      }
    }
  }
}















